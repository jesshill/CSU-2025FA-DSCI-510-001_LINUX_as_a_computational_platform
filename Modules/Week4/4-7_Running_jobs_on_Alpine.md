# Running Jobs on Alpine

Today we're going to learn how to run jobs on ALPINE.

For small jobs, we can run them on the command line as we would on our own terminal. Let's try this together.

**!!! Exercise together**

Navigate to your scratch space on ALPINE and start a new project directory called DSCI510_demo

```
cd /scratch/alpine/$USER
$ pwd # make sure you are where you think you are
$ mkdir DSCI510_demo
$ cd DSCI510_demo
```

Go back to the onDemand Dashboard and go to this same location in the **Files** window.

<p align="center">
<img width="410" alt="files menue" src="https://github.com/jesshill/CSU-2025FA-DSCI-510-001_LINUX_as_a_computational_platform/blob/main/Images/fileNavigation.png">
</p>

Return to the terminal, and start a job called `helloWorld.sh`

```
touch helloWorld.sh
```
