# Making and Removing

In this section, we'll learn how to create or delete files and directories using LINUX commands.

### Todays objectives: 

<details>
  <summary>Click to expand/collapse</summary>

- **Vocabulary**
  - Source (as in the source file in a copy `cp` command)
  - Target (as in the target file in a copy `cp` command)
  - File transfer
  - File compression
  - File formats
  - Text files
  - Binary files
  - Text editor
  - File extensions
  - Checksums
  - Standard streams
  - Redirection
  - Standard input (stdin)
  - Standard output (stdout)
  - Standard error (stderr)

- **Things you should know how to do after this class**
  - Be comfortable using `cp` to copy files or directories in a few different ways (new file in the same directory, in a different directory, or with a new name)
  - Be comfortable using `mv` to move files and directories in different ways. Know the difference between `cp` and `mv`.
  - Know how to log into a remote computer, server, or supercomputer
  - Know one or two ways to transfer files from remote computers to your local computer
  - Know how to check whether your file was corrupted during transit.
  - Know the difference between text files and binary files.
  - Know that all your files should have file extensions.
  - Know a little bit about FASTA and GTF/GFF (Annotation) files
  - Know how to zip and unzip .gz/g-zipped files
  - Understand what stdout, stderr, and stdin mean
  - Know how to redirect stdout, or stderr to an output file.

- **Commands covered**
  - mv
  - cp
  - touch <filename>
  - nano <filename>
  - rsync or wget (or sftp, curl, or scp – whichever works best for you)
  - md5sum or md5 or md5sum-lite
  - gzip
  - gunzip
  - `>`
  - `2>`
  - `&>`
  - `>>`  
</details>


### Reminder: 

HW 1 and 2 are due by 11:59 pm tonight!

### Test your understanding

<details>
  <summary>Quiz</summary>

1. Which command line execution involves an absolute path?
  - `ls Users/Paul/Arakis`
  - `cd /Users/Jessica/Caladan`
  - `ls Admin`
  - `cd ..`
  - `cd /`
  - `pwd`
  - `ls -alh`

2. Which command line execution contains an argument?
  - `ls Users/Paul/Arakis`
  - `cd /Users/Jessica/Caladan`
  - `ls Admin`
  - `cd ..`
  - `cd /`
  - `pwd`
  - `ls -alh`
     
3. Which command line execution contains an option?
  - `ls Users/Paul/Arakis`
  - `cd /Users/Jessica/Caladan`
  - `ls Admin`
  - `cd ..`
  - `cd /`
  - `pwd`
  - `ls -alh`
   
4. Which line of code will print out the last line of a file?
- `head file1.txt`
- `tail file1.txt`
- `head -n 1 file1.txt`
- `tail -n 1 file1.txt`
- `more file1.txt`
- `less file1.txt`

5. Which of the following will match to c*.txt
- computer1.txt
- chromosomes.txt
- chr.txt2
- Chromosomes2.txt
- mitochondria.txt
- celegans.2txt

</details>

### Making Directories

We can make a new directory using the command `mkdir` (MaKe DIRectory):

**mkdir** <newdirectoryname> …

**!!! Quick tip:** The … means that you can add either one or more newdirectorynames.

**!!! Exercise:** Let's make a new directory called “mynewdir”

```
$ mkdir mynewdir
$ ls
```
