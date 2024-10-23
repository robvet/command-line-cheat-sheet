# Git Hub Command Line Cheat-Sheet

## Create new repository
```
git init
git add README.md
git commit -m "first commit"
git branch -M main
git remote add origin https://github.com/robvet/test.git
git push -u origin main --force
```
## Backtracking to the GitHub repo from which you cloned code
```
# Situation: Cloned code onto my laptop, but want to get to the original GitHub Repo
git remote get-url origin # Get back to the cloned repo
git remote get-url upstream # Get gack to the forked repo
```

## Push existing repository
```
git remote add origin https://github.com/robvet/test.git
git branch -M main
git push -u origin main
```

## Create local branch shortcut command
```
git checkout -B <branch name>
```

## Set remote (upstream) server
```
git remote -v # Lists remote repos 
git remote add upstream https://github.com/MicrosoftDocs/mslearn-tailspin-spacegame-web.git # Add remote repo, in this case, upstream
```

## Delete Branch
```
# Delete local branch
git branch -d  local_branch_name
# Delete local branch with unmerged changes - D is alias Delete Force
git branch -D local_branch_name
# Delete remote branch
git push remote_name -d remote_branch_name>
git push origin -d test
# Reference
https://www.freecodecamp.org/news/git-delete-branch-how-to-remove-a-local-or-remote-branch/
```

## Fetch branch from upstream repo
```
# Applicable to fetch a branch when forked to upstream repo
git fetch upstream <branch name> # fetch remote branch
git checkout -B <branch name> upstream/<bracnh name> # create local branch for models-pacakge
```

## Clone branch
```
# Clone main and then view branches
git branch -a
# Pick the target branch and input following command
git clone --branch <branchname> <remote-repo-url>
# Reference link
https://www.freecodecamp.org/news/git-clone-branch-how-to-clone-a-specific-branch/
```


## Remove untracked directories
```
# To remove untracked files
git clean -f
# TO remove untracked directories
git clean -fd
```
