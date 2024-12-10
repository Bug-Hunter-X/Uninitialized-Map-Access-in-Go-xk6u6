# Uninitialized Map Access in Go

This repository demonstrates a common error in Go: accessing an uninitialized map.  Attempting to access a key in a map that hasn't been initialized will result in a runtime panic.

The `bug.go` file contains code that reproduces this error. The `bugSolution.go` file shows how to correctly initialize the map to prevent this issue.

## How to reproduce the bug:

1. Clone this repository.
2. Run the `bug.go` file: `go run bug.go`

You should see a runtime panic like this:

```
panic: runtime error: map index out of range
```

## Solution:

The solution is to initialize the map before accessing its elements. The `bugSolution.go` file demonstrates this by creating a map using `make(map[string]int)`. 