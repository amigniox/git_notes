# Specifying Commits

## Definitive

* `<hash>` unique identifier for each commit (SHA-1 hash of the
  commit, e.g., **d67046...9fe3ef**)

## Specific Work

* `<tag>` static name pointing to a specific commit (e.g., **v1.0.1**)
* `<branch>` dynamic name pointing to last commit on work-in-progress
  (e.g., **master**)

## Internal

* `HEAD` commit currently checkout into working directory
* `stash` temporary commit of work in progress

## Previous (values of non-static references)

* `<branch>@{<date>}` value of *branch* in this repository on *date*
* `<branch>@{<n>}` *n*th previous value of *branch*

## Relative (parents of commit)

* `<ref>^` first parent of *ref*
* `<ref>^<n>` *n*th parent of *ref*
* `<ref>~<n>` *n*th first parent of *ref* (i.e., `<ref>^...^` *n* times)

## Range

* `<first ref>..<second ref>` every commit in *second commit*
  not in *first commit*
* `<ref>` every commit reachable from *commit*
* `^<ref>` every commit not-reachable from *commit*
* `<first range> <second range>` intersection of commits in *first
  range* and *second range*


[Back to content index](Home.md) (Index)