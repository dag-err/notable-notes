---
tags: [go]
title: go maps
created: '2019-07-30T06:19:49.068Z'
modified: '2019-08-20T07:22:54.438Z'
---

# go maps


### initializing

```go
val a m[string]string

b := map[string]string        // initializes values

c := make(map[string]string)  // initializses capasity
```

```go
make ( map[string]int )
//        └───┬──┘
//   must be comparable wiht `==`
```
