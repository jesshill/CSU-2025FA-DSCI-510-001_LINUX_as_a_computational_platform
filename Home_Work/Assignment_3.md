# Assignment 3

- Due **Tuesday, September 9, 2025, 11:59 pm** 
- **DO NOT write out the questions. Do not write long descriptions. Only write your succinct answers.**
- **Here is a template to turn in:** [Assignment3_yourName.txt](https://github.com/jesshill/CSU-2025FA-DSCI-510-001_LINUX_as_a_computational_platform/blob/main/Home_Work/Assignment3_yourName.txt)
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
- Download the ce11 version of the C. elegans genome from UCSC Genome browser with one of the following commands:
- **Hint:** This is the 11th version of the C. elegans genome, so the ce11 is ce + one + one, NOT ce+ little L + little L.
- **Hint:** don't forget the last period in that `rsync` command. It tells rsync to use your current directory as the target directory.

```
$ rsync -avzP rsync://hgdownload.cse.ucsc.edu/goldenPath/ce11/chromosomes/ .
OR
$ wget --timestamping 'ftp://hgdownload.cse.ucsc.edu/goldenPath/ce11/chromosomes/*'

```

**Not working?** Click [here](extra_help_for_assignment3.md) for more help.

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

Use the file you made in Question 2 (above), celegans_genome.fa. Assume that the file blerg.jpg doesn't exist. Explain what will be saved in output.txt when you execute the following commands?:

```
A  $ wc celegans_genome.fa blerg.jpg > output.txt
B  $ wc celegans_genome.fa blerg.jpg 2> output.txt
C  $ wc celegans_genome.fa blerg.jpg &> output.txt
```

## Question 4

Let's look at the file md5sum.txt. What cut command line would you use to display just the md5 sums of each file, not the fasta file name, like so?

```
40ce7b39a878f3d6a77bc99f7e2175be
26f3335c9785bf5e4a749e1902123948
59e0901dee906259af8d1447483e3e0c
ef06d5359228a2ac60b0187aab5a36e7
812b2430b583a402ebfafcf6afa52026
1563b338c2138a73ac324b2fcc469d93
5ea698b2d176de906f420742bfc0bea3
```

## Question 5

For this next question, use this C. elegans annotation file below. Download it from google drive (click on it to take you to the google drive, then click on the down arrow key in the top right corner), move it to the same directory where you are working, and de-compress it.

[ce11_annotation_ensembl_to_ucsc.gtf.gz](https://github.com/jesshill/CSU-2025FA-DSCI-510-001_LINUX_as_a_computational_platform/blob/main/Data/ce11_annotation_ensembl_to_ucsc.gtf.gz)

A. What command line would you use to save the header information from `ce11_annotation_ensembl_to_ucsc.gtf` into a file called `annotation_information.txt`?

(**hint** - It should end up looking like below; **hint** - write the full line of code)

```
#!genome-build WBcel235
#!genome-version WBcel235
#!genome-date 2012-12
#!genome-build-accession NCBI:GCA_000002985.3
#!genebuild-last-updated 2014-10
```

B. What command line would you use to save the chromosome name, the start codon #, and stop codon # of every entry in `ce11_annotation_ensembl_to_ucsc.gtf` to a new file called `ce11.bed`?

(**hint**, they are in columns 1 & 4 & 5; **hint** - it takes a little while to print out; **hint** - peeking into the file ce11.bed would look like this)

```
#!genome-build WBcel235
#!genome-version WBcel235
#!genome-date 2012-12
#!genome-build-accession NCBI:GCA_000002985.3
#!genebuild-last-updated 2014-10
chrV    1480    3039
chrV    1480    3039
chrV    1480    1579
chrV    1480    1579
chrV    1480    1482
chrV    1691    1782
chrV    1691    1782
chrV    2851    3039
chrV    2851    3036
chrV    3037    3039
chrV    5690    6511
```
