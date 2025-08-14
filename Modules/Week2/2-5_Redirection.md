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
  - alias
  - ssh
  - rsync or wget (or sftp, curl, or scp – whichever works best for you)
  - md5sum or md5 or md5sum-lite
  - gzip
  - gunzip
  - `>`
2>
&>
>>
cat
grep
cut
| 
sort
uniq
tee

 
 
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

We can make a new directory 
