# Git Branch Commands

## How to list out all branches?
```bash
git branch
# or
git branch --list
````

## How to create branches?

```bash
git branch <branch_name>
```

## How to switch or checkout another branch?

```bash
git checkout <branch_name>   # move to branch
# or
git switch <branch_name>     # move to branch
```

## How to switch the branch while creating itself?

```bash
git checkout -b <branch_name>   # create and move to branch
```

## How to delete a branch in local repo?

```bash
git branch -d <branch_name>   # current checked-out branch cannot be deleted
```

## How to rename a branch in local repo?

```bash
git branch -m <old_branch_name> <new_branch_name>
```

## How to see all branches in local repo and remote repo?

```bash
git branch -a
```

## How to see all branches in remote repo?

```bash
git branch -r
```

## How to push all branches from local repo to remote repo?

```bash
git push <alias_name> branch1 branch2
# or
git push <alias_name> --all
```

## How to delete a branch in remote repo using command?

```bash
git push <alias_name> :branch_name   # removes branch from remote repo
```

## How to do fast-forward merge?

1. Create the branch `development` (or any name you provide) from `master`.  
2. By default, all files are copied from `master` to `development` branch.  
3. Modify any file and commit in `development` branch.  
4. Then go to `master` branch and run the below command to check the difference:

   ```bash
   git diff development
````

5. Then run the below command:

   ```bash
   git merge development
   ```

6. You may get a response like this:

   ```
   Updating 083fa89..d8cdd25
   Fast-forward
   java.txt | 1 +
   1 file changed, 1 insertion(+)
   ```

## What is merge conflict?

👉 A merge conflict happens when two developers update the **same file and the same line**.

### Steps to Reproduce and Resolve:

1. Update the file in `master` branch and commit the changes.

2. Update the same file in `development` branch and commit the changes.

3. Switch to `master` and run:

   ```bash
   git merge development
   ```

4. Resolve conflicts by **removing unused/conflicting lines**, then commit the changes.

---

## How to get file changes from one branch to another branch from remote repository?

Use the `git pull` command:

```bash
git pull <remote_repo_alias_name> master   # You are in development branch
```

Example:

```bash
git pull gitpartice master
```

