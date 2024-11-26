# What is a Repository?
A Git repository is the .git/ folder inside a project. This repository tracks all changes made in files in your project, building a history over time. Meaning, if you delete the .git/ folder, then you delete your project's history.
#### Key Features of a Git Repository:
- **Version Control**: Tracks changes to files over time, enabling you to revert to earlier versions or review the history of changes.
- **Snapshots**: Stores snapshots of your project at specific points in time (commits).
- **Branching and Merging**: Supports creating branches to work on different features independently and merging them back into the main branch when ready.
- **Collaboration**: Facilitates teamwork by allowing multiple contributors to work on the same project concurrently.

## Types of Repositories:
**Local Repository**: Resides on your computer and stores the project's history locally. you can create it using:

```bash
git init
```

**Remote Repository**: A version of the repository hosted on a server (Github, GitLab, Bitbucket) that others can access and contribute to.
### Typical Structure of a Git Repository:
When you create a Git repository, a hidden `.git` directory is created in the root of the project. This directory contains:
- **HEAD**: Points to the current branch.
- **Objects**: Stores the data for your commits, such as blobs (file data), trees (directory structure), and commits (metadata).
- **Refs**: Contains references to branches and tags.
- **Config**: Repository-specific configuration settings. [[How to config git]]
## The Working directory
The **working directory** is the local workspace where you develop your project. It reflects the current state of your files and is distinct from the Git repository, allowing you to:
1. Modify files.
2. Stage changes.
3. Commit them to preserve history.
#### **Key Characteristics**:
- **Editable**: The working directory is where you make changes to project files.
- **Unstaged Changes**: New or modified files are not tracked until explicitly staged using `git add`.
- **Difference from Repository**: It shows differences between the committed version and your current changes.
## The Three states in git
In Git, files can exist in one of three states:
1. **Modified**:
- The file has been changed but is not yet staged.
- These changes are local and exist only in the working directory.
- **Example**: You edit `file.txt`, but have not added it to the staging area yet.	
3. **Staged**:
- The file has been added to the **staging area** (also called the Index) and is ready for committing.
 - Command: `git add <file>`
4. **Committed**:
- The file's changes are saved to the repository history.
 - Command: `git commit -m "message"`
## How to Work with a Git Repository:

1. **Initialize a Repository**: 
 ```bash
 git init
```
This creates a new Git Repository in the current directory.
2. **Clone a Remote Repository**:
```bash
git clone <repository-url>
```
This creates a local copy of a remote repository.