# Loops

Loops let us cycle over a given block of code over and over again. In other words, executing the code will be iterative. A nice feature of loops is that each pass around the loop can execute the code in a slightly different way.

Types of loops. In LINUX, and in most programming languages, there are several commands that can be used to execute a loop-type flow.
- `for`
- `while`
- `until`
- `select`

For this lesson, we will learn:
- `for` loops - easy
- `while` loops - intermediate
- `while read line` loops - intermediate
- Tips & Tricks
- Looping over arguments

### `for` loops - easy

**!!! Warning** - Stuck in a loop? If you are stuck in an infinite loop, press `CTRL + C` 

The easiest loop in LINUX is a `for` loop that cycles over each element of an array variable. Before we get started, let's review array variables. Remember, array variables contain ordered elements. They are assigned like so …

```
houses=(Gryffindor Slytherin Ravenclaw Hufflepuff)
```

… and they are dereferenced like so …

```
echo -e ${houses[@]}
#or
echo -e ${houses[*]}
```

If we want to one-by-one, go through each element of an array and do something with that element, we can use a for loop. Here is the syntax:

**for usage - Python style**

```
for <var> in ${<array>[@]}
do
    <commands>
done
```

In this type of loop `for` is a command that is typed literally. `in`, `do`, and `done` are also commands that are typed literally. `array` is a variable that has already been defined elsewhere in your code. And `var` is a variable name you will choose. For each iteration of the loop, the variable `var` will store an individual element from the array as its value.

The first time around the loop `var` will represent the first element in the array. The second time around the loop, `var` will represent the second element. And so on.

What commands go inside the loop? Anything you want, really. I do recommend testing how your loop works first using an echo statement within it that dereferences `$var`. This will be helpful to ensure that everything is working properly.

**!!! Exercise:** Let's try this together. Let's make a Hogwarts houses array. Let's start giving some points to different houses using a script `givePoints.sh`. Start `givePoints.sh` and make it executable. Next, copy in the following code:

```
#!/usr/bin/env bash
 
#assign hogwarts houses to the array variable called houses
houses=(Gryffindor Slytherin Ravenclaw Hufflepuff)
 
# each element in the array variable houses will be sequentially accessed as the variable $housename
for housevar in ${houses[@]}
do
    echo -e "Ten points for $housevar"
 
done
```

Test it out! What happened?

**!!! Independent Exercise:** Try it out yourself.
- Write a script called `cycleNames.sh`
- Create an array variable called `labgroup` that includes all the members of your lab (or family or friend-group)
- Use a simple `for` loop to cycle over each person in `labgroup` and repeat a simple echo statement such as `“Hello, $member”` or `“$member, it's your turn for lab meeting”`.

### `while` loops

`while` loops are loops that test a conditional at each iteration of the loop. If the conditional statement is true, the code block is executed. If the condition is false, the loop stops.

**while usage**

```
while [ <some test> ]
do
    <commands>
done
```

Similar to what we learned in the `for` loops, the words `while`, `do`, and `done` must be literally written. The [ <some test > ] section is going to adhere to the rules and conventions we saw in the conditional section. And the commands can be anything we wish.

To achieve the proper behavior, our while loop will need three major components:

1. INITIALIZATION - where we start counter variable (i = 0)
2. CONDITION - where we check if our counter variable satisfies some conditional criteria (less than #, greater than #); and
3. INCREMENTALIZATION - where we reassign our counter by adding or subtracting 1 to/from it.

**!!! Example:** here is a loop that counts from 1 to 5. Let's call it `simpleCounter.sh`

```
#!/usr/bin/env bash
 
# INITIALIZATION of the counter variable x setting it to 1
x=1
 
# CONDITION - check whether x is less than or equal to 5? If TRUE - do a loop. If FALSE - go to the next code block.
while [ $x -le 5 ]
do
 
  echo "In this round of the loop x is equal to $x"
 
  #INCREMENTALIZATION - Add 1 to x
  x=$(( $x + 1 ))
 
done
 
echo "The code is complete"
```

We can also use while loops to access content within an array variable but it can be a little tricky …

```
#!/usr/bin/env bash
 
# INITIALIZATION of the counter variable x setting it to 1
x=1
 
# CONDITION - check whether x is less than or equal to the number of elements in the houses array? If TRUE - do a loop. If FALSE - go to the next code block.
while [ $x -le ${#houses[@]} ]
do
 
  echo "In this round of the loop x is equal to $x"
 
  echo "ten points to ${houses[$x]}"
 
  #INCREMENTALIZATION - Add 1 to x
  x=$(( $x + 1 ))  
 
done
```

OK, that's weird. It looks like it started accessing the second element, Slytherin, first. Why?

You'll recall that array variables start their counting on the number **0**. For this reason, we'll need to modify our code and start the iteration variable on 0. We'll also need to change the conditional -le (less than or equal to) to -lt (less than). If we don't do this, the loop will cycle too many times. Note, I also changed the comments, too.

```
houses=(Gryffindor Slytherin Ravenclaw Hufflepuff)
 
# INITIALIZATION of the counter variable x setting it to 0
y=0
 
# CONDITION - Is x is less than the number of elements the number of elements in the houses array? If TRUE - do a loop. If FALSE - go to the next code block.
while [ $y -lt ${#houses[@]} ]
do
 
  echo "In this round of the loop x is equal to $y"
 
  echo "ten points to ${houses[$y]}"
 
  #INCREMENTALIZATION - Add 1 to y
  y=$(( $y + 1 )) 
 
done
```

**!!! Tip:** Incrementing numeric variables using x++

if we have a numeric variable called x that is assigned the value 0, we can add one to this variable each time we go around the loop with the following x++ syntax …

```
x=0
 
while [ $x -le 5 ]
do
  echo "x is equal to $x"
 
  ((x++))     # Means the same as x=$(( $x + 1 ))
 
done
 
# similarly, "((x--))" will decrease the value by 1.
```

**!!! Independent Exercise:** 
- Comment out the `for` loop you wrote in `cycleNames.sh`, your code that cycles through group members and tells each person when to give lab meeting. Replace that `for` loop with a `while` loop that yields the same output - prints an echo statement that includes each member's name.




