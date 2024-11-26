# How to config Git
The `git config` command is an essential tool in Git for managing configuration settings. These settings control Git’s behavior and can be applied at different levels: **system**, **global**, or **local (repository-specific)**.
### **Key Features of `git config`**:
1. **Set Configuration Values**: Define how Git behaves for your system, user, or specific repository.
2. **Retrieve Configuration Values**: Display current configuration settings.
3. **Scopes of Configuration**:
    - **System-wide**: Applies to all users and repositories on the system. Stored in `/etc/gitconfig`.
    - **Global**: Applies to all repositories for the current user. Stored in `~/.gitconfig`.
    - **Local**: Applies only to the current repository. Stored in `.git/config` in the repository directory.
### **Common Use Cases**:
#### 1. **Setting Your Identity**
This is a global configuration to identify you when making commits:
```bash
git config --global user.name "Your Name"
git config --global user.email "youremail@example.com"
```
#### 2. **Setting Editor Preferences**
Specify your default text editor for Git commands like `git commit` or `git rebase`:
```bash
git config --global core.editor "vim"
```
#### 3. **Viewing Configuration Values**
To see a specific configuration:
```bash
git config user.email
```
To list all configurations:
```bash
git config --list
```
#### 4. **Setting Up Aliases**

Create shortcuts for commonly used Git commands:
```bash
git config --global alias.co checkout
git config --global alias.br branch
git config --global alias.st status
```
#### 5. **Removing a Configuration**
Unset a specific configuration:
```bash
git config --unset user.email
```