# Fetch Without Merge
In Git, fetching without merging allows you to download updates from a remote repository without applying those changes to your current branch. This operation is useful for inspecting changes or preparing to merge them manually.

### How to Fetch Without Merge
Use the `git fetch` command:
```bash
git fetch <remote>
```
example:
```bash
git fetch origin
```

This retrieves all the changes (commits, branches, tags) from the `origin` remote but does not integrate them into your current branch.

### Key Points
1. **Fetched changes are stored in `.git/`**: The changes are kept in your local repository but do not affect your working directory.
2. **Inspect Fetched changes**: Use `git log` or `git diff` to review the updates before deciding to merge or rebase.
- To compare your current branch with the remote branch
```bash
git diff origin/<branch-name>
```
 - To view the fetched commits:
```bash
git log HEAD...origin/<branch-name>
```
3. **Selective fetching**: Fetch only a specific branch:
```bash
git fetch <remote> <branch-name>
```

### **Why Use Fetch Without Merge?**
- **Avoid accidental merges**: You might want to review changes before integrating them.
- **Stay informed**: Check what has changed on the remote branch.
- **Prevent conflicts**: Identify potential conflicts before attempting a merge.

### **Next Steps After Fetching**
Once you've fetched the changes, you can:
1. **Merge changes**:
```bash
git merge origin/<branch-name>
```
This will integrate the fetched updates into your current branch.

2. **Rebase your branch**:
```bash
git rebase origin/<branch-name>
```
This applies your changes on top of the fetched updates.
3. **Do nothing**: If you fetched the changes only for inspection, you don’t need to take further action.
