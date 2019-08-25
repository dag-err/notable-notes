---
tags: [go]
title: go methods
created: '2019-07-30T06:19:49.068Z'
modified: '2019-08-20T07:22:54.439Z'
---

# go methods

> Go does not have `classes`. However, you can define `methods` on types.
> A method is a `function` with a special receiver argument. 

```go
type Vertex struct {
	X, Y float64
}

func (v Vertex) Abs() float64 {
	return math.Sqrt(v.X*v.X + v.Y*v.Y)
}

func main() {
	v := Vertex{3, 4}
	fmt.Println(v.Abs())
}
```

```go
func (h handler) ServerHttp (w http.Response, ...) {..}
//   └────┬───┘
//     reciever: (h handler) = h.ServeHttp(w, ..)

func (h handler) ServeHttp () {} // method on value

func (h *handler) ServeHttp () {} // method on pointer; pointer modifies reciever
```
