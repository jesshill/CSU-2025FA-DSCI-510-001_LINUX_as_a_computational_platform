# Making and Removing

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

**HW 1 and 2 are due by tonight!**

### Test your understanding

<details>
  <summary>Quiz</summary>
1. If you are located in the directory called "David", how would you navigate to the directory called "Users"?

<p align="center">
<img width="410" alt="quiz1" src="https://github.com/jesshill/CSU-2025FA-DSCI-510-001_LINUX_as_a_computational_platform/blob/main/Images/quiz1.png">
</p>

  - `cd David`
  - `cd ..`
  - `cd Users`
  - `cd /Users`
  - `cd /Users/Romario`

2. Which key on your keyboard will allow you to autocomplete the name of an unambiguous path?
- Return
- Shift
- Option
- ?
- Tab
- Caps
     
3. Which command lets you "see" what is in your current directory?
- `whoami`
- `hostname`
- `pwd`
- `ls`
- `currdir`
- `dir` 
   
4. Which command lists the "address" or "path" of your current directory?
- `whoami`
- `hostname`
- `pwd`
- `ls`
- `currdir`
- `dir`
  
</details>

### Moving around:
