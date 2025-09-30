---
title: 'OverTheWire: Bandit Level 0 to Level 1'
description: "The bandit wargames are aimed at absolute beginners. It will teach the basics needed to be able to play other wargames."
date: 2025-09-27 23:17 +0100
categories: [Security, OverTheWire]
tags: [overthewire, bandit, ctf, security, linux]
media_subpath: /assets/
---

## Level Goal

> The password for the next level is stored in a file called **readme** located in the home directory. Use this password to log into bandit1 using SSH. Whenever you find a password for a level, use SSH (on port 2220) to log into that level and continue the game.

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

**Note:** All commands aren't always needed to complete a level

## Solution

Let's view the files that are present in the current working directory using the `ls` command

```bash
bandit0@bandit:~$ ls
readme
```

We see the file named `readme` which contains the password to the next level. Let's view the contents using the `cat` command

```bash
bandit0@bandit:~$ cat readme
Congratulations on your first steps into the bandit game!!
Please make sure you have read the rules at https://overthewire.org/rules/
If you are following a course, workshop, walkthrough or other educational activity,
please inform the instructor about the rules as well and encourage them to
contribute to the OverTheWire community so we can keep these games free!

The password you are looking for is: ZjLjTmM6FvvyRnrb2rfNWOZOTa6ip5If
```

Bingo! We found the password for the next level. Use the password found above to login as bandit1 and move on.

```bash
ssh bandit1@bandit.labs.overthewire.org -p 2220
This is an OverTheWire game server. More information on http://www.overthewire.org/wargames

backend: gibson-0
bandit0@bandit.labs.overthewire.org's password: ZjLjTmM6FvvyRnrb2rfNWOZOTa6ip5If
```
