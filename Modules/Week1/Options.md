# Options

Up to this point, we have used commands with and without arguments. In addition to this, we can execute commands with **options**. Options are bells and whistles we can append to our commands to customize the way the shell interprets the commands.

Here are a few options for the command ls courtesy of [The Linux Command Line](https://linuxcommand.org/tlcl.php):

<p align="center">
<img width="410" alt="options" src="https://github.com/jesshill/CSU-2025FA-DSCI-510-001_LINUX_as_a_computational_platform/blob/main/Images/options.png">
</p>

Options are added after the command itself but before any arguments.

**command** [options] [arguments]
**command** [options] <arguments>

[] – optional. The command will work with or without these.
<> – required. The command requires these arguments.

Short options take one dash. Long options take two dashes.

Further, short options can often be lumped together.

For example, the following commands *should* do the same thing… but! on Mac, the double dashes don't work. This is due to some differences between Linux on these operating systems.

```
$ls -a
$ls --all
```

These commands should do the same thing on most distributions …

```
$ls -a -h -l
$ls -ahl
```
