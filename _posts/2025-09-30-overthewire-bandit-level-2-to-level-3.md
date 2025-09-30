---
title: 'OverTheWire: Bandit Level 2 to Level 3'
date: 2025-09-30 06:35 +0100
description: "The bandit wargames are aimed at absolute beginners. It will teach the basics needed to be able to play other wargames."
categories: [Security, OverTheWire]
tags: [overthewire, bandit, ctf, security, linux]
media_subpath: /assets/
---

## Level Goal

> The password for the next level is stored in a file called `-- spaces in this filename--` located in the home directory

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

[Google Search for "spaces in filename"](https://www.google.com/search?q=spaces+in+filename){: target="_blank"}

## Solution

View the files that are present in the current working directory using `ls`

```bash
bandit2@bandit:~$ ls
--spaces in this filename--
```

Similar to the previous level we can view the contents of `--spaces in this filename--` using the `cat` command along with redirection.

**Note:** We can escape spaces in a filename using `\` or by enclosing the filename in `".."` (quotes) 
**Note:** Filenames can also be auto-completed using the `Tab` key

```bash
bandit2@bandit:~$ cat < --spaces\ in\ this\ filename--
MNk8KNH3Usiio41PRUEoDFPqfxLPlSmx

bandit2@bandit:~$ cat < "--spaces in this filename--"
MNk8KNH3Usiio41PRUEoDFPqfxLPlSmx
```

There is the password to the next level. Lets end the current session and use the password for bandit3 and move on.

```bash
~ ❯ ssh bandit3@bandit.labs.overthewire.org -p 2220
This is an OverTheWire game server. More information on http://www.overthewire.org/wargames

backend: gibson-0
bandit3@bandit.labs.overthewire.org's password: MNk8KNH3Usiio41PRUEoDFPqfxLPlSmx
```
