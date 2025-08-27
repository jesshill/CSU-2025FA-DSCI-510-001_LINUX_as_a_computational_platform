# Tips and Tricks 

Here are some examples that are more complex than could be taught, but will be good to learn and incorporate on your own.

### Debugging

#### Shell options

It is useful during script development to turn on some features that change the default behavior of the shell.

#### `-n`: Read commands in script, but do not execute them

Here is “syntax_error.bash”:

```
#!/usr/bin/env bash
 
echo "this line is fine" 
echo "this line is not
```

```
$ bash -n syntax_error.bash
syntax_error.sh: line 5: unexpected EOF while looking for matching `"'
syntax_error.sh: line 6: syntax error: unexpected end of file

$ bash syntax_error.bash 
this line is fine
syntax_error.sh: line 5: unexpected EOF while looking for matching `"'
syntax_error.sh: line 6: syntax error: unexpected end of file
```

This example has a non-destructive first line, but consider an example where you don't want to run heavy commands, or try to delete a file, that only works the first time during debugging.

#### `-e` pipefail: Prevent the script from continuing after an error.

This stops the script if a command has a non-zero exit status (error), rather than a syntax error. This would be an issue if commands rely on previous commands to work successfully (as they almost always do).

```
#!/usr/bin/env bash
set -e
set -o pipefail
 
...
```

#### `-v`: Print out commands before running them

This can give you clues as to variable settings during run time, which may be unexpected.

```
#!/usr/bin/env bash
set -v
 
...
```

OR it can be specified on the command line:

```
$ bash -v print_arguments.sh 1 2 3
#!/usr/bin/env bash
 
 echo "The number of supplied arguments is $#"
The number of supplied arguments is 3
 
for param in $@
do
    echo $param
done
1
2
3
```

#### `-x`: Expand commands before running them

```
#!/usr/bin/env bash
 
number=10
 
if [[ $number -lt 5 ]]
then
    echo "$number is less than 5" 
else
    echo "$number is greater than or equal to 5."    
fi
```

```
$ bash -x  conditionals.sh 
+ number=10
+ [[ 10 -lt 5 ]]
+ echo '10 is greater than or equal to 5.'
10 is greater than or equal to 5.
```

### When `cut` doesn't work, use `awk`

The program awk has the ability to parse on multiple spaces as a single column.

File:

```
chr1 4   5
chr1   4  10
```

```
$ cut -f 2,3 different_whitespace.txt 
chr1 4   5
chr1   4  10

$ cut -f 2,3 -d ' ' different_whitespace.txt 
4


$
```

With awk, the syntax is more complex, but you can refer to columns by their own $1, $2, $3, etc. But, you have to hide them from the shell with single quotes.

```
$ awk '{print $2,$3}' different_whitespace.txt
4 5
4 10
$ awk '{print $1,$3}' different_whitespace.txt
chr1 5
chr1 10
```

[More on awk syntax with examples](https://www.geeksforgeeks.org/linux-unix/awk-command-unixlinux-examples/)

### `paste`

A counterpart to `cut`, there is paste.

Imagine you want to join two whitespace delimited files with the same number of rows.

**Text file 1 (left.txt):**

```
a   b
1   2
```

**Text file 2 (right.txt):**

```
c  d
3  4
```

```
$ paste left.txt right.txt
a   b	c  d
1   2	3  4
```

Like `cut`, the TAB character is the default delimiter with `paste`. But can be changed with the `-d` flag. Perhaps your files are *comma* separated values (.csv).

```
$ paste -d ',' left.csv right.csv
a,b,c,d
1,2,3,4
```

### Use `paste` to collapse lines in a file

`paste` works on a single file (with `-s`) to join the separate lines into a single line string.

```
$ cat seq.txt 
ggggatttagctcagttgggagagcgccagactgaagatctggaggtcct
gtgttcgatccacagaattcccacca

paste -s seq.txt 
ggggatttagctcagttgggagagcgccagactgaagatctggaggtcct	gtgttcgatccacagaattcccacca
```

Again, a TAB is inserted. Join on an empty string with `-d '\0'`

```
paste -s -d '\0' seq.txt 
ggggatttagctcagttgggagagcgccagactgaagatctggaggtcctgtgttcgatccacagaattcccacca
```

### Use `<( cmd )` to avoid a temporary file

Some pipes can't be used when a command doesn't accept input from STDIN.

```
# ideal pipe
command1 input.txt | command2 > final.out
 
# When command2 can't be piped into (no STDIN)
command1 input.txt > tmpfile
command2 tmpfile > final.out
rm tmpfile
 
 
# The tmpfile creation (and deletion) can be handled automatically with special syntax
command2 <(command1 input.txt) > final.out
```

The `<( command )` runs and the OS creates a temporary file which contains the output of `command`. You don't have to worry about creating and cleaning up temporary files.

The example:

`command2 <(command1 input.txt) > final.out`

Is equivalent to:

```
command1 input.txt > /tmp/tmpfile14587faf9
command2 /tmp/tmpfile14587faf9 > final.out
rm /tmp/tmpfile14587faf9
```

Where `/tmp/tmpfile14587faf9` is a temporary file that exists for the duration of the command only.

This is called **process substitution**.

### Calling an R script from BASH

R has an equivalent to positional parameters in BASH, and therefore you may pass arguments to it from the shell command line.

You must invoke your script (myscript.r) with the command **Rscript**, which should be installed with R.

```
$ Rscript myscript.r file1 param1
```

The contents of **myscript.r**:

```
userArgs = commandArgs(trailingOnly=TRUE)
file1 = userArgs[1]
param1 = userArgs[2]
```

### fasta to string

This only works on a fasta file with a single sequence.

1. Remove header (save in a variable)
2. Collapse sequence lines with an empty string (save in a separate variable)

```
seq_header=$(grep '>' seq.fasta)
seq=$(paste -s -d '\0' <(grep -v '>' seq.fasta ) )
```

#### Explanation:

paste is one of the commands that doesn't accept STDIN, therefore, we can use the process substitution method described above to remove the header using `grep -v '^'`.

As described above, paste can join lines in a file (using `-s`), collapsing the multiple lines of the fasta sequence into a single, unbroken string (with `-d '\0'`). It can now be processed with downstream programs that work one line at a time, such as grep and sed.

The `var=$( pipe )` construct saves the output of `pipe` into the variable `var`. Therefore, **seq_header** and **seq** are recorded as the output of their corresponding commands/pipes.

You could now search the sequence for a motif without worrying about line breaks (for example, using sed as a restriction enzyme).

```
echo $seq | sed 's/gaa[tg]/ CUT /g'
ggggatttagctcagttgggagagcgccagact CUT atctggaggtcctgtgttcgatccaca CUT tcccacca
```
