# What is gitignoregit?
A **gitignore** file specifies intentionally untracked files that Git should ignore. Files already tracked by git are not affected.
### Syntax
- Blank lines or lines starting with `#` are ignored (used for comments).
- You can use wildcards like `*`, `?`, or `[a-z]` for pattern matching.
- A leading `/` limits the scope to the directory containing the `.gitignore` file.
- A trailing `/` indicates a directory.
### **Common Usage**:
- Ignore `node_modules/` for Node.js projects.
- Ignore `*.log` files or `.env` files containing sensitive information.

### Example

```gitgnore
# Logs
*.log

# Node modules
node_modules/

# Environment variables
.env

# Build outputs
dist/

```