# Assignment 4

- Due **Tuesday, September 9, 2025, 11:59 pm** 
- **DO NOT write out the questions. Do not write long descriptions. Only write your succinct answers.**
- **Here is a template to turn in:** [Assignment4_yourName.txt](https://github.com/jesshill/CSU-2025FA-DSCI-510-001_LINUX_as_a_computational_platform/blob/main/Home_Work/Assignment4_yourName.txt)
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

Download the file [dogBreeds.txt](https://github.com/jesshill/CSU-2025FA-DSCI-510-001_LINUX_as_a_computational_platform/blob/main/Data/dogBreeds.txt) that contains a list of every type of dog breed.

- Right click on the link and open in a new tab.
- Download the file by clicking on the down arrow.
- Save the file in a directory set aside for this homework assignment.
- Navigate into the directory containing this file on your terminal.

The following sequence of commands will print out to the screen the number of lines in the file `dogBreeds.txt` that match with the word 'Terriers' while excluding the comment line. However, this process involves making two different temporary files and three command line executions.

```
$ grep -v '#' dogBreeds.txt > dogs1_tmp.txt
$ grep -i 'Terrier' dogs1_tmp.txt > terriers.txt
$ wc terriers.txt
```

How could you use pipes to transform the same set of operations into a single line of code with no temporary files created?

A. Write the single line of code (again, hint - you should not be creating any temp files with your line of code (dont write any files in the process); this should be a piped series of commands!)

B. How many Terrier entries are there?

## Question 2

Again, using the same `dogBreeds.txt` file above, how would you use piped commands to do the following in a single command line?

1. Remove the comment lines
2. Display the line numbers of lines that contain the word “hound” or “Hound”

Your output will look like this:

```
3
20
22
24
35
42
48
50
58
59
72
74
77
80
102
104
105
156
160
186
194
200
210
232
235
243
244
246
254
255
263
264
265
266
316
323
338
342
353
360
362
377
381
387
388
398
411
415
441
447
448
457
458
464
477
482
507
511
512
513
522
550
559
567
575
577
587
588
590
```

A. What was the full command line you used to obtain your result?

**Hint** - If you're stuck on this one consider how you would answer the following: On which line does the entry for “Pug” appear?

## Question 3

**File Transfer practice:** Let's download the yeast annotation file from UCSC Genome browser. Like so:

Try the following commands:

```
$ rsync -avzP rsync://hgdownload.cse.ucsc.edu/goldenPath/sacCer3/bigZips/genes/sacCer3.ensGene.gtf.gz .
OR
$ wget --timestamping 'ftp://hgdownload.cse.ucsc.edu/goldenPath/sacCer3/bigZips/genes/sacCer3.ensGene.gtf.gz' -O sacCer3.ensGene.gtf.gz
```

A. Does your md5 sum match `6c2eea692f4bdd47655accd65fac45f0`? 

B. Unzip your annotation file. How many lines, words, and characters are in this file?

C. Save all the features that are on **chrII** into a new file called `chrII_entries.gtf`. How many features are on chromosome II?

## Question 4

**bed file**

A **bed file** is a tab-delimited flat file that contains the coordinates of genes. It is in the following form:

```
start_number   stop_number   Plus_or_minus_strand
```

Create a .bed file out of the sacCer annotation file (from Question 3) for all the Coding Sequences.

Break down the problem into steps:

- 1. How would you filter for lines that contain the terms “CDS”
- 2. How would you only select columns that contain start, stop, and strand?
- 3. To answer the question, turn in:

Please turn in the following:

- A. your command line(s). Needs to be the full line containing any arguments and options
- B. the wc output to your resulting bed file (That is - run `wc` on your resulting .bed file and copy that output over to your answer key)
- C. an explanation of how you tackled the problem. There are multiple correct answers.

## Question 5

Write one question you have about the material covered in class so far. Please don't ask what will be on the test or what will be covered next in the course. Your questions can reflect something that still isn't clear to you regarding what we have already learned, or it can be a question that is sparked from your curiosity. Your question can explore how you are thinking about linking the course content to other aspects of your research/life.

If you leave this blank or say “I don't have any questions”, you will receive 0 points.
