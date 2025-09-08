## How to restore the recent changes in a file at Working Area?

```bash
git restore <filename>
````

---

## How to get the remote repository code to Local Repository?

```bash
git clone <remote_repo_url>
```

# When Branches Will Not Delete in Git

In Git, branch deletion depends on whether the branch has been **properly merged** into another branch (e.g., `main`, `develop`) or not.  

---

## 1. Improper Merge  

An **improper merge** means that commits exist in a branch but **have not been merged** into another branch.  

- If you try to delete such a branch with the safe delete command, Git will **prevent deletion** to avoid data loss.  

Example:  

```bash
git branch -d <branch_name>
````

Git will show a warning and not delete the branch.

✅ Solution: If you still want to delete it, use the **force delete** option:

```bash
git branch -D <branch_name>
```

* `-D` → forcefully deletes the branch, even if unmerged.
* ⚠️ Warning: This can cause **loss of unmerged commits**, so use carefully.

---

## 2. Proper Merge

A **proper merge** means that the commits from your branch have already been merged into another branch.

* In this case, it is safe to delete the branch, and Git allows it without force.

Example:

```bash
git branch -d <branch_name>
```

* `-d` → safely deletes the branch only if it is already merged.
* No risk of losing commits since everything is already in the target branch.



# Git Stash Guide

## What is the stash?

Stash is a **temporary save**.  
When a developer is in the middle of work and the file changes are not ready to commit, they can **stash** the changes and switch to another branch without losing the progress.  

---

## How to show list of the stashes?

```bash
git stash list
````

👉 Lists down all the stashes.

---

## How to create the stash?

```bash
git stash save "comments"
```

👉 Creates a stash with the given comment.

---

## How to unstash the changes from stash?

```bash
git stash apply <stash_id>
```

👉 Applies the changes from the given stash.

---

## How to remove the recent stash?

```bash
git stash drop
```

👉 Removes the most recent stash.

---

## How to remove the specific stash?

```bash
git stash drop <stash_id>
```

👉 Removes a particular stash by its ID.

---

## How to delete all the stashes at a time?

```bash
git stash clear
```

👉 Deletes all the stashes.

---

## How to unstash the changes and delete the stash at a time?

```bash
git stash pop
```

👉 Applies the latest stash and deletes it immediately.




