# Next steps on ALPINE!

This is all the time we have for this class. You are encouraged to learn more about how to use ALPINE on your own and through future workshops and classes.

Here are recommended next steps to consider:
- Learn to customize your user experience by editing your `.bash_profile` on ALPINE.
- Learn to load already-installed software using **modules**
  - [About modules on ALPINE](https://curc.readthedocs.io/en/latest/compute/modules.html)
- Learn to install software on ALPINE using CONDA
  - [Getting started with CONDA](https://curc.readthedocs.io/en/latest/software/python.html#basic-conda-commands-to-get-you-started)
  - [Upcoming workshop on conda and software install on ALPINE](https://www.colorado.edu/rc/events)
- Learn how to save, synchronize, and version-control your scripts using [GitHub](https://github.com/)
- Learn how to organize large computational projects - DSCI512 - RNA sequencing data analysis


Here is some old content from the SUMMIT days. It may be useful for some users:

<details>
  <summary>Summit - Customizing</summary>

---

In this section, we'll learn how to customize our SUMMIT user experience.

All the files associated with customizing the User experience will go in your home directory. Let's navigate there and inspect its contents …

```
$ cd
$ pwd
$ ls -alh
```

**Question:** Do you see a file called `.bash_profile`?

If YES, go ahead and make a backup copy into a backup directory like so …

```
# If you have a .bash_profile file, do the following...
$ mkdir bash_profile_bkup
$ cp .bash_profile bash_profile_bkup/220915_bash_profile
```

If NO, create the file …

```
# If you do not have a .bash_profile file, do the following...
$ touch .bash_profile
```

The `.bash_profile` file where we will add customized code that will run at the START of EVERY SUMMIT session.

For example, if we want to use our custom sacct and squeue commands every session, we can make aliases of these here.

To open your .bash_profile in an editor, go to **FILE –> Open from Path … –>** Type in `/home/<your-eID@colostate.edu/.bash_profile`

Then, at the bottom of the file, add the following code …

```
#Aliases
alias scheck="squeue -u $USER"
alias sa='sacct -X --format JobID,JobName,AllocCPUS,State,ExitCode,Elapsed,TimeLimit,Submit,Start,End'
```

Save and close.

On the terminal, you can refresh these new conditions using …

```
$ source .bash_profile
```

Now, you can go ANYWHERE on SUMMIT and use `scheck` instead of `squeue -u $USER` and you can use `sa` instead of the long `sacct` command. This will also be **persistent**, as in, it will work every time you log into SUMMIT.

---

</details>

<details>
  <summary>Summit - Installing Software</summary>

---




---

</details>

<details>
  <summary>Summit - Demo</summary>

---




---

</details>
