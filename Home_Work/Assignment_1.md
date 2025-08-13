# Assignment 1

- Due **Tuesday, September 2, 2025, 11:59 pm** 
- **DO NOT write out the questions. Do not write long descriptions. Only write your succinct answers.**
- **Here is a template to turn in:** [Assignment1_yourName.txt](https://github.com/jesshill/CSU-2025FA-DSCI-510-001_LINUX_as_a_computational_platform/blob/main/Home_Work/Assignment1_yourName.txt)
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

Test the two commands below. Make sure to navigate away from your home directory to several different locations to test them in order to understand their full behavior. Explain what each command does.

```
$ cd ~
```
```
$ cd -
```

## Question 2

The grandparent directory: Can you find TWO ways to move into the grandparent directory in a single command? That is, how can you move from
`/Users/erin/Documents/Photos/Selfies/` to `/Users/erin/Documents/` by executing `cd` just once? Find TWO ways to do this. One way should use an **absolute path** and the other should use a **relative path**.

## Question 3

If I have several directories within my `Photos` directory, like so: 

`/Users/erin/Documents/Photos/Instagram/`

`/Users/erin/Documents/Photos/NikonPics/`

`/Users/erin/Documents/Photos/PanoShots/`

`/Users/erin/Documents/Photos/Selfies/`

How would I move from within the `Selfies` directory to the `Instagram` directory using one `cd` command that uses a **relative path**?

## Question 4

Say you have accidentally named a directory with spaces in the name `Files for Qualifying Exam`. You try to list the contents of this directory by executing the following command?

```
$ ls Files for Qualifying Exam
```

However, this doesn't work as expected.

A. Why doesn't this work? What is the computer trying to do?

B. What is the proper command required to list the contents of this directory?

## Question 5

Open [Terminus](https://web.mit.edu/mprat/Public/web/Terminus/Web/main.html) in a new tab. Explore this Linux game. To answer this question, name one command you learned from this game and the character who taught it to you.
