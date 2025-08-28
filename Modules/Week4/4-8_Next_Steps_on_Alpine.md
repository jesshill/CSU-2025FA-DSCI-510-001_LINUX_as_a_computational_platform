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

### Loading pre-installed software with modules

The SUMMIT support staff has already installed some software on SUMMIT that you can load. To browse what is pre-installed,

```
$ module avail
```

You may have already noticed that when you login you are prompted to try this. We won't be going through the modules here, but you can learn more about them on the [Module User Guide](https://curc.readthedocs.io/en/latest/compute/modules.html)

To load a listed module,

```
$ module load <nameofmodule>
```

### Loading pre-installed software with modules

Scientific software is created by the open-source community of researchers like you and me.

<p align="center">
<img width="410" alt="open source" src="https://github.com/jesshill/CSU-2025FA-DSCI-510-001_LINUX_as_a_computational_platform/blob/main/Images/opensource_img.png">
</p>

When the software is being actively supported, there may be binaries (ready-to-run programs) available to download. If not, the **source code** of the software will need to be downloaded, compiled, and installed. For several decades, these tasks took up a large amount of a person's time and energy while wearing down their very sanity.

However, **software installers** have really changed the game. There are now several software installers available for different systems:

- Homebrew - Mac OS
- apt-get - Ubuntu, other linux
- conda - all systems

Homebrew and apt-get require administrative access on your own computer, whereas you can use conda to install on systems where you are not an administrator, such as on SUMMIT.

Today, we will walk you through how to install software on SUMMIT using **conda**. What is conda?

<p align="center">
<img width="410" alt="conda" src="https://github.com/jesshill/CSU-2025FA-DSCI-510-001_LINUX_as_a_computational_platform/blob/main/Images/conda_logo.png">
</p>

#### conda

- conda is an open-source package management system
- conda maintains a repository of open-source software code called Anaconda
  - We will use the computational biology specific version called bioconda
- conda assists in downloading, compiling, and installing software
- when a piece of software is downloaded, all dependent packages will also be obtained
- conda helps users create different environments where software collections can be collected and curated.

**packages** - small units of software

**environment** - a virtual space where a user can contain a collection of installed software. Users can have environments associated with different research projects.

#### what is up with the name?

- python, anaconda, sense a theme? hint - there is also a boa

#### A little bit about the scope of this project

<p align="center">
<img width="410" alt="conda" src="https://github.com/jesshill/CSU-2025FA-DSCI-510-001_LINUX_as_a_computational_platform/blob/main/Images/conda_logo.png">
</p>

### Configuring conda with `.condarc`




---

</details>

<details>
  <summary>Summit - Demo</summary>

---




---

</details>
