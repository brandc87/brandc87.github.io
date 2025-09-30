---
title: 'OverTheWire: Bandit Level 3 to Level 4'
date: 2025-09-30 06:35 +0100
description: "The bandit wargames are aimed at absolute beginners. It will teach the basics needed to be able to play other wargames."
categories: [Security, OverTheWire]
tags: [overthewire, bandit, ctf, security, linux]
media_subpath: /assets/
---

## Level Goal

> The password for the next level is stored in a hidden file in the **inhere** directory

## Commands you may need to solve this level

> ls, cd, cat, file, du, find

```
whatis ls
ls (1)               - list directory contents

whatis cd
cd (1)               - change working directory

whatis cat
cat (1)              - concatenate files and print on the standard output

whatis file
file (1)             - determine file type

whatis du
du (1)               - estimate file space usage

whatis find
find (1)             - search for files in a directory hierarchy
```

## Solution

Let's view the files present in the current working directory using `ls`

```bash
bandit3@bandit:~$ ls
inhere
```

Now move into the `inhere/` directory with the `cd` command

```bash
bandit3@bandit:~$ cd inhere/
```

View the files in the directory using the `ls` command, as the file is hidden we need to use the `-a` flag to view hidden files

```bash
bandit3@bandit:~/inhere$ ls -a
.  ..  ...Hiding-From-You
```

Now we can view the contents of `...Hiding-From-You` using the `cat` command

```bash
bandit3@bandit:~/inhere$ cat ...Hiding-From-You
2WmrDFRmJIq3IPxneAaMGhap0pFhF3NJ
```

There is the password to level 4! Exit the current session and use the password for bandit4 to move on

```bash
~ ❯ ssh bandit4@bandit.labs.overthewire.org -p 2220
This is an OverTheWire game server. More information on http://www.overthewire.org/wargames

backend: gibson-0
bandit4@bandit.labs.overthewire.org's password: 2WmrDFRmJIq3IPxneAaMGhap0pFhF3NJ
```
