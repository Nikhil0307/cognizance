In context of databases, a transaction is a logical unit of work that might consist of one or more database operations such as insert, update, delete.
These operations are grouped together as a single entity or a unit, where either all of the operations will succeed or none of them are executed at all.

>*It is said that a database transaction will be atomic, consistent, isolated and durable ... making transaction follows ACID principle*

How Transaction will be known for ACID??? 💩
- ***Atomicity:*** A transaction is atomic as it either completes executing all the operations and commits it to the database or it  leaves things unchanged in database in case of failure(*No partial execution of operations are made to database*).
- ***Consistency:*** A transaction to a database is consistent as transaction ensures that the database moves from one state to another state.
- ***Isolation:*** Transactions are isolated from others, making it that the intermediate state of the transaction is not visible to others until transactions is committed. This also ensures that transaction execute as if they were the only transaction running over the database.
- ***Durability:*** Once the transaction is committed, the changes made by the transaction are permanently persisted in the database, these changes are not lost even in the event of system failure (or an alien attack 🛸 🤭)

```
BEGIN TRANSACTION;

UPDATE accounts 
SET balance = balance - 100 
WHERE account_id = 123;
INSERT 
INTO transactions (account_id, amount, type) VALUES (123, -100, 'Withdrawal');

COMMIT;
```

