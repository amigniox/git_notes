# Creating a Repository

## Creating a Repository

```
git init [<directory>]
```

* create empty repository in *directory* (default to *.*)

```
git clone [-o <remote name>] [-b <branch>] <url> [<directory>]
```

* clone existing repository *url* into *directory* (defaults to *url*)
* set remote *url* name to *remote name* (defaults to origin)
* checkout branch *branch* (defaults to *url*'s HEAD)

## Setting Configuration Options

Configuration is a combination of the global **~/.gitconfig** config
and respository specific **.git/config** config (the later overrides
the former).  Theses files are frequently easier to just edit than
using the following commands.

```
git config --list
```

* show all config option (combines local and global)

```
git config [--global] <option> [<value>]
```

* set config *option* to *value*

```
git config [--global] --unset <option>
```

* unset config *option*

### Config Options to Set

```
git config user.email "<email>"
git config user.name "<full name>"
git config core.editor "<editor>"
git config color.ui auto
```
