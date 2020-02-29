Github Workshop
=====================
by Amirhossein, aafshinfard@bcgsc.ca

First download this repository and take a look at the powerpoint slides. Then start following the steps below.

After all, I invite you to fork my repo into your account, add your name to the `group.txt` file, push that into your account, and open a pull request so I add your edits to my repo. Don't worry, you will soon learn what all the jargons in the previous sentence mean :).

Contents
========

* [Before the workshop](#before-the-workshop)
* [Introduction](#introduction)
* [Github.com](#Github.com)
* [Basics](#basics)
* [Group projects](#group-projects)
* [Forking](#forking)
* [Bonus](#bonus)


Before the workshop
==============
* Make sure you have `git` installed on your system. Need a link?

	https://git-scm.com/book/en/v2/Getting-Started-Installing-Git

* Sign up for a github account here: www.github.com
* Setup your account on your system:
    
    Using the username an e-mail address you used to sign-up on github, config the git installed on your system using the following commands (change “username“ and “e-mail“ to yours):
```bash
$ git config --global user.name “username”
$ git config --global user.email “e-mail”

```
You can double check the config using the following command:
```bash
$ git config --list
```
or learn more about configuring your repository using:
```bash
$ git config --help
```

* We will be mostly using `terminal/command-line` to work with git and github. If you are not familiar with commands and working with terminal, you can take a look at this [introduction for beginners](https://ubuntu.com/tutorials/command-line-for-beginners#1-overview). If you are using windows, here it is a [list of commands](https://www.thomas-krenn.com/en/wiki/Cmd_commands_under_Windows).



Basics
======


Open you terminal or command-line (cmd).
### Go to a specific folder/directory
```bash
$ cd /home/my_project/ 		# change the directory. (linux and windows (and mac?))
```

### Create a new repository (local and online):

You have 2 options to create a new repository. You can start the remote repository and clone (download) it. Or you can create your local repository and then upload it to your github account. The first option is much easier and involves fewer steps.

* Option 1:
Got to the github website an create a repository under your account. Then:
```bash
$ git clone "Repository URL" 			#initialize a repo
```
After you clone the repo, make sure you enter the new directory (folder)
or
* Option 2:
make a directoy:
```bash
$ mkdir "directory-name"	# make a directory. we will make this directory a reposiory next
```
Enter the directory and make it a git repository:
```bash
$ cd "directory-name"		#enter the directory 
$ git init 			#initialize a repo
```
Then you need to create a repository on github with the same name, and then:
```bash
$ git remote add origin remote "repository-URL"		# Sets the new remote
$ git remote -v						# Verifies the new remote URL
```

### Start building up your project

```bash
$ git add				#add files to the stage (from working irectory to staging area)
$ git commit -m "commit-message"	#add a checkpoint to your local repo (from staging area to local repo)
$ git push origin master		#push changes to the remote repo (from local repo to remote repo)
$ git pull origin master		#pull changes from the remote repo (from remote repo to local repo)
```
you can check the satus of your reposity using:
```bash
$ git status			#check the status of your repo
```
or compare your stage with your local repository using:
```bash
$ git diff --staged
```

Group Projects
==============


### Branching
Create a new branch an switch to it:
```bash
$ git checkout -b "branch-name"
```
Make some changes to your file, and push it to your remote repo. Then check your github repository using the website. Where are the new changes?

### Merging (Pull Request)
Use the website and go to the branch you want to merge to `master`. Hit the button `create a pull request`.

If there's no conflict you can simply `merge`, if there's, then you need to resolve conflicts before merging. 

To resolve the conflicts you have two options:
(a) Using the website. Make sure you update your local repos using `pull` afterward.
(b) Using command-line and `git`:

```bash
$ git fetch origin	 		# fetch the whole remote
$ git checkout "branch-name"		# checkot to your local branch, if you're not
$ git rebase origin/master		# Add master changes to your local branch
$ git push -f 				# force push your local rebased branch into your remote branch
```

### Forking
Forking is (more or less) like making a new branch, but not under the main repo, but in your own account. This way you can "branch" projects that are owned by other accounts. You may make some changes and collaborate with the owner to merge your edits to their repo. Here is how:

First fork their repo to your account, clone your fork to your local machine, submit the changes, and then:

Add a remote to the main repo (upstream):
```bash
$ git remote add upstream "address"	#(https://github.com/afshinfard/github_workshop.git)
$ git remote -v
```

Update your local repo/branch using the upstream repo/branch:
```bash
$ git fetch upstream 			# Fetch all the changes in the upstream repo
$ git checkout "branch-name"		# checkout (switch to) the branch you want to merge
$ git merge upstream/"branch-name"	# Upates your branch with the upstream repo/branch
```

Push changes to the remote repos/branches:
```bash
$ git push origin "branch-name"			# push to your own remote repo
$ git push upstream "branch-name"		# push to upstream remote repo
```
The last step may or may not work based on your permissions. If it did not, you can go to your forked repo uner your account, and manually open a pull request from there. When your visitng the main page of the repo, there's a `new pull request` button.

Excercise
==============
Using the instructions in the [previous sections](forking), fork this repository into your account, fetch/pull it into your machine, add your nme to `group.txt`, push it into your forked repo, and open a pull request so I merge your edits to my account.

Bonus
==============

### Make a README.md
There is a `README.md` file among the files in this repo. Fork this project into your account and open the `READMME.md` file. By comparing what is in the file, an what you see here, you can start learning how to make/format a readme file for your repository. The name should be exatclty the same: "README.md" and github will automatically produce this readme as a guide to your repo. People can read this an learn about your repo/project.



