# Connecting to Remote Computers 

### Todays objectives: 

<details>
  <summary>Click to expand/collapse</summary>

- **Vocabulary**
  - Substitution
  - File extension
  - Shebang
  - Shell scripting
  - Bash scripting
  - Commenting out
  - Variables
  - Values
  - Variable assignment, reassignment, & dereferencing
  - Integers v. floating point numbers

- **Things you should know how to do after this class**
  - Be able to make substitutions within files using `sed` or `tr`
  - Be able to string commands together using pipes and chaining; know
  - the difference between when you would use the two
  - Know the parts of a bash script (shebang, comments, commands)
  - Know that bash scripts either have the extension .sh or no extension
  - Know to comment your code as a best practice
  - Know that you will need to test your code as a best practice
  - Know how to execute a bash script using the command bash
  - Know best practices in the field
    - Stay organized
    - Back up your work
    - Comment your code
    - Test scripts every 1 – 3 lines
    - Make a test file
    - save versions
  - Know that any commands interpreted by the shell from the command line can also be executed in a script
  - Know how to write out echo statements
  - Know how to assign and reassign variables
  - Know how to dereference variables to reveal their associated values
  - Know what constitutes an allowed and good sense name for a variable
  - Capture output of a command as a variable
  - Know some basic math operations

- **Commands covered**
  - `sed`
  - `tr`
  - `; (chaining)`
  - `bash`
  - `echo`
  - `variable=value`
  - `variable=$(command)`
  - `variable=$((math expression))`
  - `$variable`
  - `${variable}`

</details>


### Reminder: 

HW 3 and 4 are due by 11:59 pm tonight!

### Test your understanding - take this quiz!

[Quiz 4](https://forms.gle/kbtffRSixFUx68h69)

### Connecting to remote computers

Up to this point, we have only used the terminal to interact with your **local** computer. Today we will talk about several ways we can use the terminal to interact with **remote** computers over the internet.

In some instances, we will **log into** a remote computer, also known as **connecting** to it. This will allow us to interact with that computer as if we had opened its terminal. With this access, we could navigate that computer's file structure, write new files, run jobs, or transfer files. It would be just like interacting with our local computer.

This differs slightly from **transferring files** between the remote computer and our local computer. We transferred files from UCSC Genome Browser to our local computer. In that instance, UCSC Genome browser set up a special **public-facing, read-only** directory of files that we could copy over to our computer but we wouldn't be able to write files there or run commands there.

What types of remote computers can we log into?

```
1. remote personal computers
2. servers or repositories (computing or file storage)
3. supercomputers
```

### Accessing remote computers with ssh - Secure SHell

**ssh usage**

`ssh <addressOfRemoteServer>`

`ssh [-l <yourloginname>] <addressOfRemoteServer> #that's a lower case “L”`



