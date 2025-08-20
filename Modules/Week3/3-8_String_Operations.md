# String Operations

In computer programming, a **string** is a sequence of characters. Variables often point to values that are strings. Sometimes we want to do operations on those strings. We can do this using **string operations**.

By far the most common string operations I perform are **replacements** which just means substitution. Another common operation is **sub-setting** or selecting out just a portion of the string, also called a **sub-string**.

**Replace a part of the string**

`<newvarname>=${<oldvarname>/<pattern>/<replacement>}`

Make a new variable `$newvar` that replaces one instance of “pattern” in `$oldvar` with “replacement”.

**!!! Exercise:** You can follow along on the command line:

```
oldvar="Colorado"
newvar=${oldvar/o/O}
echo $newvar #should output COlorado
```

**Globally replace a part of the string**

```
<newvarname>=${<oldvarname>//<pattern>/<replacement>}
```

Make a new variable `$newvar` that replaces ALL instances of “pattern” in `$oldvar` with “replacement”

```
oldvar="Colorado"
newvar=${oldvar//o/O}
echo $newvar # should output COlOradO
```

**Replace a prefix**

`<newvarname>=${<oldvarname>/#<pattern>/<replacement>}`

Make a new variable `$newvar` that replaces “pattern” at the BEGINNING of the string `$oldvar` with “replacement”.

```
oldvar="To be or not to be"
newvar=${oldvar/#To/So}
echo $newvar # should be "So be or not to be"
```

**Replace a suffix**

`<newvarname>=${<oldvarname>/%<pattern>/<replacement>}`

Make a new variable `$newvar` that replaces “pattern” at the END of the string `$oldvar` with “replacement”.

```
oldvar="file1.txt"
newvar=${oldvar/%txt/fastq}
echo $newvar # should be "file1.fastq"
```

**Subset a string** 

`<newvarname>=${<oldvarname>:<n>}`

Make a new variable `$newvar` that corresponds to the `$var` string starting at nth letter.

```
oldvar="California"
newvar=${oldvar:3}
echo $newvar # should be ifornia
```

**Subset a string of specific length** 

`<newvarname>=${<oldvarname>:<n>:<length>}`

Make a new variable `$newvar` that corresponds to the `$oldvar` string starting at nth letter and going for “length” letters.

```
oldvar="California"
newvar=${oldvar:3:4}
echo $newvar # should be "ifor"
```

Cheatsheet For String Replacement - Altering the Values of Variables








