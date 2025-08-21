# Scripting 3 - Control Flow

### Todays objectives: 

<details>
  <summary>Click to expand/collapse</summary>

- **Vocabulary**
  - Control flow
  - Sequences
  - Conditionals (also called selections)
  - Loops

- **Things you should know how to do after this class**
  - Be able to differentiate sequences, conditionals, and loops
  - Write a basic conditional statement using "if"
  - Write a basic conditional statement using "for"
  - Be able to use a string operation to replace file extensions
  - Be able to loop over a list of arguments supplied to the script using "$@"

- **Commands covered**
  - String operations:
    - `newvar=${oldvar/a/A}`
    - `newvar=${oldvar//a/A}`
    - `newvar=${oldvar/#To/So}`
    - `newvar=${oldvar/%txt/fastq}`
    - `newvar=${oldvar:3}`
    - `newvar=${oldvar:3:4}`
  - `if`
  - `else`
  - `elif`
  - `for`
  - `while`

</details>


### Reminder: 

HW 5 and 6 are due by 11:59 pm tonight!

### Test your understanding - take this quiz!

[Quiz 6]()

### Control Flow

All the software we use in every aspect of our lives is running some sort of code in the background. Surprisingly, the vast majority of that code can be broken down into three simple programming structures: 1) sequences, 2) conditionals, and 3) loops. Together, these are the big three of control flow which refers to the concept of how code is wired together and the order in which blocks of code run.


