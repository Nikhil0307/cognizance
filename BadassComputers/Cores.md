---
title: "Cores: BadassComputers"
date: "2025-03-12"
tags:
  - "BadassComputers"
  - "Cores"
---

> ***CPU core is essentially a processing unit within a CPU which executes tasks***
> ***CPU may have multiple cores, allowing to perform multiple tasks simultaneously***

**Sushhhhh😮‍💨 what are multi core processors ??**
- As said in the intro, a single CPU can contain multiple cores, each capable of executing its own instructions *(Thread of instructions)*
- More the number of cores more multitasking can be performed

**Wkiesss !! What are threads in core ? 🧶**
- Each core can handle one or more threads in general.
- Basically in most of the CPU's every core would handle only a single thread.
- Considering Intel's Hyper-Threading technology, which allows a single core to manage two threads at a time

**CPU cores married to Cache!!!! 🤭 HAHA**
- Each core has its own cache.
- In general there are namely l1, l2, l3 cache. 
- Every core has its own l1 cache.
- Depending on the CPU l2 cache might also be coupled to a single core *(making it every core has its own l1 and l2 cache)*
- L3 cache is a shared cache which will be shared among cores of the CPU
- This can be simplified as the more the cache level increases size and latency increases linearly
- We can have these speeds with reference to cpu cycles

![[Cache_access_latency.png]]

`Note :: The above values varies with respect to processor models`
