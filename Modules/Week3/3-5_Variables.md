# Variables 

**Variables** are placeholders for information. The information can either stay constant throughout the script or change.

All programming languages use variables so if you are learning this concept here for the first time, welcome! You will see this concept again and again as you learn new languages.

Basically, a variable is just a **name** that is given to a **value**. Variables are **assigned** values using the syntax:

```
varname="value"
```

Then, the value can be accessed by typing the variable name after a dollar sign like this - `$varname` or with a fancier syntax like this - `${varname}`. This is called **dereferencing** a variable. For example, we can print out a variable's value using `echo` like so:

```
echo $varname
echo ${varname}
```

**!!! Demonstration:** within the bash script `roomNumbers.sh` we can assign the value “AZ E210” to a variable called `myroom`:

```
#!/usr/bin/env bash
 
myroom="AZ E210"
 
echo $myroom
echo ${myroom}
echo -e "Today's class is being taught in ${myroom}."
```

Then, when we execute `roomNumbers.sh` it should look like this:

```
$ bash roomNumbers.sh
AZ E210
AZ E210
Today's class is being taught in AZ E210.
```

#### How do I come up with good variable names? 

- can only be a string of characters and/or numbers
- cannot have spaces in them
- cannot start with a number
- best practice - do not make them all caps
- think of a name that is meaningful and will help you read the code

**Values** can be individual or multiples (called strings) of letters, numbers, symbols, spaces, special characters, returns, etc. Simple things can be assigned to variables without quotes, but complex things (especially spaces) require quotes. Either double or single quotes can be used but you must be consistent.

**!!! Major pitfall:**
- Use quotes around values that are comprised of characters or strings of characters. Avoid using quotes around numbers
- You cannot put spaces around the equals sign. The variable name and the value must be flush.

```
favoritenumber=42 # this works
favoritenumber = 12 # this doesn't work
favorite number=3 # this doesn't work
 
echo -e "my favorite number is ${favoritenumber}."
```

**!!! Examples:** Here are a few more examples of variable assignments:

```
homeDir="/nas02/home/e/r/erinosb"
favoriteNumber=42
favoriteLetter="E"
```

**!!! Exercise:** Favorite things





