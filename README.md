
# git-test: A Practice Project for Git and GitHub 

This project was done to get more familirized with version controlling with Git and GitHub. I have shared some of my learnings below.

## Some useful Git Commands

**Install git on Ubuntu**
```
sudo apt install git
```

**Initialize a git project**
```
git init
```

**Setting-up global username**
```
git config --global user.name "My Name"
```

**Setting-up global email**
```
git config --global user.email "test@test.com"
```

**Check staged changes**
```
git status
```

**Stage a file**
```
git add <file_name>
```

**Stage multiple files**
```
git add <first_file> <second_file> <third_file>
```

**Stage all in the current directory**
```
git add .
```

**Commit the staged changes**
```
git commit
```

**Commit the staged changes with commit message**
```
git commit -m "Commit message"
```

**Switch to a previous commit**
```
git checkout <commit_id>
```

**View all branches**
```
git branch
```

**Create a new branch from current branch**
```
git branch <branch_name>
```

**Switch to an another branch**
```
git checkout <branch_name>
```

**Merge a branch to current branch**
```
git merge <source_branch_name>
```

**Delete a branch**
```
git branch -D <branch_name>
```

**Check connected remote repository**
```
git remote -v
```

**Connecting to a remote repository (remote_name=origin)**
```
git remote add <remote_name> <remote_url>
```

**Push changes in current branch to remote repository with setting a tracking branch**
```
git push <remote_name> -u <remote_branch_name>
```

**Push changes in current branch to already setted tracking branch in remote repository**
```
git push
```

**Clone a remote repository to local**
```
git clone <remote_url>
```

**Pull updates on remote repository**
```
git pull
```

**Add a tag to a specific commit**
```
git tag <tag_name> <commit_id>
```

**Add a tag to current commit**
```
git tag <tag_name>
```

**Push tags to remote repository**
```
git push <remote_name> <tag_name>
```

**Install gitk on for git tree**
```
sudo apt install gitk
```

**View git tree**
```
gitk --all
```

## Resources Used
For this task, I mainly referred `Git මුල් පොත` by `Supun Budhajeewa` and internet resources.
