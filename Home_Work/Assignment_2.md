# Assignment 2

- Due **Tuesday, September 2, 2025, 11:59 pm** 
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

## Preparation for the exercise

- Download the following file: [genomes_2018.tgz](https://github.com/jesshill/CSU-2025FA-DSCI-510-001_LINUX_as_a_computational_platform/blob/main/Data/genomes_2018.tgz)
- Extract it by either double-clicking on it OR navigating to where the file is located and executing:

```
$ tar -zxvf genomes_2018.tgz
```
- Navigate into the directory `genomes_2018`
- The directory contains 11 .txt or .gtf files.

## Question 1

A. How would you rename `sc3_chrom_sizes.txt` to `scerevisiae.txt`? Write the full command line including any necessary arguments or options.

B. How would you read the file `README_download.txt`? Write the full command line including necessary arguments and options.

## Question 2

A. This directory is a little messy. To organize it, make the following directories: `01_readme`, `02_annotations`, `03_chromsizes`. What single command line did you use?

B. How would you move the file `README_download.txt` into the directory `01_readme`? Write the full command line (including arguments and options).

C. How would you move **all** the .gtf files into the directory `02_annotations` using a single command? *(hint: use a wildcard)*. Again, full command line, please.

D. How would you move **all** the `_chrom_sizes.txt` files into the directory `03_chromsizes` using a single command? *(hint: use a wildcard)*. Again, full command line, please.

## Question 3

A. What command line would print out the first line of the file `hg38_annotation_head.gtf`?

B. What command line would print out the **last** 20 lines of the file `hg38_annotation_head.gtf`?

## Question 4

A. How many lines are in the file `README_download.txt`?

B. How many total lines are in all the .txt files (add up the number of lines in each .txt file)?

C. The .gtf files are all the same length. How many lines are in each of the .gtf files?

## Question 5

A. We haven't yet studied the command `du`. What command line can you execute in the terminal to learn more about `du`?

B. How would you use the command `du` to show how many megabytes of size comprises the entire directory `genomes_2018` in a human-readable format? Write the full command line.

C. How many megabytes is it?
