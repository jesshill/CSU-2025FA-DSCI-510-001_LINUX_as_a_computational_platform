# Control Flow Practice

### Todays objectives: 

<details>
  <summary>Click to expand/collapse</summary>

- **Vocabulary**
  - High-Performance Computing (HPC)
  - Supercomputer
  - Compute Cluster
  - Nodes
    - Login nodes
    - Compile nodes
    - Compute nodes
  - Custom Commands
  - `$PATH` – your path
  - `.bash_profile` file

- **Things you should know how to do after this class**
  - Know how to log onto ALPINE
  - Understand the benefits of using a supercomputer
  - Have a rudimentary understanding of Nodes on ALPINE
    - Understand that you shouldn’t do large jobs on the login node
  - Have a rudimentary understanding of the File Structure system on ALPINE
  - Learn about the $PATH which is an environmental variable.
    - Be aware of the concept of adding directories to your $PATH
  - Have a cursory knowledge about how .bash_profile files can be used to customize the user experience
  - Learn about the main steps in creating a custom command

- **Commands covered**
  - `acompile`
  - `curc-quota`
  - `module avail`

</details>


### Reminder: 

HW 5 and 6 are due by 11:59 pm tonight!

### Test your understanding - take this quiz!

[Quiz 7](https://forms.gle/Ck9tM4q91brAZ8457)

### Exercises for practice

**!!! Exercise 1** - Use a `for` loop structure to produce the following output:

```
10
9
8
7
6
5
4
3
2
1
blast off!
```

**!!! Exercise 2** - Use a `while` loop structure to produce the same output above.

**!!! BONUS - Exercise 3** - `measureDiskSpace.sh` - Add to the `measureDiskSpace.sh` script so that instead of printing content to the screen, it now redirects all its output to a file called `diskUsage_output.txt`

**!!! BONUS - Exercise 4** - `measureDiskSpace2.sh` - create a conditional inside your loop that gives a different message if the file is empty like so …

```
$ bash measureDiskSpace.sh *.txt
The file listOfHouses.txt takes up 4.0K of disk space
The file text1.txt takes up 4.0K of disk space
The file text2.txt takes up 4.0K of disk space
WARNING! text3.txt is empty!!!
The file text4.txt takes up 4.0K of disk space
```

Answer for Exercise 4

<details>
  <summary>Answer</summary>

```
#!/usr/bin/env bash
 
#Note: This answer contains a conditional within a for loop...
 
# For loop
   # If
   # Else
 
 
# Capture arguments
myarguments=$@
 
#Loop over each argument
 
for myfile in ${myarguments[@]}
do
	# Calculate the disk usage for a file
	# Remove the file name from the output using cut
	# Remove white space from the output using sed
	myspace=$( du -h $myfile | cut -f 1 | sed 's/ //g' )
 
	# Check if $myspace is 0B
	if [ $myspace == "0B" ]
	then
		# If file is empty, say so
		echo "File is empty!"
	else
		# If file is not empty, print the sentence including the file name and the disk usage:
		echo -e "The file $myfile takes up $myspace of disk space"
	fi
 
done
```

</details>

