# ACID Compliance Lesson

## Learning Goals

- Guarantees of ACID Compliant DB Systems

## Introduction

Crashing applications can be patched and stabilized, failing hardware can be fixed or replaced, but lost or corrupted data is gone for good. And depending on the criticality of the data, might lead to a resume updating event.

Relational database systems tend to be used as a root source of truth, therefor they predominately favor data preservation and reliability over performance.
These guarantees and drawbacks may not be readily apparent for most developers, but as complex applications start hitting performance and scale bottlenecks, these DB design considerations start needing to be taken into account
in the application design.

Most if not all serious RDBMS adhere to what is known as ACID compliance to provide for this data security.
And compromises in this area for better performance is one of the larger differences between RDBMS and NoSQL systems.

## Guarantees of ACID Compliance

The problem of data preservation is quite complex. It ultimately spans the full realm of Computer Science, Software Engineering, Hardware Engineering, IT, and Operations.
At the highest level we could visualize a full stack of correctly implemented and redundant applications and systems to correctly preserve the complex layout of data, on what essentially works out to be magnetized sections on spinning disks.
And if enough components in that chain fail, core business data could be irretrievably lost.

The Database software implements the Database transactions in such a way that data integrity and preservation is maximized. However, given the above, there is only so much that can be done at this layer to support this goal. 

Read through the following documentation to get a better understanding of what ACID compliance is, and how Postgres implements this.

- [ACID Overview](https://mariadb.com/kb/en/acid-concurrency-control-with-transactions/)
- [Postgres Transactions](https://www.postgresql.org/docs/current/transaction-iso.html)
- [Postgres Constraints](https://www.postgresql.org/docs/current/ddl-constraints.html)
- [Postgres Reliability](https://www.postgresql.org/docs/current/wal-reliability.html)
