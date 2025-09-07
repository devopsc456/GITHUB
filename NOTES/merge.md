# Fast-Forward Merge in Git

## Steps for Fast-Forward Merge

1. Create a new branch (example: `development`) from `master`.
   ```bash
   git checkout -b development master
````

> By default, all files are copied from `master` to `development`.

2. Modify any file and commit the changes in the `development` branch.

3. Switch back to the `master` branch and check the difference:

   ```bash
   git diff development
   ```

4. Merge the `development` branch into `master`:

   ```bash
   git merge development
   ```

   **Response:**

   ```
   Updating 083fa89..d8cdd25
   Fast-forward
   java.txt | 1 +
   1 file changed, 1 insertion(+)
   ```


## What is a Merge Conflict?

A merge conflict occurs **when two developers update the same file and the same line** in different branches.

## Steps to Reproduce and Resolve Merge Conflict

1. Update a file in the `master` branch and commit the changes.
2. Update the **same file** in the `development` branch and commit the changes.
3. Switch to the `master` branch and run:

   ```bash
   git merge development
   ```
4. Resolve the conflict manually by removing unused/duplicate lines, then commit the changes.

---

# Pulling Changes Between Branches

To get file changes from one branch to another from remote repo:

```bash
# Run this while you are in the development branch
git pull <remote_repo_alias_name> master

# Example
git pull gitpractice master
```



Do you want me to also **add diagrams/flow illustrations** (in Markdown with Mermaid) so that it visually explains fast-forward vs. merge conflict?
```
