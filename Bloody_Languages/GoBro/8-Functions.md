---
title: "8-Functions: GoBro"
date: "2025-03-12"
tags:
  - "GoBro"
  - "8-Functions"
---

As seen previously we can create a function with `func` keyword

*Functions are the central in GO*

Functions can take input as `func add(a int , b int){return a+b}`

Now, in the above example both a and be have same data type , meaning same consecutive type params *we can skip explicitly mentioning every D-type instead the final one mentioned will be applicable to all* . Example below 
```
func add(a , b, c int){
	return a+b+c
}
```

Return type of the function can be declared before the curly braces as  below 
```
func add(a , b, c int) int{
	return a+b+c
}
```

functions can have multiple return values be mentioned as below
```
func addsub(a, b int) (int,int){
	return a+b, a-b
}
```

Functions can also take any number of params with ... such as `func sum(nums ...int){}`