---
tags: [bash/keyword]
title: bash while
created: '2019-07-30T06:19:49.024Z'
modified: '2020-01-27T07:28:58.764Z'
---

# bash while

> Execute commands as long as a test succeeds.

## usage
```sh
while condition; do statements done


command | while read foo; do
  echo $foo
done


while read; do eval echo "$REPLY"; done < config.yml
```

## see also
- [[watch]]
- [[bash read]]
