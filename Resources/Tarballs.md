# Tarballs

We can compress a directory of files into a single, compressed file using the **tar** command. This greatly reduces the directory size and makes it easy to move a whole directory from computer-to-computer. Sadly, the commands and option for the **tar** command are notoriously hard to memorize:



To compress a directory into a tarball:
tar compression
tar -zcvf <tarball.tgz> <directory_to_compress>
-z - gzip it
-c - compress it
-v - verbose
-f - files

To extract a tarball into an un-compressed directory again:
tar extraction
tar -zxvf <tarball.tgz>
-z - it's gzipped
-x - eXpand it
-v - verbose
-f - files
