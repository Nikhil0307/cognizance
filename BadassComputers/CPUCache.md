---
title: "CPUCache: BadassComputers"
date: "2025-03-12"
tags:
  - "BadassComputers"
  - "CPUCache"
---

> As we know, every core has cache dependent to the specific core *(namely l1 and l2 in below diagram)* and all cache share an common cache *(namely l3 in below diagram)*

![[CPU_cache_architecture.png]]

Okeyyyy !! now we are getting into the weeds of processor's world 🌍 ..... looks funny nahh 😆

>there is an important concept called as **locality of reference**. When a processor accesses a particular memory location, it is like :
- *It will access the same location in the near future; called as **temporal locality principle***
- *It will accesses the nearby memory location; called as spatial locality principle*** 

Temporal locality principle is one of the reason to have CPU caches. Though how processor leverages spatial locality bro ? *Instead of copying a single memory location to the CPU caches, the solution is to copy a **cache line***

*What is a **cache line** ???* 
- *Cache line is a contiguous segment of memory*
- *Each cache level specifies its own size of cache line*
- *Considering our l1 cache has cache line of size 64 bytes, making it copying contiguous segment of 64 bytes instead of copying a single memory location or variable*
- We can go through an example to get a clean understanding

```
𐁘 As we might already gone through the size of int64 which is 8 bytes
Lets consider a slice of int64 in GO with few number of elements in it.
Now instead of storing a single int64 val in memory which is 8 bytes, we can store 8 bytes * 8 value-> 64 bytes in memory ... i.e a cache line
```


***Cache line miss??***
***False sharing ???***

