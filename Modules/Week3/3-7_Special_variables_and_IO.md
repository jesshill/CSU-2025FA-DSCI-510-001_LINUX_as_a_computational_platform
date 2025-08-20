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

We can have the user supply the input interactively using the command read

**!!! Exercise:** 
- Create a new directory called moreScripting
- In that directory, copy and paste some files from other places on your file system.
- Create a new script called wordCounter.sh.
- Copy and paste the following code into wordCounters.sh:

```
#!/usr/bin/env bash
 
echo "Type the name of the file do you want to count and press enter: "
read filetocount
 
wc -w $filetocount
```
