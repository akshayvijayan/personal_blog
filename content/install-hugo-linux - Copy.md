---
title: "How to install Hugo on linux"
date: "2020-06-14"
description: "Complete steps to install Hugo on Linux"
tags: [hugo, linux]
categories: [Technology]
---

Hugo is a powerful platform which simple to use. Using Hugo we can design portfolios, blogs etc. Here are the steps that you need to complete to setup a hugo website. I have faced issues while installing Hugo on my LXLE linux 18.04.3 and that is the reason why I have written an article on how to do it properly.
<!--more-->

<script data-ad-client="ca-pub-9770552734505179" async src="https://pagead2.googlesyndication.com/pagead/js/adsbygoogle.js"></script>

<script data-ad-client="ca-pub-9770552734505179" async src="https://pagead2.googlesyndication.com/pagead/js/adsbygoogle.js"></script>

In command prompt type
```
$sudo apt install linuxbrew-wrapper 
```
Linubrew is a package manager which is now known as Homebrew. For more details check [documentation](https://docs.brew.sh/Homebrew-on-Linux).
```
$sudo apt-get install build-essential
```
The build-essential includes GCC/g++ compilers and libraries and some other utilities.

It is recommended to install brew install GCC dependencies
```
$brew install gcc
```

Add Linuxbrew to your ~/.bash_profile by running
```
$echo 'export PATH="/home/linuxbrew/.linuxbrew/bin:$PATH"' >>~/.bash_profile
$echo 'export MANPATH="/home/linuxbrew/.linuxbrew/share/man:$MANPATH"' >>~/.bash_profile
$echo 'export INFOPATH="/home/linuxbrew/.linuxbrew/share/info:$INFOPATH"' >>~/.bash_profile
```


Now we can install hugo using brew. 
```
$brew install hugo   
```
The above installation may take sometime. Make sure you have proper internet connectivity. Slow internet may result in instalation failure.


<details>
  <summary>Errors may occur, if the internet connectivity is slow.</summary>
remote: Enumerating objects: 353411, done. 
error: RPC failed; curl 56 GnuTLS recv error (-54): Error in the pull function.
fatal: The remote end hung up unexpectedly
fatal: early EOF
fatal: index-pack failed
Failed during: git fetch origin master:refs/remotes/origin/master -n
</details>


If hugo installation is completed, we can start creating new site.
```
$hugo new site blog
```
It will create a hugo site under the folder blog.


Now add theme & contents!!!

(Themes can be downloaded from https://themes.gohugo.io/)

If you face any issue during installation, please comment the details in the below section.



