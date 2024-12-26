# Go: Panic on nil map access

This repository demonstrates a common Go error: panicking due to accessing an uninitialized map.  Uninitialized maps are `nil`, and attempting to use the indexing operator (`m["key"]`) on a `nil` map results in a runtime panic.

The `bug.go` file contains the buggy code, while `bugSolution.go` provides a corrected version.

## Bug

The core issue lies in the `main` function of `bug.go`. The map `m` is declared but not initialized, therefore it's `nil`. The line `m["a"] = 1` attempts to assign a value to a key in this `nil` map, triggering a panic.

## Solution

`bugSolution.go` addresses this by initializing the map before use.  This prevents the panic and ensures the code runs correctly.