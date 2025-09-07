
# How to do fast-forward merge?

1. Create a new branch (e.g., `development`) from `master`:
   ```bash
   git checkout -b development master
````

2. By default, all files are copied from `master` to the `development` branch.

3. Modify any file and commit in the `development` branch.

4. Switch back to the `master` branch and check the differences:

   ```bash
   git checkout master
   git diff development
   ```

5. Merge the `development` branch into `master`:

   ```bash
   git merge development
   ```

6. Example output:

   ```text
   Updating 083fa89..d8cdd25
   Fast-forward
   java.txt | 1 +
   1 file changed, 1 insertion(+)
   ```

# What is Merge Conflict?

A **merge conflict** occurs when two developers update the same file and the same line. This results in a conflict when trying to merge the changes.

## Steps to Resolve Merge Conflict

1. **Update the file in `master` branch and commit the changes.**

2. **Update the same file in `development` branch and commit the changes.**

3. **Go to `master` branch and apply:**

   ```bash
   git merge development
````

4. **Remove the conflicting or unused lines and then commit the changes.**



# How to Get File Changes from One Branch to Another in a Remote Repo

To get the file changes from one branch to another branch in a remote repository, follow these steps:

1. Make sure you are on the **development** branch (or the branch you want to update).

2. Pull the changes from the remote `master` branch:

```bash
git pull <remote_repo_alias_name> master
````

**Example:**

```bash
git pull gitpractice master
```

This will fetch the changes from the remote `master` branch into your current `development` branch.
