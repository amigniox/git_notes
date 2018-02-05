# Working with Branches

## Creating and Deleting Branches

```
git branch [-a] [-v]
```

* List branches
* `-a` include remote branches
* `-v` include current commit information

```
git branch <name> [<commit>]
```

* Create branch *name* start at *commit* (defaults to last commit)

```
git branch -m <old name> <new name>
```

* Rename branch *old name* to *new name*

```
git branch -d <name>
```

* Delete branch *name*

## Switching Branches

```
git checkout [<branch>]
```

* Switch index and working tree to *branch*

```
git checkout -b <branch> [<commit>]
```

* Create new branch *branch* starting at commit *commit* (defaults to
  last commit)

### The Stash

Switching branches requires a clean state.  Frequently you have work
in progress that you would like to come back to.  The stash is a
temporary place to store work (under the hood it is just another
commit and associated reflog).

```
git stash [-p] [<message>]
```

* Stash outstanding changes away (push)
* `-p` interactively select specific patches (blocks of edits)

```
git stash list [-p]
```

* List stashes
* `-p` include patches (differences) between commits

```
git stash apply [<stash>]
```

* Re-apply *stash* (defaults to last) and then drop it (pop)

```
git stash drop [<stash>]
```

* Drop *stash* (defaults to last)

```
git stash clear
```

* Drop all stashes

## Reflog

The reflog tracks previous values of branches.  This is not the
history of the commit the branch currently points to but rather the
history of what commits the branch has pointed to in the past.  It is
specific to the local repository.

```
git reflog [<branch>]
```

* List previous values of *branch* (defaults to current branch)

## Tags

Tags provide a human friendly name for commits.  The commit they point
to remains the same unlike branches which roll forward with each
commit.

```
git tag
```

* List tags

```
git tag <name> [<commit>]
```

* Create tag *name* pointing to commit *commit* (defaults to last
  commit)

```
git tag -d <name>
```

* Delete tag *name*

[Back to content index](Home.md) (Index)
