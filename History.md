# Examining your Repository

## Inspecing the Repository

```
git show [<object>]
```

* show *object* (defaults to last commit)

```
git log [-p] [--graph] [<revision range>] [<path> ...]
```

* show log messages spanning *revision range* (defaults to last commit
  and all its parents) for *path*s (defaults to everthing)
* `-p` include patches (differences) between commits
* `--graph` include graph indicating branch structure

```
git blame [<commit>] <file>
```

* show who lasted edited each line of *file* starting with *commit*
  (defaults to last commit)

## Differences

```
git diff [--words-diff] [<path> ...]
```

* changes made to working tree relative to index
* `--words-diff` do a word-by-word diff instead of a line-by-line diff

```
git diff [--words-diff] [--cached] <commit> [<path> ...]
```

* changes made relative to given commit
* `--cached` compare with index instead of working tree
* `--words-diff` do a word-by-word diff instead of a line-by-line diff

```
git diff [--words-diff] <first commit> <second commit> [<path> ...]
```

* changes made between *first commit* and *second commit* (can also
  use *first commit*..*second commit*)
* `--words-diff` do a word-by-word diff instead of a line-by-line diff
