# Assignment 5

- Due **Tuesday, September 16, 2025, 11:59 pm** 
- **DO NOT write out the questions. Do not write long descriptions. Only write your succinct answers.**
- Here is a template to turn in: [Assignment5_yourName.txt](Assignment5_yourName.txt)
  - Copy and paste the template into a .txt file within a text editor such as BBEdit, Notepad++, or some other application. Do not use Word. Do not use TextEdit (MAC).
  - Remove and replace with your actual name
  - Remove and replace with your actual answer
  - Yes, remove the “<” and “>” characters, too
- **Turn in your answers as the .txt file on Canvas by uploading your file.**
- Assignments account for 70% of your final grade. 


## Question 1 - Read the exam assignment

For this question, read the exam assignment. Practice answering the first question. You don't have to commit to this answer for your actual exam.

*Select a standardized file type in your field. You can use any flat/text file formats listed in this Wikipedia page of scientific standardized file types. OR, you can pick any other file type that is flat. If you are a master's student or a graduate student not currently in a lab, you can pick any of the file formats we covered in class (.fa, .gtf) or go on the internet and try to learn more about how information is stored in the field or profession you eventually wish to join.*

**Answer the following:** What file type did you select? Describe the information that is gathered in your file type. If your file has columns, what is tabulated in each column? For full credit, you must explain how this information is organized - what are the column headers? What are the information blocks?

## Question 2 - brainstorm an exam project

Practice brainstorming what you might do for the Final Exam project. You don't have to commit to this project. It will be actually pretty tricky to determine what is feasible or not until you learn more about bash scripting. For this question, just try to brainstorm what you might **want** to do.

- A. What is the operation your script will perform?
- B. Why is this a useful operation to do in your field or in your project?
- C. Outline a few key commands or steps your script will do.

Having trouble? Think about how you might filter, sort, select, re-format, compile, quantitate, or display information from your text file in a way that would be meaningful.

## Question 3 - Alias

Do you recall how we used the command 'alias' to create a new command? Try to use alias to make the following new commands:

A. Write a new command called RNA2DNA that converts and RNA sequence to a DNA sequence. Have rna2dna work in the following way:

```
$ rna2dna rnafile1.txt > dnafile1.txt
```

Turn in the command line in which you define the alias command. Turn in the full line of code that allowed you to assign that alias.

B. Write an alias called txt2csv that converts tab-delimited text files to comma-separated value files. Have txt2csv work in the following way:

```
$ txt2csv file1.txt > file1.csv
```

Turn in the command line in which you define the alias command. Turn in the full line of code that allowed you to assign that alias.

## Question 4 - special variables

Alexi is working in the terminal to execute a shell script he has just written. This is what is on his terminal.

```
$ pwd
/user/alexip/dataproject1/
 
$ ls -1
image201.tif
image202.tif
image203.tif
image204.tif
image205.tif
processImages.sh
 
$ bash processImages.sh *.tif
```

What will be the values of the following special variables within Alexi's script when he executes the script (last line above)?

- A. $0
- B. $1
- C. $2
- D. $@
- E. $#
