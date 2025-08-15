# More Pipes

Now that we know what piping is, we can discover some new functionalities of Linux. Let's learn how to pipe the following commands:

`sort` - sort lines in a file

`uniq` - find unique (or duplicated) lines in a pre-sorted file

`tee` - redirect stdout or stderr to multiple locations

**!!! Exercise:** Let's download a small file [mini.gff](https://github.com/jesshill/CSU-2025FA-DSCI-510-001_LINUX_as_a_computational_platform/blob/main/Data/mini.gff).

- To download, right-click and open in a new tab
- click on the down arrow to download
- save to an appropriate place
- sync your working directory (in the terminal) with the directory containing mini.gff

### Sorting files by line using `sort`

We can use sort to sort a file's lines into a new order …

**sort usage:**

`sort [options] <file.txt> …`

**!!! Exercise:** Sort the mini.gff file:

```
$ sort mini.gff
```

**!!! Exercise:** Read the sort man pages to figure out how you would …

- sort in reverse order
- sort the capital and lower case letters together
- sort in numerical order.
- Try some of these options

### Sorting files by line using `sort`
