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

### Removing Directories

We can remove empty directories using `rmdir` (ReMove DIRectory):

**rmdir** <directoryname> …

**!!! Exercise:** Let's remove the “mynewdir” directory

```
$ ls
$ rmdir mynewdir
$ ls
```

**!!! More Exercises:** 

1. Through the terminal, navigate to the place in your computer where you want to store files for this class. If you haven't already made a directory specifically for this class, use `mkdir` to make that directory.
2. Navigate inside your new course directory.
3. Make some subdirectories for the course like “Assignments”, “Notes”, “Exercises”.
4. Check out your subdirectories using `ls`
5. Hmm, maybe those subdirectories don't sort the way you want them to. Delete the directories “Assignments”, “Notes', and “Exercises”.
6. You can add multiple directories by listing new directory names after `mkdir` separated by spaces: `mkdir dir1 dir2 dir3`
7. Using one `mkdir` command, make the directories “01_Notes”, “02_Exercises”, “03_Assignments”.
8. Now `ls` to see the subdirectories. 

### Making Files

Files are documents that live within directories. All files in the Linux environment should follow some naming standards …

- NO spaces
- NO weird characters (A-Z, 0-9, _, - are OK)
- Should contain a file extension (.txt, .docx, .png, etc)
- Should not be the name of a function (like ls)

**!!! Quick tip:** If you cannot see file extensions on your computer, take a moment to make these visible:
  - [MacOS show file extensions](https://www.idownloadblog.com/2023/05/23/how-to-show-hide-filename-extensions-mac/)
  - [Windows show file extensions](https://www.howtogeek.com/205086/beginner-how-to-make-windows-show-file-extensions/)

There are many ways to make a new file. We'll cover just a few: 

#### Making files with touch 

We can make a new file with **touch**:

**touch** <filename.txt>
