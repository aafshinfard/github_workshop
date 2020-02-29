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
* [Bonus](#bonus)


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
Got to the github website an create a repository under your account. Then:
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
$ git remote add origin remote "repository-URL"		# Sets the new remote
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
or compare your stage with your local repository using:
```bash
git diff --staged
```

Group Projects
==============


### Branching
Create a new branch an switch to it:
```bash
git checkout -b "branch-name"
```
Make some changes to your file, and push it to your remote repo. Then check your github repository using the website. Where are the new changes?

### Merging (Pull Request)
Use the website and go to the branch you want to merge to `master`. Hit the button `create a pull request`.

If there's no conflict you can simply `merge`, if there's, then you need to resolve conflicts before merging. 

To resolve the conflicts you have two options:
(a) Using the website. Make sure you update your local repos using `pull` afterward.
(b) Using command-line and `git`:

```bash
> git fetch origin	 		# fetch the whole remote
> git checkout "branch-name"		# checkot to your local branch, if you're not
> git rebase origin/master		# Add master changes to your local branch
> git push -f 				# force push your local rebased branch into your remote branch
```

### Contribute to projects owned by others

First fork their repo to your account, clone your fork to your local machine, submit the changes, and then:

Add a remote to the main repo (upstream):
```bash
git remote add upstream "address"	#(https://github.com/afshinfard/github_workshop.git)
git remote -v
```

Update your local repo/branch using the upstream repo/branch:
```bash
git fetch upstream 			# Fetch all the changes in the upstream repo
git checkout "branch-name"		# checkout (switch to) the branch you want to merge
git merge upstream/"branch-name"	# Upates your branch with the upstream repo/branch
```

Push changes to the remote repos/branches:
```bash
git push origin "branch-name"		# push to your own remote repo
git push upstream "branch-name"		# push to upstream remote repo
```

Bonus
==============

### Make a README.md

