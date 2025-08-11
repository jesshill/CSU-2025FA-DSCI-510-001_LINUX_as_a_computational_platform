
# Paths

### Todays objectives: 

<details>
  <summary>Click to expand/collapse</summary>

- **Vocabulary**
  - Options
  - Manuals
  - Source (as in the source file in a copy cp command)
  - Target (as in the target file in a copy cp command)
  - Wildcards

- **Things you should know how to do after this class**
  - Know the difference between “command”, “argument” and “options” and be able to identify them
  - Realize you can glob options together (-a -l -s is the same as -als for most command options)
  - Be comfortable navigating manuals and knowing they are available as a help resource
  - Know how to make and remove directories
  - Know how to create files with touch or nano
  - Be comfortable navigating nano and using it to make changes to files
  - Know how to safely remove files and directories using rm
  - Peek into files using more and less and head and tail
  - Be comfortable using cp to copy files or directories in a few different ways (new file in the same directory, in a different directory, or with a new name)
  - Be comfortable using mv to move files and directories in different ways. Know the difference between cp and mv.
  - Know how to use wildcards * and ?
  - Know how to get help using man, help, command -h, or command --help

- **Commands covered**
  - ls – with commands
  - man <command>
  - mkdir
  - rmdir
  - touch <filename>
  - nano <filename>
  - rm
  - more
  - less
  - cp
  - mv
  - *
  - ?
  - .
  - head 
</details>

### Reminder: 

- Assignments 1 & 2 → submit on canvas, **DUE September 2nd by midnight**
- This course is short and should be a springboard to more learning such as:
  - [Boulder Computing Training Series](https://www.colorado.edu/crdds/events#research_computing-89)
  - [Coding & Cookies](https://libguides.colostate.edu/coding-cookies/home) in the Morgan Library at CSU

### Short in class quiz

<details>
  <summary>Quiz</summary>
1. If you are located in the directory called "David", how would you navigate to the directory called "Users"?

<p align="center">
<img width="410" alt="quiz1" src="https://github.com/jesshill/CSU-2025FA-DSCI-510-001_LINUX_as_a_computational_platform/blob/main/Images/quiz1.png">
</p>

  - cd David
  - cd ..
  - cd Users
  - cd /Users
  - cd /Users/Romario

2. Which key on your keyboard will allow you to autocomplete the name of an unambiguous path?
- Return
- Shift
- Option
- ?
- Tab
- Caps
     
3. Which command lets you "see" what is in your current directory?
- whoami
- hostname
- pwd
- ls
- currdir
- dir 
   
4. Which command lists the "address" or "path" of your current directory?
- whoami
- hostname
- pwd
- ls
- curridr
- dir
  
</details>

### Moving around: absolute paths v. relative paths

The types of paths we've used for navigating up to this point are called relative paths. This means that they only make sense from the perspective of the current working directory. In contrast, we can use cd to take us to absolute paths that would make sense anywhere on the computer system. Absolute paths always begin with the root directory, /. When we execute pwd, the shell spits out our current working directory as an absolute path because it start with a / such as /Users/erinnishimura/.
