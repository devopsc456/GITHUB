
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
