 - git clone https://github.com/zaedulislam/Graph_Neural_Networks.git

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
