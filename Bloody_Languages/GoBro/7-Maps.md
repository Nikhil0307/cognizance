---
title: "7-Maps: GoBro"
date: "2025-03-12"
tags:
  - "GoBro"
  - "7-Maps"
---

To create an empty map, use the builtin `make`: `make(map[key-type]val-type)`
Map is a package which needs to be imported as `import "maps"`
> We can set key value pairs as like in python

```
m := make(map[string]int)
m["key1] = 3
m["key2] = 12
```

>We can get a value of a key with `m["key2]`

- `Delete(m, "key1")` will remove the particular key value pair from map
- To remove all key value pair `clear(m)` can be used
-  map can be declared and initialized as `new_map := map[string]int{"foo": 1, "bar": 2}`

maps can also be created as below 
```
m := map[int]int{}
```

To check if a key is in map we can proceed as below 👇

```
pairs := map[int]int{}
pairs[10] = 1
pairs[11] = 2

value,status := pairs[10]

# status above will be true if the key is present else false
```
