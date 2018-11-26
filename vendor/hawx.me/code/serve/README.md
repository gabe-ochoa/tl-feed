# servers-gonna-serve [![docs](http://godoc.org/hawx.me/code/serve?status.svg)](http://godoc.org/hawx.me/code/serve)

A small package that wraps up serving a `http.Handler` via a port or socket. It
catches interrupts so any `defer`s will run properly.

``` go
package main

import (
  "hawx.me/code/serve"
  "net/http"
  "flag"
)

var (
  port   = flag.String("port", "8080", "")
  socket = flag.String("socket", "", "")
)

func main() {
  flag.Parse()

  http.HandleFunc("/", func(w http.ResponseWriter, r *http.Request) {
    // ...
  })

  serve.Serve(*port, *socket, http.DefaultServeMux)
}
```
