# Array Variables

### Todays objectives: 

<details>
  <summary>Click to expand/collapse</summary>

- **Vocabulary**
  - Variables
  - Values
  - Variable assignment, reassignment, & dereferencing
  - Integers v. floating point numbers
  - Array variables
  - Array elements
  - Indexing
  - Special variables
  - Hard Coding
  - String
  - String operation
  - Replacement/substitution
  - Sub-setting strings
  - Sub-strings
  - The environment
  - Environmental variables
  - Startup files
  - Control flow

- **Things you should know how to do after this class**
  - Know how to assign and reassign variables
  - Know how to dereference variables to reveal their associated values
  - Know what constitutes an allowed and good sense name for a variable
  - Capture output of a command as a variable
  - Know some basic math operations
  - Know what an array variable is and how to assign values to one
  - Understand the basics of array indexing
  - Know how to enter input into a script by passing argument that can be accessed with a special variable
  - Know how to save output from a script using `>` and `>>`
  - Know a little bit about manipulating string variables
  - Understand that when strings are saved as the values of a variable, they can be manipulated using string operations.
  - Be able to describe the environment. Know that the shell stores information about the environment in environmental variables. Be able to dereference environmental variables on your terminal or within a script
  - Be able to differentiate sequences, conditionals, and loops

- **Commands covered**
  - `; (chaining)`
  - `bash`
  - `echo`
  - `variable=value`
  - `variable=$(command)`
  - `variable=$((math expression))`
  - `$variable`
  - `${variable}`
  - `arrayvariable=(value1 value2 value3)`
  - `${arrayvariable[*]}`
  - `${arrayvariable[@]}`
  - `${arrayvariable[0]}`
  - `${arrayvariable[1]}`
  - `${arrayvariable[#]}`
  - `${#arrayvariable[@]}`
  - `read`
  - `$0`
  - `$1`
  - `$2`
  - `$#`
  - `$@`
  - `$*`
  - String operations:
    - `newvar=${oldvar/a/A}`
    - `newvar=${oldvar//a/A}`
    - `newvar=${oldvar/#To/So}`
    - `newvar=${oldvar/%txt/fastq}`
    - `newvar=${oldvar:3}`
    - `newvar=${oldvar:3:4}`
  - `printenv`
  - `$USER`

</details>


### Reminder: 

HW 1 and 2 are due by 11:59 pm tonight!

### Test your understanding - take this quiz!

[Quiz](https://forms.gle/rmNNG3vXTzVgFc6X8)

### Standard Streams 

**Standard streams** are default input and output channels. In Linux, there are three standard streams: **stdin**, **stdout**, and **stderr**. You may also see input and output channels referred to as Input/Output or simply **I/O**.

<p align="center">
<img width="410" alt="stdin-stdout-stderr" src="https://github.com/jesshill/CSU-2025FA-DSCI-510-001_LINUX_as_a_computational_platform/blob/main/Images/stdin-stdout-stderr.png">
</p>
