# Workflow:

## 1) Inital Setup

```git init && git remote add origin <project_remote_url.git>```

fetch branches not on local, and on remote repo

```git fetch origin```

```git checkout -b <working_branch_name>```

make .gitignore file

## 2) Working

pull most recent changes on master
```git pull origin master```

```<coding....>```

```git add .```

```git commit -m "something descriptive"```

push working branch >> then generate pull request on github

```git push origin <working_branch_name>```

## 3) Approval of Pull Request means: merge working to origin (master branch)



## Useful commands:

Display commit tree with: 
```
git log --decorate --all --graph --oneline
```

# General Info:
`origin` is simply an alias for your remote repository
```remote add origin <remote_repo_url.git>```
translates to: remote repo's origin location is at 

`HEAD` is sentinal pointer to current branch
`master` is not a special branch name, just like any other
- best practice to use for maintaing stable version


Pull Requests are like an additional staging area, where other collaborators 
can review changes you've made on your branch BEFORE merging to master
- as a result, master branch is never being updated/pushed on directly
- updates to master will only come up PR approval 




