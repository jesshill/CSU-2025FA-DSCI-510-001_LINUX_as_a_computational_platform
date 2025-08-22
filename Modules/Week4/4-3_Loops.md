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

