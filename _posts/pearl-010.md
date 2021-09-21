---
layout: post
title: Pealr 010 - The Database Pearl
date: 210920
---
How can we store data:
 - in large volumes
 - so it does not get lost or corrupted
 - reliably available
 - durably
 - securely
 - robustly

Database (DB) resides on a database server.
DB is managed by database management system (DBMS).
End users controls applications, that query DBMS.

ANSI/SPARC architecture:
 - disks
 - physical schema
 - conceptual schema
 - external schemas
 - apps

Development process:
 - information analyst makes an entity-relationship (ER) model
 - database designer uses the DBMS to create the database
 - database admin manages the DB and allows accesses
 - application programmer queries the DB in the app

DB is made up of tables. Tables have attributes and records.

Key - collection of one or more attributes that determine a record in a table:
 - primary key - unique for every record, every table needs one
 - surrogate key - synthetic primary key
 - candidate key - minimal group of columns that uniquely identifies every entry
 - composite key - a key made up of more than one attribute
 - foreign key - a primary key from another table used to reference an entry

**Foreign key** is an attribute, that is a primary key in another table.

Redundant information in databases causes insertion and update issues.
This can be solved by splitting the table into


## SQL
SQL stand for Structured Query Language.

It is a data definition language (DDL) and data manipulation language (DML).

In relational databases operations take tables as inputs
and produce tables as outputs.

**Selection** reduces the number of rows.

**Projection** reduces the number of columns.

data query language (DQL) commands:
 - SELECT {DISTINCT} [columns] {AS alias} from [tables]
   - you can use multiple SELECT statements and join them with UNION {ALL}
 - WHERE [condition]
   - you can use logical operators AND, OR, NOT in the condition
   - you can also use IS NULL and IS NOT NULL
   - you can use [column] LIKE [pattern with wild cards % (any chars) and _ (1 char)]
   - you can use [column] IN [multiple values]
   - you can use [column] BETWEEN [value1] and [value2]
 - ORDER BY [columns] {ASC}/DES 
 - LIMIT [number]
 - [table1] [INNER / LEFT / RIGHT / CROSS] [table2] ON [condition]
   - you can join a table onto itself by FROM [table] t1, [table] t2
data manipulation language (DML) commands:
 - INSERT INTO [table]...
   - ...([columns]) VALUES ([values])
   - ...FROM [table2] WHERE [condition]
 - UPDATE [table] SET [column1=value1...columnn=valuen]
   - you can use WHERE after
 - DELETE FROM [table] WHERE [condition]

data definition language (DDL) commands:
 - CREATE [DATABASE/TABLE] [name] 
 - DROP [DATABASE/TABLE] [name] 
 - ALTER TABLE [name]...
   - ... ADD COLUMN [name] [data type]
   - ... DROP COLUMN [name]
   - ... MODIFY COLUMN [name] [data type] [constraint]
 - TRUNCATE 

functions:
 - SELECT FUNCTION([column]) FROM [table] WHERE [condition]
 - MIN
 - MAX
 - COUNT
  - can also be used 
  SELECT [column] count(id) FROM [table] GROUP BY [column]
 - AVG
 - SUM
 - IFNULL

 other syntax:
  - CASE  
    WHEN condition1 THEN result1  
    WHEN condition2 THEN result2  
    WHEN conditionN THEN resultN  
    ELSE result  
END;  
 - comment with $-\ -$ (double-dash) for single line
 and /* ... */ for multi line
 - arithmetic operators: +, -, *, /, %
 - comparisons: =, >, <, >, >=, <=, <>
 - logical operators:
   - ALL, SOME/ANY, EXISTS
   - IN, BETWEEN, LIKE
   - AND, OR, NOT

## Constraints
 - specified when the table is created or altered  
 
```
CREATE TABLE [name] (  
    [column 1] [datatype] [inline constraint], 
    [column 2] [datatype] [inline constraint],  
    ...  
    [separate line constraint]
    [separate line constraint]
    ...
);
```

 - inline constraints:
   - NOT NULL
   - DEFAULT [value]
 - separate line constraints
   - UNIQUE ([columns])
   - PRIMARY KEY ([columns])
   - FOREIGN KEY ([columns]) REFERENCES [foreign table]([foreign key])
   - CHECK
   - CREATE INDEX
