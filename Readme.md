# Readme

New repository

```
$ pre-commit install

# 20kb has not been staged yet
$ pre-commit run --all-files
check for added large files..............................................Passed

# 20kb has been staged
$ pre-commit run --all-files
check for added large files..............................................Failed

# Commit using --no-verify
$ git commit -m "Add 20kb file" --no-verify

# --all-files ignores 20kb.txt now
$ pre-commit run --all-files
check for added large files..............................................Passed

# Change 20kb.txt and commit
$ git add 20kb.txt
$ git commit -m "Change 20kb file"
check for added large files..............................................Passed
$ pre-commit run --all-files
check for added large files..............................................Passed
```