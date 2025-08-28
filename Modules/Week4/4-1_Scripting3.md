# Scripting 3 - Control Flow

### Todays objectives: 

<details>
  <summary>Click to expand/collapse</summary>

---

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

---

</details>


### Reminder: 

HW 5 and 6 are due by 11:59 pm tonight!

### Test your understanding - take this quiz!

[Quiz 6](https://forms.gle/Ck9tM4q91brAZ8457)

Also, take this brief course [survey](https://colostate.az1.qualtrics.com/jfe/form/SV_01Jwotnp3Pa8fVs)!

### Control Flow

All the software we use in every aspect of our lives is running some sort of code in the background. Surprisingly, the vast majority of that code can be broken down into three simple programming structures: 1) **sequences**, 2) **conditionals**, and 3) **loops**. Together, these are the big three of **control flow** which refers to the concept of how code is wired together and the order in which blocks of code run.

<p align="center">
<img width="410" alt="controlFlow" src="https://github.com/jesshill/CSU-2025FA-DSCI-510-001_LINUX_as_a_computational_platform/blob/main/Images/sequence_cond_loops.png">
</p>

### Sequences

**Sequences** are actions that are completed in a specific order. **A** must be done first. Next **B**. Then **C**. Sequences are complete when all the actions in the sequence are complete.

Example:
- wake up
- take shower
- get dressed
- eat breakfast

In LINUX, the order of sequenced operations is dictated by the order of the lines of code. Each line is executed one at a time.

### Conditionals 

**Conditionals** (sometimes also called **selections**) are forks in the road. A question is asked and depending on the answer, either action **A** or **B** is chosen.

Example:
- If it's a weekday → go to the lab
- If it's a weekend → clean the house

In LINUX, conditionals are specified by `if` statements.

### Loops

**Loops** are similar to conditionals in that they also ask a question. However, the difference is that loops ask the same question over and over and over again until a set criterion is satisfied.

Example: Hammering a nail
- You ask - is the nail hammered in? No → hit the nail
- Now is the nail hammered in? No → hit the nail
- Now is the nail hammered in? No → hit the nail
- Now is the nail hammered in? No → hit the nail
- Now is the nail hammered in? No → hit the nail
- Now is the nail hammered in? No → hit the nail
- Now is the nail hammered in? Yes → stop hammering

In LINUX, there are different types of loops: `while`, `for`, `until`, and `select`. In the interest of time, we will only cover `while` and `for`.

These three structures are each very simple on their own, but combined together, a sophisticated complexity emerges.

Continue on to [Conditionals](4-2_Conditionals.md)
