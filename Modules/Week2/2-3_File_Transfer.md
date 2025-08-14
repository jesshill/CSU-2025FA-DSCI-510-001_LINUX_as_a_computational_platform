# File Transfer 

So far, we have learned to copy and move files from one location on your local computer to another location on the same computer. However, we can also copy content from remote computers and this is called transferring files.

There are many different programs to help transfer files (or directories) between computers. Different linux installations have different programs as default. Also, remote servers and repositories are often set up to interact with one or another of these programs. You'll need to experiment to determine which of these options works best on your system.

When we learn software installation later in this course, we will add more of these programs.

Common file transfer programs are:

- sftp
- wget
- curl
- rsync
- scp

### sftp - Secure File Transfer Program

```
ftp <sftp://address/to/ftp/site>

-requires that the host/remote is configured as an sftp site
-interact remotely with the remote computer
-use commands cd, ls, get, bye
```

### wget - World wide web GET

```
wget <http://address/to/file/file.txt>

-must be installed on MacOS systems using Conda or Homebrew
```

### curl - Command line URL

```
curl [options] <sourcefile.txt> curl [–remote-name-all] <http://address/to/file/file.txt>

-can only download one file at a time
```

### rsync - Remote file and directory SYNChronization

```
rsync [options] <source> <target>
rsync [-avzP] http://address/to/dir/> <.>

-a archival, preserves time stamps and permissions
- v verbose, outputs comments to the screen
- z zip, compress to transfer between computers
- P progress, print information on progress to the screen
```

### scp - Secure CoPy

```
scp <sourcefile> <target>
scp <http://address/to/file/file.txt> <.>
```

## Exercise 

We are going to do the following:

1. Download the yeast genome (using rsync or wget)
2. Ensure the files were not corrupted in transit (using md5 sums)
3. Unzip the files (using gunzip)

### Using rsync or wget to download files from UCSC Genome Browser








