---
title: "OverTheWire: Bandit Level 0"
description: "The bandit wargames are aimed at absolute beginners. It will teach the basics needed to be able to play other wargames."
date: 2025-09-27 05:46 +0100
categories: [Security, OverTheWire]
tags: [overthewire, bandit, ctf, security, linux]
media_subpath: /assets/
---

## Level Goal

> The goal of this level is for you to log into the game using SSH. The host to which you need to connect is **bandit.labs.overthewire.org**, on port 2220. The username is **bandit0** and the password is **bandit0**. Once logged in, go to the Level 1 page to find out how to beat Level 1.

## Commands you may need to solve this level

> ssh

```
> whatis ssh
ssh (1) - OpenSSH remote login client
```

## Helpful reading material

[Secure Shell (SSH) on Wikipedia](https://en.wikipedia.org/wiki/Secure_Shell){: target="_blank"}

[How to use SSH with a non-standard port on It's FOSS](https://itsfoss.com/ssh-to-port/){: target="_blank"}

[How to use SSH with ssh-keys on wikiHow](https://www.wikihow.com/Use-SSH){: target="_blank"}

## Useful information

* Username: `bandit0`
* Hostname: `bandit.labs.overthewire.org`
* Port: `2220`
* Password: `bandit0`

## Solution

Open a terminal

To login to Level 0 we need to use the SSH command

SSH command: `ssh <username>@<hostname> -p <port>`

**Note:** If asked to accept any fingerprint type "yes" and press Enter

When asked for the password type **bandit0** and press Enter

```bash
> ssh bandit0@bandit.labs.overthewire.org -p 2220
This is a OverTheWire game server. More information on http://www.overthewire.org/wargames

backend: gibson-0
bandit0@bandit.labs.overthewire.org's password:
```

If the login was successful you will see the following:

![Logged into Level 0](/img/bandit/level-0-login.png){: width="360"}

To quit the SSH session type `exit` or use the keyboard shortcut `Ctrl + D`
