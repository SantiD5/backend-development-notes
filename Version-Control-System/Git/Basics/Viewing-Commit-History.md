# viewing Commit History
To view the commit history in Git, you can use the `git log` command. This command shows the commit history of your repository, including details such as commit hashes, authors, dates, and commit messages.
```bash
git log
```
This displays the commit history in reverse chronological order (newest commits first).

### Customizing the Output

1. **One-Line Summary**: Display a concise commit history.
```bash
git log --oneline
```
Example:
```bash
a1b2c3d Fix bug in login form
e4f5g6h Add feature to upload images

```

2. **Show Graph**: Visualize the branch structure with a commit graph.
```bash
git log --oneline --graph
```
3. Limit Number of Commits
```bash
git log -n <number>
```
4. Filter by Author:
```bash
git log --author = <author_name>
```
5. Search by Commit Message:
```bash
git log --grep="<search_term>"
```
6. Display specific file's History:
```bash
git log -- <file_name>
```
7. Show Commit Details in a Specific Format:
```bash
git log --pretty=format:"%h - %an, %ar : %s"
```
8. Show Commit files that were modified:
```bash
git log --stat
```
9. Prettier Format
```
git log --pretty=format:"%Cred%h%Creset -%C(yellow)%d%Creset %s %Cgreen(%cr) %C(bold blue)<%an>%Creset" --author="Santiago" --all
```


### Comparing Changes in History
**View Changes in a Commit**:
```bash
git show <commit_hash>
```
Compare Two Commits:
```bash
git diff <hash> <hash2>
```