# Working Locally with a Repository

## Current State

```
git status
```

* information regarding the state of the working tree, the index, and
  the repository

## Stagging and Committing Local Edits

The .gitignore (include in repository) and .git/info/exclude (not
included in repository) files contain paterns of files to ignore
(e.g., **\*~** to ignore backup files and **\*.o** to ignore object
files).

```
git add [-p] <path> ...
```

* stage *path* for committing
* `-p` interactively select specific patches (blocks of edits)

```
git commit [--amend [--no-edit]] [-m <message> ...] [<file> ...]
```

* commit index (staged changed) of just *file*...
* `--amend` adds to previous commit instead of creating a new one
* `--no-edit` don't change previous commit message
* `-m` provide *message* on command line

## Unstagging and Undoing Local Edits

```
git reset [-p] <path> ...
```

* reset *path* in stagging area (undo `git add`)
* `-p` interactively select specific patches (blocks of edits)

```
git checkout [-p] <path> ...
```

* reset *path* in working directory (undo non-staged local edits)
* `-p` interactively select specific patches (blocks of edits)
