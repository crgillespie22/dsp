# Learn command line

Please follow and complete the free online [Bash Scripting Tutorial](https://ryanstutorials.net/bash-scripting-tutorial/) or [Codecademy's Learn the Command Line](https://www.codecademy.com/learn/learn-the-command-line). These are helpful tutorials. You should be able to go through these in a couple of hours.

**Note:** Bash is not installed on a PC. Rather, PC users must install Cygwin. Once Cygwin has been installed, the command line interface witll _emulate_ bash. You can find all information regarding Cygwin [here](https://www.cygwin.com/).

---

### Q1.  Cheat Sheet of Commands  

Here's a list of items with which you should be familiar:  
* show current working directory path
* creating a directory
* deleting a directory
* creating a file using `touch` command
* deleting a file
* renaming a file
* listing hidden files
* copying a file from one directory to another

Make a cheat sheet for yourself: a list of at least **ten** commands and what they do.  (Use the 8 items above and add a couple of your own.)  

> > * pwd - print working (current) directory
    * mkdir - create a directory
    * rmdir - remove a directory
    * touch - create a file that does not yet exist
    * rm <file> - delete a file
    * mv - use same source and destination, but with different name to rename a file
    * ls -a - shows hidden files
    * cp <source> <destination>
    * mv - move a directory without having to copy recursively
    * -r - recursive, allows copying and deletion of non-empty files

---

### Q2.  List Files in Unix   

What do the following commands do:  
`ls`  
`ls -a`  
`ls -l`  
`ls -lh`  
`ls -lah`  
`ls -t`  
`ls -Glp`  

> > ls - provides a list of directory contents
    ls -a - does the same as ls, but displays hidden files
    ls -l - displays contents in 'long format'
    ls -lh - uses unit suffixes for directory content to minimize output
    ls -lah - diplays all contents, including hidden ones in 'long format' with unit suffixes
    ls -t - sort contents by time
    ls -Glp - colorize ouput in long form, and include a '/' after a file that is a directory

---

### Q3.  More List Files in Unix  

Explore these other [ls options](http://www.techonthenet.com/unix/basic/ls.php) and pick 5 of your favorites:

> > -r - reverse the sort order
    -S - sort files by size
    -c - sort by last time a file was modified
    -f - unsorted list
    -1 - forces output to be one entry per line
    

---

### Q4.  Xargs   

What does `xargs` do? Give an example of how to use it.

> > xargs run a command for every item in a list. You can run xargs to modify a file extension that has been mistyped (e.g., uppercase vs lowercase).

 

