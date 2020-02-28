Github Workshop
=====================
by Amirhossein, aafshinfard@bcgsc.ca

Contents
========

* [Before the workshop](#before-the-workshop)
* [Introduction](#introduction)
* [Github.com](#Github.com)
* [Basics](#basics)
* [Group projects](#group-projects)
* [Bonus - Extra Tricks](#bonus---extra-tricks)


Before the workshop
==============
* Make sure you have `git` installed on your system. Need a link?

	https://git-scm.com/book/en/v2/Getting-Started-Installing-Git

* Sign up for a github account here: www.github.com
* Setup your account on your system:
    
    Using the username an e-mail address you used to sign-up on github, config the git installed on your system using the following commands (change “username“ and “e-mail“ to yours):
```bash
> git config --global user.name “username”
> git config --global user.email “e-mail”

```
You can double check the config using the following command:
```bash
git config --list
```


Basics
======

##### Create a new repo
Open you terminal or command-line (cmd).
Go to a specific folder/directory (using `dir` or `cd` command)
```bash
> cd /home/my_project/ 		# for linux
> dir /home/my_project/ 	# for windows
```
and use the command below to init a new repository. The name will be the same as the directory's name in which you are running the command.
	
```bash
> git init
```
