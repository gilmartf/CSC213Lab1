# Useful `git` Commands:

Below are many of the most commonly used git commands. We won't necessarily use all of them. However: 

- we will use some of these commands directly,
- we will use the concepts of the others,
- and the rest are to plant seeds for the future.

## 1. Setting Up Git

You may need these commands if you are using git for the first time on the machine: 

### a. List all Configuration Settings:

```
git config --list
```

The below commands can help prevent you from repeatedly entering in this information.

### b. Globally Set Your Username for All Repos:

```
git config --global user.name "Your Username"
```

### c. Globally Set Your Email for All Repos:
```
git config --global user.email "your_email@whatever.com"
```

---

## 2. Initializing and Cloning Repos:

You are either going to be creating a brand new local repo that you will push to a remote repo **or** cloning a remote repo to
your local machine. Both of the below commands will create/clone a local git repo in your current working directory.

### a. Initialize a Local Repo:
```
git init
```

### b. Cloning a Remote Repo:
```
git clone url/to/remote/repo.git
```

---

All the below commands assume that you are in the root directory of the local git repository.


## 3. Viewing History and Changes

A lot of different information is presented depending on the status of the repo with the two below commands. Some basic info as
to what is presented is listed below each command.

### a. Viewing Repo's History:
```
git log
```
Displays the commit history.


### b. Viewing Changes:

```
git status
```
Some common things that you will see include, but are not limited to:

- Tracked unstaged files that have changes will be displayed in red.
- Tracked staged files that have been staged will be displayed in green.
- Committed files are ready to be pushed to the remote repository at any time

Either way, carefully read the message(s) returned from the output of this command!

## 4. Staging and Committing Changes:

### a. Staging a Tracked and Changed File:
```
git add path/to/file
```
Sometimes you might want to stage all the changes you made. in which case you can execute:
```
git add .
```

Be careful with this! With small projects this is probably fine, but you'll usually want to be more fine-grained with your
stagings and commits for larger projects.

### b. Committing Changes:
```
git commit -m "Your commit message goes here"
```

## 5. Undoing Changes:
Since we are dealing with relatively smaller code bases, it is probably easier to simply undo changes by manually editing our
files...However, these do come in handy quite often in larger code bases.

### a. Restoring File to Last Committed State:
```
git restore <file>
```

For the two below commands `<commit>` represents the commit's hash value.

### b. Undoing a Commit
```
git revert <commit>
```
Creates a new commit that undoes the changes made in the given commit.

### c. Resetting Current Working Branch (**Be Careful!**):
```
git reset <commit>
```
This removes commits from the repo's history! **Always be very bloody careful when altering history!**

## 6. Working with Remote Repos:

### a. Add a New Remote Repo:
```
git remote add origin /url/to/remote/repo.git
```
You should only have to do this once unless the location of the remote repo changes.

### b. View Remote URL:
```
git remote -v
```
Mostly just to help our sanity and check that things are setup correctly.

### c. Retrieve Changes from Remote Repo **without** merging them:
```
git fetch
```
Usually, this is to help us see how the remote repo differs from our local copy.

### d. Retrieve **and** Merge Changes from Remote Repo:
```
git pull
```
If there are no issues with the differences between your local and remote repo, then can safely call this command.

### e. Push Local Commits to Remote Repo:
```
git push
```
Whenever you think it is a good idea to "backup" your local changes to the remote, you should call this command.

## 7. Branching and Merging:

### a. Listing Branches:
```
git branch
```
Your current checked-out branch will be listed next to an '*'.

### b. Creating a New Branch:
```
git branch <branch-name>
```

### c. Switching to a Branch:
```
git checkout <branch-name>
```

### d. Merging Changes from a Branch into Current Branch:
```
git merge <branch-name>
```
