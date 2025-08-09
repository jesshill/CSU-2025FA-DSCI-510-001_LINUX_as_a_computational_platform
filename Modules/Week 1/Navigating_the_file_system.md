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
Colostate		Library			Pictures
Desktop			Movies			Public
Documents		Music
Downloads		OneDrive - Colostate
```

These are the items I have inside the working directory. This directory corresponds to the same directory I can locate in my MAC Finder.

PC people, you will probably see nothing …

```
$ ls
$
```

The home folder on UBUNTU for Windows is in a really weird, hidden place.

### Independent exercises for Mac users

**!!! Exercise**: Open your Finder or Explorer and navigate to the same directory you're in on the terminal. Double check that the contents are the same. Check that the path is similar.

**!!! Mac tip**: If you don't see your path in the Finder window, pull down the **View** menu and select **Show Path Bar**.

The directory you find yourself in when you first open up your terminal is called you **home** directory. This is a special place where the shell starts up by default.

### Independent exercises for Windows users

**!!! Exercise**: Try to find where your home directory is located on your computer. This is pretty challenging, but here we go …

- In your home directory, create a file called 240820_test.txt like so …

```
$ touch 240820_test.txt
```

- Switch over to your File Explorer and search for the file 240820_test.txt on “this PC”.
- ...
Once your File Explorer has located your test file, navigate to that place.
Open a NEW File Explorer.
Go to “View”
Click on “File Name Extensions” to ensure that file name extensions are shown.
Click on “Hidden Items” to ensure that hidden items are shown.
Then click on “This PC” or “C:” and follow the train of folders down and down until you locate the directory where your test file was stored. This is your home directory.
Create a shortcut to this home directory on your desktop so you always know where to find it.



