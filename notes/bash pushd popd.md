---
tags: [bash/built-in]
title: bash pushd popd
created: '2019-08-02T06:42:37.617Z'
modified: '2020-01-27T07:49:34.934Z'
---

# bash pushd popd

## usage
```sh
pushd /opt/path/logs    # switch to path and put on the stack

pushd +2                # bring the 3rd directory on the stack to the front (0-based) and rotating the stack


pushd $(mktemp -d)

popd
```

## see also
- [[bash dirs]]
- [[mktemp]]
