# Database Concepts Notes

These are some important database concepts that help in understanding how databases work and how to write better queries and design better systems.

---

## ACID Properties

ACID properties make sure that database transactions are safe and reliable.

**Atomicity**  
A transaction should complete fully or not happen at all. If something fails in between, all changes are undone.

**Consistency**  
After a transaction, the data should remain valid according to the rules and constraints.

**Isolation**  
Multiple transactions running at the same time should not affect each other.

**Durability**  
Once the transaction is committed, the data is saved permanently even if the system crashes.

---

## CAP Theorem

CAP theorem is important for distributed databases. It says that a system can provide only two out of these three:

- Consistency - all users see the same data
- Availability - every request gets a response
- Partition Tolerance - system works even if network failure happens

Most distributed systems choose between:
CP or AP

---

## Joins

Joins are used to combine data from multiple tables based on a common column.

Types of joins:

- INNER JOIN - only matching records
- LEFT JOIN - all records from left table + matching from right
- RIGHT JOIN - all records from right table + matching from left
- FULL JOIN - all records from both tables

Joins are very useful when working with relational data.

---

## Aggregations and Filters

Aggregation functions are used to perform calculations on data.

Common functions:
- COUNT()
- SUM()
- AVG()
- MIN()
- MAX()

Filters help to get specific data.

- WHERE - filters rows before grouping
- HAVING - filters after grouping

Example:
SELECT department, COUNT(*)  
FROM employees  
GROUP BY department  
HAVING COUNT(*) > 5;

---

## Normalization

Normalization is used to organize data and reduce duplication.

**1NF**
- No repeating columns
- Each field has a single value

**2NF**
- Must be in 1NF
- No partial dependency

**3NF**
- No dependency on non-key columns

Benefits:
- Less redundancy
- Better data integrity
- Easier updates

---

## Indexes

Indexes are used to make data retrieval faster.

Without index - database checks entire table  
With index - faster search

But too many indexes can slow down insert and update operations.

---

## Transactions

A transaction is a group of operations executed together.

Commands:
- BEGIN
- COMMIT
- ROLLBACK

Example: transferring money between two accounts.

If any step fails, the whole transaction should be rolled back.

---

## Locking Mechanism

Locking is used when multiple users access the same data.

**Shared Lock**
- Multiple users can read
- No writing allowed

**Exclusive Lock**
- Only one user can read/write
- Others must wait

Locks help maintain consistency but too many locks can reduce performance.

---

## Database Isolation Levels

Isolation levels control how transactions see each other’s data.

- Read Uncommitted - dirty reads possible
- Read Committed - only committed data is visible
- Repeatable Read - same data during transaction
- Serializable - highest level, transactions run one by one

Higher isolation means better consistency but slower performance.

---

## Triggers

Triggers are automatic actions that run when certain events happen in a table.

Events:
- INSERT
- UPDATE
- DELETE

Uses:
- Logging changes
- Auditing
- Automatic updates

Triggers are useful but should be used carefully because they can affect performance.

---

## Summary

These concepts help in building reliable and efficient database systems. Understanding transactions, indexing, normalization, and isolation levels is very important for backend development and database design.