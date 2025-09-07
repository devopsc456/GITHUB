# Git Branch Commands

1. ## How to list out all branches?
```bash
git branch
# or
git branch --list
````

2. ## How to create branches?

```bash
git branch <branch_name>
```

3. ## How to switch or checkout another branch?

```bash
git checkout <branch_name>   # move to branch
# or
git switch <branch_name>     # move to branch
```

4. ## How to switch the branch while creating itself?

```bash
git checkout -b <branch_name>   # create and move to branch
```

5. ## How to delete a branch in local repo?

```bash
git branch -d <branch_name>   # current checked-out branch cannot be deleted
```

6. ## How to rename a branch in local repo?

```bash
git branch -m <old_branch_name> <new_branch_name>
```

7. ## How to see all branches in local repo and remote repo?

```bash
git branch -a
```

8. ## How to see all branches in remote repo?

```bash
git branch -r
```

9. ## How to push all branches from local repo to remote repo?

```bash
git push <alias_name> branch1 branch2
# or
git push <alias_name> --all
```

10. ## How to delete a branch in remote repo using command?

```bash
git push <alias_name> :branch_name   # removes branch from remote repo
```
