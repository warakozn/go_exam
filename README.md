Create a module for your code
=============================
$ mkdir workspace
$ cd workspace

$ mkdir hello
$ cd hello
$ go mod init example.com/hello
go: creating new go.mod: module example.com/hello

Add a dependency on the golang.org/x/example module by using go get.
$ go get golang.org/x/example

Create hello.go in the hello directory with the following contents:
```
package main

import (
    "fmt"

    "golang.org/x/example/stringutil"
)

func main() {
    fmt.Println(stringutil.Reverse("Hello"))
}```




Create the workspace
===================

Initialize the workspace
In the workspace directory, run:

$ go work init ./hello

Run the program in the workspace directory
In the workspace directory, run:

$ go run example.com/hello



Download and modify the golang.org/x/example module
$ git clone https://go.googlesource.com/example

Add the module to the workspace
$ go work use ./example