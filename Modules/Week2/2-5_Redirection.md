# Redirection 

### Todays objectives: 

<details>
  <summary>Click to expand/collapse</summary>

- **Vocabulary**
  - Standard streams
  - Redirection
  - Standard input (stdin)
  - Standard output (stdout)
  - Standard error (stderr)
  - Concatenate
  - Regular expressions/regex
  - Delimiting character
  - Field
  - Pipe

- **Things you should know how to do after this class**
  - Understand what stdout, stderr, and stdin mean
  - Know how to redirect stdout, or stderr to an output file.
  - Know how to concatenate files together
  - Know how to search for simple strings in files
  - Know how to modify your search for simple strings using options
  - Know how to cut out delimited information from files
  - Know how to change the delimiter from a tab to another character (using cut)
  - Know how to use pipes to combine two commands into one

- **Commands covered**
  - `alias`
  - `ssh`
  - `rsync` or `wget` (or sftp, curl, or scp – whichever works best for you)
  - `md5sum` or `md5` or `md5sum-lite`
  - `gzip`
  - `gunzip`
  - `>`
  - `2>`
  - `&>`
  - `>>`
  - `cat`
  - `grep`
  - `cut`
  - `|`
  - `sort`
  - `uniq`
  - `tee`

</details>


### Reminder: 

HW 1 and 2 are due by 11:59 pm tonight!

### Test your understanding - take this quiz!

[Quiz](https://forms.gle/rmNNG3vXTzVgFc6X8)

### Standard Streams 

**Standard streams** are default input and output channels. In Linux, there are three standard streams: **stdin**, **stdout**, and **stderr**. You may also see input and output channels referred to as Input/Output or simply **I/O**.

<p align="center">
<img width="410" alt="stdin, stdout, stderr" src="">
</p>

**Standard Input**, or **stdin**, is input going into the shell. By default, this input comes from you typing on the keyboard.

When your run a command, say `wc file1.txt`, the shell sends its output to a special file called **standard output** (**stdout**), which by default is not saved in a directory, but is routed to the screen.

If you run an errant command, say `wc werkejtkhgo` when there is no file `werkejtkhgo`, an error message will be produced. The error message goes to a file called **standard error** (**stderr**) that is also routed to the screen by default.

**Redirection** allows us to circumvent the defaults, allowing us to redefine where standard output and standard error go. This is a useful way to capture information.

### Redirect output with >

Redirection of standard-output is performed using the `>` operator.














