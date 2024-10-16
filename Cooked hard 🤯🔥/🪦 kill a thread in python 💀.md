*GIL releases thread either during an i/o operation or when executions are under cpython👀🔥*

While multithreading Killing a python thread sucks as it may lead to dreadlock , issues on release of memory🏃

##### Things to consider 📍
> thread might hold abrupt of resource😵
> thread creates multiple other threads🪡🪡
> thread is killed when under a lock✂️🔗

##### ways to handle a thread 🪡 
> Flags🏴‍☠️
> Join with timeout🤞🏻
> Using a daemon thread🧑‍🧒

##### Best practices for handling a thread ♾️
> Avoid sharing state🦈
> Shouldn’t forget to Join✔️
> avoid too many threads (Creates over-head to handle many threads)🤯


