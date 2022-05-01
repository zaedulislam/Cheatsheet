 - git clone https://github.com/zaedulislam/Graph_Neural_Networks.git
## How to Push an Existing Project to GitHub
### Step 1: Create a new GitHub Repo
### Step 2: Initialize Git in the project folder
#### Initialize the Git Repo
```
git init
```
#### Add the files to Git index
```
git add -A
```
#### Commit Added Files
```
git commit -m 'Added my project'
```
#### Push to GitHub
```
git push -u -f origin master
```
#### All together
```
git init
git add -A
git commit -m 'Added my project'
git remote add origin git@github.com:sammy/my-new-project.git
git push -u -f origin master
```
---
### Check Current Branch
```
git branch
```
## git reset
### Undo git reset
Git keeps a log of all ref updates and to view them,
```
git reflog
```
And the output may look something like below,
```
39ab761 HEAD@{0}: reset: moving to HEAD~1
b55c098 HEAD@{1}: Update argument list ...
```
To go back at the commit before reseting,
```
git reset HEAD@{1}
```
Or,
```
git reset b55c098
```
---
### Change Git Remote URL
```
git remote set-url <remote_name> <remote_url>
```

For example,
```
git remote set-url origin https://git-repo/new-repository.git
```

- In order to verify that the changes were made, you can use the “git remote” command with the “-v” option (for verbose)
```
git remote -v
```
---


# Reference
- https://devconnected.com/how-to-change-git-remote-origin/
- https://www.digitalocean.com/community/tutorials/how-to-push-an-existing-project-to-github
