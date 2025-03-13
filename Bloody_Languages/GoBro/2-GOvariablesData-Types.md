---
title: "2-GOvariablesData-Types: GoBro"
date: "2025-03-12"
tags:
  - "GoBro"
  - "2-GOvariablesData-Types"
---

Broo, Go as any other language has several built-in data types👻

> **Basic types :**  `int, float64, string, bool`
> **Composite Types**: `array, slice, map, struct`
> **Reference Types**: `pointer, channel, function` 

Okayyy , now to define a variable GO provides us an keyword **var**.😪

```
#  Decleartion without initialization 
var name string # name has default val as ""
var age int # age has default val as 0

#  Decleartion without initialization
var name string = "My_Name"
var age int = 10
```

🙈GO got us an surprise Mannn, ***GO could even automatically infer the data type based on the value assigned to it..(Just like how python does)*** 🧑🏼‍🍳

*Is there a short-hand to declare and initialise variable without explicit mentioning of Data-type?* 🤡
- Yeahhhhh, we can use `=:` to declare and initialise a variable simultaneously 😯

```
#  Type Inference
var height = 5.9 // Type inferred as float64

#  Short-hand
message := "Hello, Go!" // key message declared & initialized to String
```

What if I have a value which will not change forever ? maybe I could call it a constant value ? 😑 
- Here comes the ***const*** keyword bruhhh. 😎
- This keyword can be used to declare constants which cannot be changed after declaration

