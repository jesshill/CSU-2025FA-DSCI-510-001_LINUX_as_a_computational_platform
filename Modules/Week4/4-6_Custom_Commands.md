# User-specified Custom Commands

Where should I store my scripts?

- It depends on the project.
- For many **small, specific bash scripts**, you can keep them in the same directory as the project they were designed for.
  - This makes a lot of sense for scripts that are designed for one specific task like cleaning up a specific dataset or filtering through some input data.
- For **larger, analytical scripts**, like data analysis that will be published, consider using [git hub]() as a repository for all your scripts.
  - This is a best practice for reproducible data
  - For training: [coding and cookies](https://libguides.colostate.edu/coding-cookies/home)
  - For training: [Github at Boulder](https://calendar.colorado.edu/event/git-github-in-depth-an-rc-short-course) - Friday October 17th, 2025 from 10 am to 12 pm
- What about **generally useful scripts** that you want to use over and over again?
  - For these, we will want to build them into our own **user-specified custom commands**!

### Steps for building custom commands

1. Add the `bin` directory to your `$PATH`
2. Put script in `bin` directory
3. Make script executable
4. Take the `.sh` off the script name

Currently, we can execute our shell script two ways …
1. Within the same directory as the program

```
$ bash script.sh
```

2. From anywhere in our computer using an absolute path

```
$ bash /Users/name/dir1/dir2/script.sh
```

However, once we turn our scripts into **custom commands** we can turn our scripts into programs that more closely resemble real **commands**!

```
$ script
```

Recall our original script `startProject.sh`. Let's try transforming this into a custom command on ALPINE.

1. Add the `bin` directory to your `$PATH`
2. Put script in `bin` directory
3. Make script executable
4. Take the `.sh` off the script name

#### 1. Add the `bin` directory to your `$PATH`

Do you already have a `bin` directory in your projects directory on ALPINE?

- Check it
- Go to `/projects/<user>`
- Use the `ls` to see if there is a directory called `bin`
- Make this directory if you don't have it already

Recall that one of our environmental variables was called PATH:

```
$ echo $PATH
```






