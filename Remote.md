# Working with Remote Repositories

## Adding Remote Repositories

```
git remote [-v]
```

* List remote repositories
* `-v` include URLs

```
git remote add <name> <url>
```

* Add remote repository *url* and assign it name *name*

```
git remote rename <old name> <new name>
```

* Change name from *old name* to *new name*

```
git remote remove <name>
```

* Remove remote repository *name*

## Exchanging Work

Mappings between local and remote branches are specified with refspecs.
These have the form *local branch*:*remote branch*.  The default remote
and refspec can be set in the config.

* The special prefix **+** allows commits to be dropped (a
  non-fast-forward update)
* An blank *local branch* will delete *remote branch* in a push

```
git push [--tags] [<repository> [<refspec> ...]]
```

* Push refs according to *refspect* to *repository* (defaults depend
  on config)
* `--tags` also push any tags

```
git fetch [<repository> [<refspec> ...]]
```

* Fetch refs according to *refspec* from *repository* (defaults depend
  on config)

```
git merge [-m <message>] [<commit> ...]
```

* Merge in any work under *commit*s (defaults to associated remote
  branch) that isn't already under last commit
* `-m` provide *message* on command line

```
git pull [<repository> [<refspec> ...]]
```

* Fetch refs according to *refspec* from *repository* (defaults depend
  on config) and then merge them


[Back to content index](Home.md) (Index)