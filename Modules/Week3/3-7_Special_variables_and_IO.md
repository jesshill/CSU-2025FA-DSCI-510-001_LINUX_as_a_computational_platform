# Special Variables & IO

How can we send information into a script? How do we get information out of script? This section will start to explore those concepts. Remember from before that this is called **Input/Output** or simply **IO**.

In this section, we're going to introduce **special variables**. In essence, special variables will allow us to access input that is supplied by the user as an argument. Before we get into the details of that, let's explore our options. How, generally, can we get data into scripts?

### Hard Coding

We can write the input into the script directly. If the input we're talking about is the name of a desired file, we can just write that name into the script itself.

```
#!/usr/bin/env bash
 
wc -w file1.txt
```

### Reading

We can have the user supply the input interactively using the command **read**

**!!! Exercise:** 
- Create a new directory called `moreScripting`
- In that directory, copy and paste some files from other places on your file system.
- Create a new script called `wordCounter.sh`.
- Copy and paste the following code into `wordCounters.sh`:

```
#!/usr/bin/env bash
 
echo "Type the name of the file do you want to count and press enter: "
read filetocount
 
wc -w $filetocount
```

- Make sure you know some of the filenames in your current working directory.
- Execute your script and see what happens:

```
bash wordCounter.sh
```

**Usage of read**

`read <variable name>`

`read` prompts the reader to type something and press enter. The entered keystrokes become the value assigned to the variable named in the command argument.

### Special Variables - passing input into scripts as arguments

We can also pass input into our script as arguments. These arguments can be typed in by the user as they execute the script on the command line like so:

`bash <shellscript.sh> [argument1] [argument2] …` 

Argument1 will be captured as a **special variable** that can be dereferenced using the syntax **$1** within the script itself. Argument2 can be dereferenced as **$2**. Special variables are initiated when you execute your code. They are useful for accessing information about how the script was executed.

Here's how we pass in arguments from the command line.

### List of special variables






