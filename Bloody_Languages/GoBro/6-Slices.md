---
title: "6-Slices: GoBro"
date: "2025-03-12"
tags:
  - "GoBro"
  - "6-Slices"
---

***Slices_ are an important data type in Go, giving a more powerful interface to sequences than arrays.***

Unlike arrays, slices are typed only by the elements they contain. An unintialized slice equals to `nil` and has length as `0`

To create an empty slice with non-zero length, we can use the built in `make`.we will make a slice of strings of length 2(initial value will be 0) as  `s = make([]string, 3)`

We can assign values to slice just like in arrays

Slice supports append operation, where we can append one or more items to slice 
```
s := make([]string, 3)
s[0]="a"
s[1]="b"
s[2]="3"

s = append(s,"d")
s = append(s,"e","f")
```
Did you note a thing ???👀
- we initiated a slice of length 3 but added more elements to it ??
	- Yeessss,If slice grows ,it's possible to add new elements.

> Slice supports the operations known as *`slicing in python`*


