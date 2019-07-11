# Tips on Git
Tips on Git for Linux.

## Config file
Stores name, e-mail, default program for text files, etc.

### First-Time setup, edit config file:
https://git-scm.com/book/en/v2/Getting-Started-First-Time-Git-Setup

### Check configuration settings
```git
$ git config --list
```

## Getting a Git Repository
This action is done only once, to set up Git inside a directory. If one wants to resume the work, it is not necessary to run any command. It is only necessary to `cd` to the directory of the desired project.

### Initializing a Repository in an Existing Directory
```git
$ cd /home/user/my_project
$ git init
```

### Cloning an Existing Repository
```git
$ git clone https://github.com/repository my-local-repository
```

## Recording Changes to the Repository
![lifecycle-git.png](https://github.com/giovanipollachini/git-github-tips/blob/master/git-tips/images/lifecycle-git.png)

Source: 
https://git-scm.com/book/en/v2/Git-Basics-Recording-Changes-to-the-Repository


### Checking the Status of Your Files
```terminal
$ git status
$ git status --short
```

### Tracking New Files
```git
$ git add NEWFILE
```
`git add` is a multipurpose command — you use it to begin tracking new files, to stage files, and to do other things like marking merge-conflicted files as resolved. It may be helpful to think of it more as “add precisely this content to the next commit” rather than “add this file to the project”.











```
