---
layout: post
title: 'OverTheWire: Bandit Level 1 to Level 2'
date: 2025-09-27 23:20 +0100
description: "The bandit wargames are aimed at absolute beginners. It will teach the basics needed to be able to play other wargames."
categories: [Security, OverTheWire]
tags: [overthewire, bandit, ctf, security, linux]
media_subpath: /assets/
---

## Level Goal

> The password for the next level is stored in a file called **-** located in the home directory

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

## Helpful reading material

[Google Search for "dashed filename"](https://www.google.com/search?q=dashed+filename){: target="_blank"}

[Advanced Bash-scripting Guide - Chapter 3 - Special Characters](https://linux.die.net/abs-guide/special-chars.html){: target="_blank"}

## Solution

Let's view the files present in the current working directory using the `ls` command

```bash
bandit1@bandit:~$ ls
-
```

We see the file that contains the password named `-`, view the contents using the `cat` command

**Note:** Using the filename directly as in the previous level will not work as `-` is a special character on Linux that is used to denote Standard Input / Standard Output (STDIN / STDOUT). We need to use redirection or the absolute path to access it.

```bash
bandit1@bandit:~$ cat < -
263JGJPfgU6LtdEvgfWU1XP5yac29mFx

bandit1@bandit:~$ cat ./-
263JGJPfgU6LtdEvgfWU1XP5yac29mFx
```

There we see the password for the next level!
Lets exit the current session by typing `exit` or using `Ctrl + D`

Use the password found and access the next level using bandit2

```bash
ssh bandit2@bandit.labs.overthewire.org -p 2220
This is an OverTheWire game server. More information on http://www.overthewire.org/wargames

backend: gibson-0
bandit2@bandit.labs.overthewire.org's password: 263JGJPfgU6LtdEvgfWU1XP5yac29mFx
```
