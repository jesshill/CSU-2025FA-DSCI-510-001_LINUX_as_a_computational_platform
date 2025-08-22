# Conditionals 

**Conditionals** are if/else statements that allow us to skip over blocks of code entirely based on passing or failing of a test. The simplest conditionals just involve the command `if`.

### `if`

If statements allow us to modify our code to only execute commands only **IF** a particular test is true. If a particular test is true, a set of actions are performed. If it is not true then don't perform those actions.

**if usage**

```
if [ <some test> ]
then
    <commands>
fi
```

**!!! Example:** Follow along. Imagine asking the user for their age. If they are over 21, let them in the club. Start the code `screenPatrons.sh`

```
#!/usr/bin/env bash
 
# prompt user for their age
echo -e "How old are you?"
 
read age
 
#Conditional statement
if [ $age -ge 21 ]
then
    echo -e "Welcome to the club!"
fi
```

Run your code: 

```
$ bash screenPatrons.sh
```

### The test statement

In an `if` statement, like in this one …

```
if [ <some test> ]
then
    <commands>
fi
```

… getting the test statement correct is a little tricky. The syntax needs to be very perfect.

```
if [ $age -ge 21 ]
```

Don't forget the spaces just inside of the square bracket!

`-ge` in this example is a **conditional operator** that means greater than or equal to

### Conditional Operators: Numbers

| Symbol | Comparison |
|--------| -----------|
| `-eq` | Returns true if two numbers are **equal** |
| `-ne` | Returns true if two numbers are **not equal** |
| `-lt` | Returns true if a number is **less than** another |
| `-le` | Returns true if a number is **less than or equal to** another number |
| `-gt` | Returns true if a number is **greater than** another number |
| `-ge` | Returns true if a number is **greater than or equal to** another number |

Here are some examples:

```
# Prints out a message if the value saved in myvar is less than or equal to 2023
if [ $myvar -le 2023 ]
then
  echo "your number is less than 2023"
fi
 
# Prints out a message if the value saved in myvar is equal to 42
if [ $myvar -eq 42 ]
then
  echo "You guess it! My favorite number is 42"
fi
 
# Prints out a message if the value saved in myvar is not equal to 42
if [ $myvar -ne 42 ]
then
  echo "That's not my favorite number. Keep guessing"
fi
```

For a detailed description of how these are used see: [Ryan's Tutorials: bash if statements](https://ryanstutorials.net/bash-scripting-tutorial/bash-if-statements.php)

**!!! Exercise:** Write a brief script called `numberReader.sh` that asks the user to type in a number. If the number is greater than 100, print out “That's a big number”

**!!! Potential Pitfall:** The following does not work ...

```
# Throws an error and doesn't work
if [$myvar -le 2023]
then
  echo "your number is less than 2023"
fi
```

**!!! Potential Pitfall:** In some situations, conditional statements work better with double square brackets

```
[[ if statement here ]] 
```

[More about single vs double square brackets](https://www.baeldung.com/linux/bash-single-vs-double-brackets#:~:text=The%20single%20bracket%20is%20a,brackets%20is%20generally%20more%20convenient.)

### `if/else`


Try running your `screenPatrons.sh` script again but now type in a number that is less than 21. Hmmm, it's not very satisfying. **if/else** statements can help with that. If the test is true, you can execute one block of code. If the test is false, you can execute a different block:

**if/else Usage**

```
if [ <some test> ]
then
    <commands>
else
    <commands>
fi
```

```
#!/usr/bin/env bash
 
# prompt user for their age
echo -e "How old are you?"
 
read age
 
#Conditional statement
if [ $age -ge 21 ]
then
    echo -e "Welcome to the club!"
else
    echo - "Scram, kid!"
fi
```


