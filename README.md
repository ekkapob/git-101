# Git 101 Training

Let's Git

[Slide](https://docs.google.com/presentation/d/1AVjxR8bVwGqhqVdHnbDtFindELM5OW4Lp-VE00uwYJI/edit?usp=sharing)

## Git Cheat Sheet

### Fasten Git Bash
```
$ git config --global core.preloadindex true
$ git config --global core.fscache true
$ git config --global gc.auto 256
```

### Git Setup and Init

```
$ git config --global user.name “{name}”
$ git config --global user.email “{email}”
$ git commit --amend --reset-author
```

### Initalize Git repository
```
$ cd {folder}
$ git init
```

### Git Status, Add, Commit
```
# Check Git status
$ git status

# Stage file to be committed
$ git add {filename}

# Stage all files in current folder
$ git add .

# Commit staged file(s)
$ git commit -m "message"

# Stage (tracked files) and Commit
$ git commit -am "message"
```

### Git Clone
```
$ git clone {repository URL}
# i.e. git clone git@github.com:ekkapob/git-101.git
```

### Branching
```
# Create new branch
# After creating a new branch, Git will switch to the new branch
$ git checkout -b {branch name}

# Switch to a branch
$ git checkout {branch name}

# Delete a branch
$ git branch -d {branch name}   # this will delete a branch which already merged into the branch running this command.
$ git branch -D {branch name}   # force delete a branch regardless of merging status

# Change branch name
$ git branch -m {new branch name}   # change a current branch's name to new name
```

### Push
```
$ git push origin {remote branch}

# "origin" is a shorthand name for the remote repository that a project was originally cloned from e.g. GitHub repository
# "remote brach" should be the same name of the local branch a user is on.
# if names are different, use "git push origin {local branch:remote branch}"
# i.e. git push origin local-main:main
```

### Pull
```
$ git pull origin {remote branch}
# i.e. git pull origin main
```

### Update Info of Meta-data, Remote branches, and etc.
```
$ git fetch
```

### How to Merge Binary Conflicts
- [How to Merge Binary Conflicts](https://gist.github.com/ekkapob/36f9a1eeca246617ffbd33e5f6714a3f)
