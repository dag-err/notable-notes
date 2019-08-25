---
tags: [container/docker, linux, packagemanager]
title: linux apk
created: '2019-07-30T20:26:52.476Z'
modified: '2019-08-22T08:31:36.292Z'
---

# linux apk

> Software packages for `Alpine Linux` are digitally signed `tar.gz` archives containing programs, configuration files, and dependency metadata. They have the extension `.apk`, and are often called `"a-packs"`

```sh
apk info    # list installed

apk add --no-cache package  # install package
```

### unsatisfiable constraints
if package is only available in edge alpine repo, not in a stable one
```sh
echo "http://dl-cdn.alpinelinux.org/alpine/edge/testing" >> /etc/apk/repositories
```

## see also
- [wiki.alpinelinux.org](https://wiki.alpinelinux.org/wiki/Alpine_Linux_package_management)
- [docker-alpine :: viewdocs.io](http://gliderlabs.viewdocs.io/docker-alpine/)
- [BusyBox - The Swiss Army Knife of Embedded Linux](https://busybox.net/downloads/BusyBox.html)
- [ERROR: unsatisfiable constraints using apk in dockerfile - Stack Overflow](https://stackoverflow.com/a/48893148)


