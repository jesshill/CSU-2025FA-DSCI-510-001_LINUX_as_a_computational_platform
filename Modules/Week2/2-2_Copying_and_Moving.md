# Copying and Moving

### Copying files and directories with `cp`

The `cp` (CoPy) command is quite flexible. There are a few ways it can be used to copy a file.

#### Duplicating a file and giving it a new name

<p align="center">
<img width="410" alt="cp example" src="https://github.com/jesshill/CSU-2025FA-DSCI-510-001_LINUX_as_a_computational_platform/blob/main/Images/cp_example.png">
</p>

This can be used to copy the contents of a file (the source file) into a new file (the target file) with a new name:

`cp <source_file.txt> <target_file.txt>`

**!!! Exercise:** Make a backup copy of a file. Navigate into your folder `chromsizess`. Make a copy of `hgs1_chrom_sizes.txt` called `hs1_chrom_sizes_backup.txt`.

```
$ cp hs1_chrom_sizes.txt hs1_chrom_sizes_backup.txt
$ ls
$ more hs1_chrom_sizes.txt #peek in the file
$ more hs1_chrom_sizes_backup.txt #peek in the backup
```

You can think of this as basically shorthand for …

```
$ cp ./file1.txt ./file2.txt
```

You can expand the source and target names to be absolute paths, too!

```
$ cp /users/jtkirk/captainslog_2713.txt /users/jtkirk/captainslog_2714.txt
```

#### Duplicating a file into a directory

Once you make the connection that names, absolute paths, or relative paths can substitute in for <source_file.txt> or <target_file.txt>, you can see how you can place the copied file in some other directory, or pull a copy of a file from a source directory into your working directory.

<p align="center">
<img width="410" alt="cp example 2" src="https://github.com/jesshill/CSU-2025FA-DSCI-510-001_LINUX_as_a_computational_platform/blob/main/Images/cp_example2.png">
</p>

Duplicating a file into a directory and renaming it: `cp <source_file.txt> <target/path/targetname.txt>`

OR

Duplicating a file from another directory into the current directory and renaming it: `cp <target/path/sourcename.txt> <./targetname.txt>`

**!!! Exercise:** Navigate into your folder `chromSizes`. Make a directory called `backups`. Place a copy of `mm10_chrom_sizes.txt` into `backups` and name it `mm10_chrom_sizes_backups.txt`.

```
$ mkdir backups
$ cp mm10_chrom_sizes.txt backups/mm10_chrom_sizes_backup.txt
$ ls 
$ ls backups
```

**!!! Quick Tip:** Absolute paths as well as relative paths can be used as the source and target in `cp`.

If you want to duplicate a file into a sub-directory, you don't need to change the name. To keep the name the same ...

`cp <source_file.txt> <target_directory>`

**!!! Exercise:** Try it out

```
$ cp dm6_chrom_sizes.txt backups
$ ls 
$ ls backups
```

A list of files can also be copied in this way: 

`cp <source_file.txt> … <target_directory>`

– where “…” means you can keep adding additional `source_files.txt`, as many as you have.

#### Duplicating a directory and its contents

Directories that contain files can also be duplicated using `cp`. Just add the option `-R`.  

```
$ cp -R backups copy_of_backups
$ ls 
$ ls backups
$ ls copy_of_backups
```

**!!! Independent Exercise:** I like to stay organized by adding notes to myself within project directories. I call these README or ABOUT files.

1. Within your directory called `chromSizes` create a directory called `NOTES`.
2. Copy the file `README_download.txt` into the `NOTES` directory.

**!!! Independent Exercise:** Add an XX genome.

1. Copy `hs1_chrom_sizes.txt` to a new file called `hs1_chrom_sizes_XX.txt`.
2. Using **nano**, go into `hs1_chrom_sizes_XX.txt` and delete the entry for the Y chromosome. **Hint:** you can't add a cursor anywhere you want. You'll need to navigate with arrow keys.

### Moving files and directories with `mv`

Once you know `cp`, `mv` is pretty much the same thing with one exception. The source file will **disappear** once the operation is complete. This ends up **renaming** your file if you are working within the same directory. It acts like **cut-and-paste** instead of a copy-and-paste if you're moving between directories.

<p align="center">
<img width="410" alt="mv example" src="https://github.com/jesshill/CSU-2025FA-DSCI-510-001_LINUX_as_a_computational_platform/blob/main/Images/mv_example.png">
</p>

Again, `mv` tries to operate in slightly different ways depending on the types of arguments you give it:

| | |
|-------|------|
| **mv** <source_file.txt> <target_file.txt> | Rename source_file.txt to be called target_file.txt |
| **mv** <source_file.txt> <dir/target_file.txt> | Move source_file.txt into dir and rename it target_file.txt |
| **mv** <source_file.txt> ... <dir> | Move source_file.txt(s) into dir and keep the names the same |

**!!! Independent Exercise:** On your own, practice using the `mv` command to rename `danRer11_chrom_sizes.txt` to `dr11_chrom_sizes.txt`.

Continue on to [File Transfer](2-3_File_Transfer.md)
