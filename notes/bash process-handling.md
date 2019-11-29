---
favorited: true
tags: [bash]
title: bash process-handling
created: '2019-07-30T06:19:49.016Z'
modified: '2019-08-29T12:27:04.882Z'
---

# bash process-handling

## bash option enable/disabe job-control
`set -o monitor / set -m`


## move to background
> to suspend a job, type `CTRL+Z` while it is running. You can also suspend a job with `CTRL+Y`. This is slightly different from `CTRL+Z` in that the process is only stopped when it attempts to read input from terminal. Of course, to interupt a job, type `CTRL+C`
```sh
myCommand &     # runs job in the background and prompts back the shell
```

## see also
- [[bash jobs]]
- [[bash fg]]
- [[bash bg]]
- [[bash disown]]
- [[bash wait]]
- [[bash set]]
- [Job Control Commands](http://tldp.org/LDP/abs/html/x9644.html)

