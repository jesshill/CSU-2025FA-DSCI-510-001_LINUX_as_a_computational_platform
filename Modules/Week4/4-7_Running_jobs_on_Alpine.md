# Running Jobs on Alpine

Today we're going to learn how to run jobs on ALPINE.

For small jobs, we can run them on the command line as we would on our own terminal. Let's try this together.

**!!! Exercise together**

- Navigate to your scratch space on ALPINE and start a new project directory called DSCI510_demo

```
cd /scratch/alpine/$USER
$ pwd # make sure you are where you think you are
$ mkdir DSCI510_demo
$ cd DSCI510_demo
```

- Go back to the onDemand Dashboard and go to this same location in the **Files** window.

...

- Return to the terminal, and start a job called `helloWorld.sh`

```
touch helloWorld.sh
```

- Now, switch back to the file open helloWorld.sh by pulling down the horizontal dot menu and selecting **Edit:**

...

- Write the following script:

```
#!/bin/usr/env bash
 
echo "Hello world!"
```

- Execute the script on the command line like so:

```
$ bash helloWorld.sh
```

Well, that sure seemed familiar. We can do this for simple tasks and scripts - things like copying files, moving files, and scripts that use very little time and hardware.

Once our jobs take longer to execute or require more processing power (cores), then we need to get in line by using the **job sharing utility** called **SLURM**.
