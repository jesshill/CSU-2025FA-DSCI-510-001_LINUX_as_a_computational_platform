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
<img width="410" alt="cp example 2" src="https://github.com/jesshill/CSU-2025FA-DSCI-510-001_LINUX_as_a_computational_platform/blob/main/Images/cp_example.png">
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
