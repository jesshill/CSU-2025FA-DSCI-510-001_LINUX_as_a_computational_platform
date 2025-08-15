# Working With Files 2

The following commands will help you to access and organize the information contained in files.

`cat` – concatenate. concatenate files together

`grep` – regular expressions. search for a specific pattern within a file

`cut` – pull out a specific column (or any other delimited information) from a file

### Let's make a file

**!!! Group Exercise:** 

To prepare for the exercise, please do the following …

1. Make a directory called `workingWithFiles`
2. Using nano, copy and paste the following content into a file called `chr_sizes.txt`

```
# a list of the yeast chromosomes and their lengths
chrIV	1531933
chrXV	1091291
chrVII	1090940
chrXII	1078177
chrXVI	948066
chrXIII	924431
chrII	813184
chrXIV	784333
chrX	745751
chrXI	666816
chrV	576874
chrVIII	562643
chrIX	439888
chrIII	316620
chrVI	270161
chrI	230218
chrM	85779
```

### Concatenating files with `cat`

The `cat` command reads one or more files and prints the output of all files to the screen. The output can be redirected to a file, as well, and in this way, we can join files together.

**concatenate usage:**

`cat <file.txt> …`

Typically, we join two different files together. For the purpose of example, let's try to duplicate the contents of our file using cat. The  `…` means you can keep adding more and more files.

```
$ cat chr_sizes.txt chr_sizes.txt
$ cat chr_sizes.txt chr_sizes.txt > double_sizes.txt
$ more double_sizes.txt
$ wc chr_sizes.txt
$ wc double_sizes.txt 
```

**!!! Challenge question:** If you had the following files in your directory, how would you concatenate them together using a wildcard?

```
$ ls
data1.csv data2.csv data3.csv data4.csv

$ 
```

### Searching for patterns using `grep`




