---
tags: [bash]
title: bash environment
created: '2019-07-30T06:19:48.998Z'
modified: '2020-01-17T07:50:43.073Z'
---

# bash environment

## usage
```sh
shopt -p                # show alle options

( set -o posix ; set ) | less   # set shows all shell variables (exported or not); -o posix => only variables
```

## see also

- [[bash shopt]]
- [[bash set]]
- [[bash debugging]]
- [[bash declare]]
- [What is the difference between 'env' and 'printenv' ?](https://unix.stackexchange.com/questions/123473/what-is-the-difference-between-env-and-printenv)
