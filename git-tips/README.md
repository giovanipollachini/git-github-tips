# Tips on Git
Tips on Git for Linux.

## Config file
Stores name, e-mail, default program for text files, etc.

### First-Time setup, edit config file:
https://git-scm.com/book/en/v2/Getting-Started-First-Time-Git-Setup

### Check configuration settings
```shell
git config --list
```
### Insert default text editor

Use a text editor which can be launch on terminal and that leaves the terminal occupied while running. Suggestions: VI / VIM (terminal), Leafpad (opens in a new window but locks terminal while running).

```shell
git config --global core.editor "leafpad"
```

## Getting a Git Repository
This action is done only once, to set up Git inside a directory. If you want to resume your work, it is not necessary to run any command. It is only necessary to `cd` to the directory of the desired project.

### Initializing a Repository in an Existing Directory
```shell
cd /home/user/my_project
git init
```

### Cloning an Existing Repository
```shell
git clone https://github.com/repository my-local-repository
```

## Recording Changes to the Repository
![lifecycle-git.png](https://github.com/giovanipollachini/git-github-tips/blob/master/git-tips/images/lifecycle-git.png)

Source: 
https://git-scm.com/book/en/v2/Git-Basics-Recording-Changes-to-the-Repository


### Checking the Status of Your Files
```shell
git status
git status --short
```

### Tracking New Files
```shell
git add NEWFILE
```
`git add` is a multipurpose command — you use it to begin tracking new files, to stage files, and to do other things like marking merge-conflicted files as resolved. It may be helpful to think of it more as “add precisely this content to the next commit” rather than “add this file to the project”.


### Ignoring Files

Useful for log files produced by your system, binary files or files produced by your build system. 
The file `.gitignore` contains patterns used to ignore these files. It is only necessary to edit this file, adding all the files or patterns you want git to ignore. 

More information: https://git-scm.com/book/en/v2/Git-Basics-Recording-Changes-to-the-Repository -> Subsection: Ignoring Files


### Viewing Your Staged and Unstaged Changes

```shell
# View unstaged changes
git diff
# View staged changes
git diff --staged
```
`git diff` shows you the exact lines added and removed to the files — the patch.
You can configure Git Diff in an External Tool.

### Committing Your Changes

```shell
# Commit staged changes
git commit
# Stage all files and commit changes
git commit -a
# Commit with inline message
git commit -m "My message about the changes in the code"
```
Recommendations for commits: 
https://chris.beams.io/posts/git-commit/

Commit a change with both message and description:
https://stackoverflow.com/questions/16122234/how-to-commit-a-change-with-both-message-and-description-from-the-command-li

### Removing Files

```shell
# Stage the file removal 
git rm FILE-TO-BE-REMOVED
# Stage for removal modified files or already staged files
# (you have to force removal in this case)
git rm -f FILE-TO-BE-REMOVED
```

### Moving and Renaming Files

```shell
# Move files
git mv FILE-FROM FILE-TO
# Rename files
# (move to the same folder with a diferent name)
git mv OLD-NAME NEW-NAME
```

## Viewing the Commit History

### Viewing the Commit History
```shell
git log
git log --pretty=oneline
```

Other options: https://git-scm.com/book/en/v2/Git-Basics-Viewing-the-Commit-History

## Undoing Things

### Redo the commit

If you want to redo your last commit, make the additional changes you forgot, stage them, and commit again using the --amend option. It is also useful for fixing the commit message.

```shell
git commit --amend
```

### Unstaging a Staged File
```shell
git reset HEAD FILE-TO-BE-UNSTAGED
```

### Unmodifying a Modified File
```shell
git checkout -- FILE
```

## Git Branching - Branch Management

### List branches
```shell
# List branches
git branch
```

### Create new branch
```shell
# Create new branch called 'branch-name'
git branch branch-name
```

### Move to another branch
```shell
# Move the HEAD to another branch
git checkout branch-name
```

### Merge branches
```shell
# Switch to branch 'master'
git checkout master
# Merge branch 'branch-name' into 'master
git merge branch-name
```
