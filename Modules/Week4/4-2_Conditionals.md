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

Don't forget the spaces just inside of the square bracket

`ge` in this example is a **conditional operator** that means greater than or equal to

### Conditional Operators: Numbers


