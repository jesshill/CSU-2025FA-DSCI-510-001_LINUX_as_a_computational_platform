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

[Quiz 4](https://forms.gle/Yzqwismcg5N1RB136)

### Try Alpine login again:  

- Navigate to https://ondemand-rmacc.rc.colorado.edu in a new tab or window
  - For me, I right-click on the above link and select **Open Link in New Window**
- Log into your "CSU NET ID". You will receive a "DUO PUSH" on your phone. Accept it.
- To access the LINUX command line on ALPINE, go to the **Clusters** menu. Select **>_Alpine Shell**
- In another window, you can also access your files by going to the **Files** menu and selecting any available directories.

For reference, see: [Connecting to remote computers](../../Resources/Connecting_to_remote_computers.md)

Keep learning: 
- DSCI 511 - Python
- DSCI 512 - RNA-seq
- [RC help events and training](https://www.colorado.edu/rc/events)
  - [Working with Linux](https://colorado.libcal.com/calendar/events/linux) a short course - Friday, August 29, 11am - 12pm
- [Coding & Cookies]() through the Morgan Library

### Array Variables

So far, we have assigned only a single value to each variable. We can also assign multiple, ordered values to a variable. These create **array variables**.

Arrays are zero-based. That is, the first element is accessed with the number 0.

**Assign values** to an array variable using parentheses:

```
arrayname=(value1 value2 value3 value4)
```

**Dereference** the list in a variety of different ways:

```
echo $arrayname
echo ${arrayname[*]}
echo ${arrayname[@]}
```

