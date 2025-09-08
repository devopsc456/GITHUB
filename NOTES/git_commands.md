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

## Case: Improper Merge  

An **improper merge** occurs when commits exist in a branch that have **not been merged** into another branch (for example, `main` or `develop`).  

In such cases, if you try to delete the branch normally using:  

```bash
git branch -d <branch_name>
````

Git will **not allow deletion**, because it prevents potential **loss of unmerged work**.

---

## Force Deletion

If you are sure you want to delete the branch (even though it contains unmerged commits), you can use the **force delete option**:

```bash
git branch -D <branch_name>
```

* `-D` → stands for **force delete**, which is equivalent to `--delete --force`.
* It will remove the branch regardless of whether it is merged or not.

⚠️ **Warning**: Use this with caution, as unmerged changes will be permanently lost.
