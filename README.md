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
or learn more about configuring your repository using:
```bash
git config --help
```

* We will be mostly using `terminal/command-line` to work with git and github. If you are not familiar with commands and working with terminal, you can take a look at this [introduction for beginners](https://ubuntu.com/tutorials/command-line-for-beginners#1-overview). If you are using windows, here it is a [list of commands](https://www.thomas-krenn.com/en/wiki/Cmd_commands_under_Windows).



Basics
======


Open you terminal or command-line (cmd).
### Go to a specific folder/directory
```bash
> cd /home/my_project/ 		# change the directory. (linux and windows (and mac?))
```

### Create a new repository (local and online):

You have 2 options to create a new repository. You can start the remote repository and clone (download) it. Or you can create your local repository and then upload it to your github account. The first option is much easier and involves fewer steps.

* Option 1:
```bash
> git clone "Repository URL" 			#initialize a repo
```
or
* Option 2:
```bash
> git init 			#initialize a repo
```
Then you need to create a repository on github with the same name, and then:
```bash
$ git remote add origin remote repository URL		# Sets the new remote
$ git remote -v						# Verifies the new remote URL
```

### Start building up your project

```bash
> git add				#add files to the stage (from working irectory to staging area)
> git commit -m "commit-message"	#add a checkpoint to your local repo (from staging area to local repo)
> git push origin master		#push changes to the remote repo (from local repo to remote repo)
> git pull origin master		#pull changes from the remote repo (from remote repo to local repo)
```
you can check the satus of your reposity using:
```bash
> git status			#check the status of your repo
```




