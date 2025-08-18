# Intro To Scripting 

### Chaining with ; 

So far, we've executed one command per line. However, we learned to pipe commands together, which is a way of combining two commands into one long command.

We can also execute two commands in succession. This is called chaining and it uses the `;` semi-colon.

**chaining usage:**

`command1; command2`

**!!! Exercise:** Try it:

```
$ mkdir testdir; touch testdir/testfile.txt
```

The shell waits for the first command to finish before the second command starts. You can command multiple commands together. Hmm, this seems very useful. If only there was a way we could build on this …

### What is a bash script? 

Next, we're going to level up and start saving our commands in files that can be executed. A simple such file is called a **script**. When scripts are written to be read by a linux shell, they are called **bash scripts**, and the process of coding in this way is called **bash scripting**.

To date, our interactions with the shell have been **interactive** similar to having a conversation with a person. Writing scripts will be analogous to writing a script for a movie or a play. In this way the conversations are written and recorded, to be recalled and acted out in a precisely defined order and in a precisely defined way at any time.

A **bash script** is simply a file that contains a list of linux commands. The **file extension** for bash scripts can take on a few different flavors, but for now we'll use `.sh` to identify them. The script is typically started with a special line called a **shebang** that answers the command line question `$ which bash` and looks like so:

```
#!/bin/bash
```

However, for this class, we'll get into the habit of using a slightly more complex shebang just because many people are running different types of shells. Our bash scripts will start like so:

```
#!/usr/bin/env bash
```

With minor exceptions, anything you can run normally on the command line can be put into a script and it will do exactly the same thing. Similarly, any commands you can put into a script can generally also be run on the command line.


### When do I use bash Scripts? 

If you have some reason to do the same **series** of commands over and over again, it is often best to write these commands into a script so that the process can be **automated** and **reproducible**.

Let's take an example. Say, I want to get into the habit of having the same sub-directory structure in every new project I start. I also want to have a readme file inside every project directory. I find myself doing the same list of commands every time I start a new project …

```
$ mkdir 01_input
$ mkdir 02_scripts
$ mkdir 03_output
$ touch README.txt
```

I can write these same commands into a script called `startProject.sh`. It looks like this …

```
#!/usr/bin/env bash
 
# Make three subdirectories
mkdir 01_input
mkdir 02_scripts
mkdir 03_output
 
# Start a readme file beginning with today's date and time:
touch README.txt
```

Let's take a look at each part of this script …

... picture
