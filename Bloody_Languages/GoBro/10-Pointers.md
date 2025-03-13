---
title: "10-Pointers: GoBro"
date: "2025-03-12"
tags:
  - "GoBro"
  - "10-Pointers"
---

Wheyyyyyyy, GO supports Pointers 😋

Just like in C we can get the address of a variable with `&` and `*` for a pointer

```
package main
import "fmt"

func deReference(mem_address *int){
	*mem_address = 0
}

func main(){
	i:=1
	fmt.Println("initial:", i)
	deReference(&i)
	fmt.Println("After:", i)
}
```
