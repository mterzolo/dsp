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

> > pwd (show current working directory path)
> > mkdir <dirname> (create a directory)
> > rm -r <dirname> (remove a directory)
> > touch <filename> (create a file)
> > rm <filename> (delete a file)
> > mv <filename> <newfilename> (rename a file)
> > ls -a (list hidden files)
> > cp <filename> <newpath>
> > cd <path> (change directory)
> > cd .. (move back one directory)
> > vi <filename> (edit file)
> > i (enter edit mode once in vi)
> > esc (exit edit mode once in vi)
> > :wq (save changes and exit vi)
> > :q! (exit vi without saving)

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

> > ls (list files in current directory
> > ls -a (lists all files in directory including hidden files)
> > ls -l (long:lists file permissions, last edit date, who editted, etc.)
> > ls -lh (lists in long format plus readable file size)
> > ls -lah (lists in long format plus hidden files plus readable file size)
> > ls -t (sorts by time and date)
> > ls -Glp (directories are colored blue, in long format, directories have / appended to directories)

---

### Q3.  More List Files in Unix  

Explore these other [ls options](http://www.techonthenet.com/unix/basic/ls.php) and pick 5 of your favorites:

> > ls -c (displays file by their timestamp)
> > ls -R (shows subdirectories)
> > ls -r (shows in reverse order)
> > ls -u (shows with time file was accessed)
> > ls -m (shows as comma seperated list)


---

### Q4.  Xargs   

What does `xargs` do? Give an example of how to use it.

> > xargs extend the functionality of many commands to allow the output of other commands to become the inputs

> > example:

> > create three new directories named dir_1, dir_2, dir_3

> > echo dir_1 dir_2 dir_3 | xargs mkdir
