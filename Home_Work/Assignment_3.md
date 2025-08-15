# Assignment 3

- Due **Tuesday, September 9, 2025, 11:59 pm** 
- **DO NOT write out the questions. Do not write long descriptions. Only write your succinct answers.**
- **Here is a template to turn in:** [Assignment2_yourName.txt](https://github.com/jesshill/CSU-2025FA-DSCI-510-001_LINUX_as_a_computational_platform/blob/main/Home_Work/Assignment2_yourName.txt)
  - Copy and paste the template into a .txt file within a text editor such as BBEdit, Notepad++, or some other application. Do not use Word. Do not use TextEdit (MAC).
  - Remove <yourNameHere> and replace with your actual name
  - Remove <answerHere> and replace with your actual answer
  - Yes, remove the “<” and “>” characters, too
- **Turn in your answers as the .txt file on Canvas by uploading your file.**
- Assignments account for 70% of your final grade. 

---

**!!! Hint**: If the question asks for a command, write out the full command line entry as you would write it on the command line to generate the requested task.

---

## Question 1

- Let's download the C. elegans genome. Create a directory called `celegans` and navigate into it.
- Download the ce10 version of the C. elegans genome from UCSC Genome browser with one of the following commands:
- **Hint:** This is the 11th version of the C. elegans genome, so the ce11 is ce + one + one, NOT ce+ little L + little L.
- **Hint:** don't forget the last period in that `rsync` command. It tells rsync to use your current directory as the target directory.

```
$ rsync -avzP rsync://hgdownload.cse.ucsc.edu/goldenPath/ce11/chromosomes/ .
OR
$ wget --timestamping 'ftp://hgdownload.cse.ucsc.edu/goldenPath/ce11/chromosomes/*'

```

**Not working?** Click [here]() for more help.

- A. What is the md5sum you obtain for the file `chrI.fa.gz`?
- B. What command line would decompress **all** the .fa.gz files (in one command)? execute the command
- C. Now what is the md5sum for the expanded file `chrI.fa`?

## Question 2

If you did Exercise 1 correctly, you should have a directory containing individual fasta files for each *C. elegans* chromosome. Now, let's merge these individual chromosome files into one large genome fasta file.

- A. What command line would concatenate all the fasta files into a genome fasta file called `celegans_genome.fa`? execute the command
- B. Let's double-check that the file `celegans_genome.fa` contains seven concatenated chromosomes. What command line would you execute on `celegans_genome.fa` to give the following output?

```
>chrI
>chrII
>chrIII
>chrIV
>chrM
>chrV
>chrX
```

## Question 3



## Question 4



## Question 5


