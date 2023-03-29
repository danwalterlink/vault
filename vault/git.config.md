---
id: xr93cdqoqz6le5cw65otu1i
title: Config
desc: ''
updated: 1676623923369
created: 1665768522736
---

default config:

pull in aliases from:
/Users/grimnir/.config/git/alias/gitalias.txt

in git config --global (~/.gitconfig)
add :
```gitconfig
[path]
  ~[[gitalias]]
```

git templates signing
-> branch protection

dotfile repo
  root dir : starting with .
    but otherwise same name as branch
    and origin.url contains ddubl
    -> current feature branch follows remote ddubl/^.(BRANCHNAME)
    HEAD pointing to

    experimental config
      submodule.propagateBranches = true
        enabling branch support in submodules :
      submodule.recurse = true