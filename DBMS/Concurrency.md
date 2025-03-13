---
title: "Concurrency: DBMS"
date: "2025-03-12"
tags:
  - "DBMS"
  - "Concurrency"
---

As we might know, a database is not meant for a single transaction execution
Lets take an example to get a clear view
considering our database is a banking transaction database, where every money transaction across accounts happens as dbms transactions ... [To know why this case happens as a database transaction and not as a simple query execution??](obsidian://open?vault=Fu*king%20banged%20%F0%9F%91%80&file=DBMS%20%F0%9F%AB%99%F0%9F%92%BF%2FTransactions%20%F0%9F%9A%80)

>So our banking database doesn't have only one customer, we will having N number of customers and these customers might transfer money across accounts simultaneously -> making the database to run multiple transactions simultaneously.

Concurrent execution refers to the simultaneous execution of multiple transactions in a db. However, concurrent executions can introduce various challenges and issues such as :
- ***Dirty Reads:*** A transaction might read uncommitted data from another transaction which is yet to be committed. If the other transaction is aborted, the read data made will become inconsistent 🧟
- ***Lost Updates:*** When two or more transactions tries to update the same data simultaneously, one transactions update might be overridden by other transaction update, again leading to data inconsistency 😩
- ***Non-Repeatable reads:*** Consider reading a particular data multiple times within a single transaction, whereas at the same time various other transactions might commit which might have changed the data. So, our transaction that has reading a data multiple times might be inconsistent or un predictable results. 🔁

>There are few mechanisms known as concurrency control mechanism which are employed to address the above challenges and ensures that transactions are executed in order and there will be no inconsistency between data. Some common techniques are below :

1) ***Locking:*** Transaction acquires lock on data items to prevent other transactions from accessing or modifying the same data concurrently
	1) ***Exclusive Locks (X-Locks):*** A transaction holds an exclusive lock on a data item when it wants to modify it, while other transactions will be prevented from reading or writing to the locked data item until the lock is released.
	2) ***Shared Locks (S-Locks):*** This lock will be held on a data item by multiple transaction simultaneously for reading purposes. At the same time, E-Lock could not be made on the data item with shared lock
	3) ***Two-Phase Locking (2PL):*** As the name of the lock says, a Transaction is said to acquire all the necessary locks before starting the execution phase and release all the locks after completion of execution. This prevents conflicts among transactions
2) ***MultiVersion Concurrent Control (MVCC):*** Instead of locking data items, MVCC maintains multiple versions of a data time to allow concurrent transactions to read consistent snapshots of the database without blocking other transactions
	1) Read operations retrieve the appropriate version of the data based on the transaction's timestamp or snapshot isolation level.
	2) Write operations create a new version of the data item, ensuring that read operations from other transactions remain unaffected.
3) ***Timestamp Ordering:*** Transactions are assigned timestamps, and the system ensures that transactions are executed in order of their timestamps to maintain consistency and prevent conflicts.
4) ***Optimistic Concurrency Control:*** Transactions are allowed to proceed without acquiring locks initially, and conflicts are detected and resolved at commit time. If conflicts occur, one or more transactions might get aborted and restarted.
>By employing the above concurrency control techniques, database systems can ensure that concurrent execution of transaction maintain data consistency and integrity while *maximising systems throughput and responsiveness*


