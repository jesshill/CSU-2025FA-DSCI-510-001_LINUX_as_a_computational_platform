# Navigating the file system

### Who, What, When, Where commands

In your previous exercise you did the following:

```
$ whoami
$ hostname
$ pwd
$ ls
$ date
$ cal
```

Hopefully, when you typed in these commands, the shell responded more intelligibly than when you typed gibberish. This is because commands are programs that the shell has installed. When you type the command, you are instructing the shell to run a program it recognizes.

```
$ whoami  # WHO am I?
$ hostname  # WHAT computer is this?
$ pwd  # (Path to Working Directory) WHERE on the computer am I?
$ ls  # (List Segments) WHAT are the contents of this directory?
$ date  # WHEN? What is the date and time?
$ cal # WHEN? cute little calendar of this month
```

**!!! Quick tip**: Everything written after a “#” sign is a **comment** or annotation. The shell will not read things written after “#”.

**!!! Quick tip**: A **directory** is just the Linux-y term for “folder”. Just as there are slight terminology differences between MAC and Windows, so too are there differences in Linux.

### Intro to Independent Exercise - Dissecting the path

Let's take a closer look at what spits out when you type the command `$pwd`

When I type this out on my MAC computer, I get something that looks like this:

```
$ pwd 
/Users/jessicahill
```

If you are on a LINUX machine or a Windows, you will probably see something more like this …

```
$ pwd 
/home/jessicahill
```

This notation is called a **path** and it describes the location, or the address, of my working directory within the file structure of a computer system.

When I look in this directory (on a MAC), I see …

```
$ ls
Applications            Dropbox                 master_backup_171220.sh
Backup_logs             Library                 master_backup_bkps
Backup_profiles         Movies                  seqmonk_cache
Creative Cloud Files    Music                   seqmonk_genomes
Desktop                 Pictures                seqmonk_prefs.txt
Documents               Public
Downloads               igv
```
