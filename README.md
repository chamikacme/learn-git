
# git-test: A Practice Project for Git and GitHub 

This is a guide to get more familiar with version control using Git and GitHub and this will give the a excellent start to begin your journey with Git. This will updated continuously. Star repository and keep in touch. Feel free to provide any feedback via the contacts in the bottom.

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

Adding option `-b` will create a new branch with given branch_name and checkout to it. (Ex: `git checkout -b <branch_name>`)
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

**Push changes in current branch to already set tracking branch in remote repository**

`--force` will forcefully send current commit, disregarding commits that are ahead in remote repository.
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

**Fetch data from remote repository (Without pulling)**

Adding `--prune` option will delete all the files that are not reachable from the current branch.
```
git fetch
```

**Prune data from remote repository (Without fetching)**
```
git remote prune
```

**Set prune default with fetch**
```
git config –global fetch.prune true

```

**Reset to previous commit**

There are three options, `--soft`, `--hard`, and `mixed`(default). `--soft` will remove commits and keep changes remain on staged area. `--mixed` will remove commits and keep changes in working area(unstaged). `--hard` will remove commits and all changes up to given commit.
```
git reset <previous_commit_id>
```

**Rebase current branch**

There are two options, Standard (default) and `--interactive`. Standard (default) mode will rebase the branch automatically. The interactive mode will allow you to alter individual commits.
```
git rebase <base>
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

**Install gitk for git tree**
```
sudo apt install gitk
```

**View git tree**
```
gitk --all
```

## Conflict Handling

Conflict handling is needed when the files that are trying to merge have conflicts. Then those conflicts will show up as follows:

```
// Content without conflicts.
<<<<<< HEAD
// ...
// Content from active branch.
// ...
======
// ...
// Content from source branch.
// ...
>>>>>> <source-branch-name>
```

There are few options available for conflict handling.

1. Keep the content from the active branch and disregard the content from the source branch.
2. Keep the content from the source branch and disregard the content from the active branch.
3. Keep the content from both branches.
4. Disregard the content from both branches.
5. Edit the file in some other way.

The suitable option should be selected depending on the scenario.

## SSH Key Pair

When pushing changes to a remote repository, it's essential to verify that the person who sends the data is an authorized person. For that, an SSH key pair is used. Here, an SSH key pair is created, with a public key and a private key. The public key is sent to the remote repository. The private key is kept safely with the authorized person. When an update is sent, a remote repository can verify the sender by comparing the public key they have with the private key that the user has.


In Ubuntu, a SSH key pair can be created using the following command: Press Enter in the next steps to keep the default settings, or you can change those as you need.
```
ssh-keygen
```

Then a key pair will be created in the `'<home-path>/.ssh'` directory (or in the directory you specified). In that directory, `id_rsa.pub` will contain the public key. Open it with a text editor to copy the text, and add it to your remote repository.

## git fetch and git pull

In the Fetch method, it doesn't update the files in the local repository. It just fetches information and checks whether it has been updated. To get those data, it needs to merge the remote repository's changes (commits) into the local repository. The following commands can be used for that.
```
git fetch
git merge <remote_name>/<remote_branch_name>
```

In the pull method, it directly updates the local files with changes in the remote repository. It does the combined function of both `fetch` and `merge`.
```
git pull
```

## git commit --amend

`--amend` can be used with `git commit` command to add minor changes to the previous commit. It will not create a new commit, but alter the previous one. The staged changes will be committed.
```
git commit --amend --no-edit
```
`--no-edit` tag will help skip the entering commit message step, keeping the same commit message.

This command can be used to update the commit message also.
```
git commit --amend -m "Updated commit message"
```

## Resources Used

+ `Git මුල් පොත` by `Supun Budhajeewa`
+ Internet resources.

## Contact

+ [Email](mailto:chamikacme@gmail.com?subject=I%20visited%20your%20Git%20Commands%20Repository)
+ [LinkedIn](https://www.linkedin.com/in/chamikacme/)


---