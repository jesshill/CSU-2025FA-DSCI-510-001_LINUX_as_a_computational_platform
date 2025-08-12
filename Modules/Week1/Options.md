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

For example, the following commands *should* do the same thing … but! on Mac, the double dashes don't work. This is due to some differences between Linux on these operating systems.

```
$ls -a
$ls --all
```

These commands should do the same thing on most distributions …

```
$ls -a -h -l
$ls -ahl
```

### Exercise: Exploring Options

**!!! Exercise**: Let's obtain a dataset to allow us to explore `ls` and its options:

Download the following file by clicking on it. When prompted, save it to your a directory you can navigate to by both your Finder/Explorer AND by the terminal: [chromsizes2.tgz](https://github.com/jesshill/CSU-2025FA-DSCI-510-001_LINUX_as_a_computational_platform/blob/main/Data/chromsizes2.tgz)

Note: this may be a good time to make a directory specifically for this class.

Use the Finder/Explorer, navigate to the location where you downloaded the file.

Double click on the chromsizes2.tgz file to decompress it.

**!!! Quick tip**: If double-clicking on the “tarball” doesn't open it, try copying-and-pasting the file someplace you can access through your terminal. Then, navigate to the file through the terminal, then execute this command line to decompress it.

```
$tar -zxvf chromsizes2.tgz
```

If you need to, move the resulting expanded directory and its contents to a location you can easily manipulate in the terminal.

Open your terminal and navigate (use `cd, pwd, ls`) to the directory chromsizes.

Not working? Dr. Nishimura made a video of this in case it is confusing. [Video link to tutorial of tarball download](https://zoom.us/rec/component-page?eagerLoadZvaPages=sidemenu.billing.plan_management&accessLevel=meeting&action=viewdetailpage&sharelevel=meeting&useWhichPasswd=meeting&requestFrom=pwdCheck&clusterId=aw1&componentName=need-password&meetingId=baghS9zqnq9wa-F1KmP-HQdRBUimkEIk8kUzxBj449faPZDHgFKF91eBQsvQgbyo.O63ixl1U5Lv2ax7D&originRequestUrl=https%3A%2F%2Fzoom.us%2Frec%2Fshare%2F9_N4ArPU2l9LYc_jsRrACo0eI6X8eaa80SQcqPtexEcWyMaB7TbVkWJ7gYbepY9I%3FstartTime%3D1598531909000). Passcode: f$fQf2Lc
