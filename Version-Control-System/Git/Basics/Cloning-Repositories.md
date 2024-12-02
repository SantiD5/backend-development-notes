# Cloning Repositories
`git clone` is a Git command line utility which is used to target an existing repository and create a clone, or copy of the target repository. In this page we'll discuss extended configuration options and common use cases of `git clone`. Some points we'll cover here are:

- Cloning a local or remote repository
- Cloning a bare repository
- Using shallow options to partially clone repositories
- Git URL syntax and supported protocols

### Cloning a Local or Remote Repository
**Local Repository**: Clone a repository from your local file system using the path.
```bash
git clone /path/to/repository
```
This is useful for working with repositories shared between teams on the same network.

**Remote Repository**: Clone a repository hosted on a server or service (e.g., GitHub, GitLab).
```bash
git clone https://github.com/user/repo.git
```
Git will download the repository's content, including its history, and create a new directory with the same name as the repository.

### Cloning a Bare Repository 
A **bare repository** is a version of the repository without a working directory. It's used for remote collaboration and lacks files meant for direct edits.
```bash
git clone --bare https://github.com/user/repo.git
```
This is commonly used to set up mirrors or a central remote repository.

### Using Shallow Options to Partially Clone Repositories
Clone a repository without its full history to save space and reduce download time.
- Clone only the latest commit:
```bash
git clone --depth 1 https://github.com/user/repo.git
```
- Specify a specific number of commits:
```bash
git clone --depth <num> https://github.com/user/repo.git
```
- Shallow clone with minimal history while tracking branches:
```bash
git clone --single-branch --branch <branch-name> https://github.com/user/repo.git
```
