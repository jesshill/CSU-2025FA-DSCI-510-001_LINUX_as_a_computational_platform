# Assignment 6

- Due **Tuesday, September 16, 2025, 11:59 pm** 
- **DO NOT write out the questions. Do not write long descriptions. Only write your succinct answers.**
- **Turn in your answers as the .txt file on Canvas by uploading your file.**
- Assignments account for 70% of your final grade. 

## Question 1

- A. What echo statement would you use to print out your default language settings?
- B. What are they? (ie: copy and paste the output of A)
- C. What echo statement would you use to print out your terminal's environmental shell settings?
- D. What are they? (ie: copy and paste the output of C)

## Question 2

Finish this bash script.

The following bash script is halfway done. It is called printNameTags.sh. It will gather information interactively from a user and create a file called output_tag.txt that contains some user information.

Here is the code so far.

```
#!/usr/bin/env bash
 
# Prompt user for their name
echo -n "Print Name Tags>>> What is your name? Type and press [RETURN]: "
read username # The variable is called username and the value is set to what the person has typed
 
# Prompt user for their department
echo -n "Print Name Tags>>> What is your department? Type and press [RETURN]: "
read deptname # The variable is called deptname and the value is set to what the person has typed
 
# Prompt user for their department
echo -n "Print Name Tags>>> What is your university? Type and press [RETURN]: "
read uniname # The variable is called uniname and the value is set to what the person has typed
 
# Tell the user you are printing their nametag in the file output.txt
echo "Print Name Tags>>> Generating your name tag. It be found in output_tag.txt"
```

Complete the nametag script so that if I give it “Shuri Ajara”, “Engineering”, and “University of Wakanda” it will save the following in the file output_tag.txt:

```
Hello my name is Shuri Ajara
from Engineering
at University of Wakanda
```

## Question 3

Write a short script called tabToCSV.sh. It takes in as input, a tab-delimited text file and converts it to a comma-separated file, the output file.

Is executed like so…

```
$ bash tabToCSV.sh file1.txt
```

It creates a file called file1.csv. The content in file1.txt is then copied into a file called file1.csv with the tabs replaced by commas.

Here is an outline of how to write your script:

```
#!/usr/bin/env bash
 
# Capture the $1 argument as a variable called infile (will have the value file1.txt)
 
# Use string replacement to create a new variable called outfile (will have the value file1.csv)
 
# Use a sed or tr statement command to convert tabs to commas and re-direct the content to the output file
```

Complete the above script so it works to do the required task.

Try first: Try writing your output into the file called file1.csv by hard coding the redirect command like so within your script:

```
<code here> > file1.csv
```

Optional Bonus Challenge - read about **string replacement**. See if you can use string replacement to redirect the code into into a file that uses the input file (a .txt file) name and outputs it to a corresponding .csv file name. In this case, you would instead redirect using a command like so:

```
mytxtfile=$1
 
<some line of code here to create a new variable called mycsvfile by string replacing certain characters in $mytxtfile
 
<code here> > $mycsvfile
```

## Question 4 - Complete a gtf2bed.sh script

Below is a short but incomplete script called gtf2bed.sh. The script takes as input the [SARSCoV2_ncbiGenes.gtf]() file and outputs a .bed that lists the chromosome, start, stop, and strand information for each “exon”. That is, it will first filter for lines that contain the term 'exon', then extract out the 1st, 4th, 5th, & 7th columns. Then it will save the information in an output file.

Use any of the .gtf files used in this course as a practice/test file.

```
#!/usr/bin/env bash
 
# Create a variable for your desired input file
inputfile="SARSCoV2_ncbiGenes.gtf"
 
# Write a line of code below that will take the input file, select only exon entries, and convert those entries to .bed format (select rows 1,4,5, & 7. The output should be saved to a file called "SARS_Cov2_exons.bed"
 
# Write a line of code below that echos (prints out) a brief summary of what was done to the user.
```

- A. Copy your code into the answer key.
- B. Write down what you wrote on the command line to execute this code (hint: should start with bash)
- C. Copy and paste what you get when you execute the command $ head SARS_Cov2_exons.bed
