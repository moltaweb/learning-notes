# SQL ESSENTIAL TRAINING

INTRODUCTION

What is SQL?

SQL can be divided into 2 major categories

DDL, Data Definition Language
Define tables, indexes and relationships

DML, Data Manipulation Language
Add, query, manipulate and delete data from tables and datasets

SQL is designed to work with Relation databases. A Relation database is a data store capable of representing relationships between different sets of data, in the form of tables

    A table is a collection of rows (records) and columns
    A database is a collection of tables, plus other metadata like 
        indexes, 
        triggers and 
        stored procedures
    A DBMS (SGBD) is a DB management system


SQL will be found in 2 contexts:
- directly in a SW interface to query the DB provided by the vendor (ex Sybase)
- embedded in another lnguage to query the DB within the flow of the program


Each DBMS has its own implementation of SQL. Learning generic SQL will give us the base, but we may need afterwards to learn the specificites of the DBMS we use.




SQL Quick Start

    Quick Start Introduction


SELECT : statement to get data out of the DB
INSERT: add data to a table
UPDATE : modify values existing
DELETE: remove rows from a table
SELECT COUNT() : count howmany rows


    Using the basic SELECT statement


SELECT * FROM table

By default, SQL does not guarantee that data is returned in a specific order unless we specify the order. So, depending on the system, the order may be different.

The asterisk determines ALL COLUMNS. We can specify them:

SELECT col1, col2 as 'Second Column' FROM table


    Selecting rows


We can select just the rows we are interested in

SELECT Name, Continent, Region FROM Country WHERE clause

The WHERE clause uses a condition to determine which rows to return

We can also limit the output:
SELECT Name, Continent, Region FROM Country WHERE clause LIMIT 10


    Selecting columns


Selecting particular columns is easy:

SELECT col1, col2,..., colN FROM table


    Counting rows


SELECT COUNT(*) FROM table WHERE clause


    Inserting data


INSERT INTO table (col1, col2, col3, col4) VALUES (val1, val2, val3, val4)

If we do:
INSERT INTO table (col1, col3, col4) VALUES (val1, val3, val4)

--> it will insert NULL in col2

NULL is a special value in SQL. It's a lack of data. It's different from Zero or Zero-length string


    Updating data


UPDATE table SET col1 = val1, col2 = val2, col3 = val3  WHERE condition


    Deleting data


Before Deleting anythng, it's recommended that we use SELECT to make sure we see only what we want to delete

DELETE FROM table WHERE condition

--> delete entire rows





Fundamentals


Databases and tables

A database is a collection of tables, and eventually other metadata (indexes, triggers, stored procedures)

A table is a collection of data organized in rows and columns
Normally a table is a collection of related things, like countries, customers, etc
Tables may also have relationships with other tables (Customers with Orders, for instance)

Typically, one application uses one database. Not always the case, though



SQL Syntax overview

SQL is a standard language for describing relational databases and queries

It's an ANSI standard that has been updated many times. Therefore, most SQL vendors implement slightly different versions (some legacy code that predates the standards), and none of them fully comply with the standard

We will have to learn the specificites of the DBMS we are working with. 
Here we learn core features of SQL that are common to all implemntations. Still, some specific datatypes and so on may be different in each system.

SQL statements:

    Are not case-sensitive
        Table and field names depend on DBMS settings
    must be ended with semi-colon
    Comments start with "--"
    Long comments /* ...... */  (not available in all DBMS)


While the SQL syntax is simpl, we can create very complex statements



Formatting SQL

Format is not important as the SQl engine interprets OK

It's a matter of style and readability

Advice: Start lines with keywords



Creating tables

CREATE TABLE TableName (
     a INTEGER,         -- this is called
     b TEXT               -- the schema
);



Deleting a table with DROP TABLE

DROP TABLE TableName

We can add an If clause;

DROP TABLE IF EXISTS TableName



Inserting rows into a table

INSERT INTO table VALUES (val1, val2, val3, val4)       -- all columns

INSERT INTO table (col1, col2, col3, col4) VALUES (val1, val2, val3, val4)     -- specific columns


Insert from another table:

INSERT INTO Table1 SELECT col1, col2, col3 FROM Table2



Deleting rows from a table

DELETE FROM table WHERE condition

This statement is destructuve: Always perform first the same statement replaceing "DELETE" with "SELECT *"



Understanding NULL

NULL is a special state in SQL. It's the lack of value

Normally we cannot do a condition like this:

WHERE a = NULL

since NULL is not a value, so cannot be equal to a

--> use "IS NULL" or "IS NOT NULL"



Controlling column behaviors with constraints

CREATE TABLE TableName (
     a INTEGER,         -- NOT NULL
     b TEXT               -- DEFAULT 'text_default'
     b TEXT               -- UNIQUE
);

    NULL / NOT NULL
    DEFAULT 'default_value'
    UNIQUE --> not allow repeated values


--> depends on DBMS


Changing a schema with ALTER

ALTER TABLE tables ADD NewCol DATETYPE

--> depends on DBMS



Creating an ID column

The method varies from every DBMS

In SQLite:

CREATE TABLE TableName (
a INTEGER PRIMARY KEY
b TEXT,
c TEXT
);



Filtering data with WHERE, LIKE, and IN

WHERE to lkmit values that verify a Boolean condition. Can is AND or OR

LIKE to select values that match some pattern
% any string
_ any character

IN to select values in a list between parenthesis


Removing duplicates with SELECT DISTINCT

Powerful tool to remove duplicates, either from a single column or multiple columns

Most engines work by first ordering the results, then removing the duplicates. Therefore the output is generally sorted


Sorting with ORDER BY

ORDER BY col1, col2, etc.


Conditional expressions with CASE

Shitty examples, do not bring anything



Relationships


Understanding Joins

    JOIN = INNER JOIN
    LEFT JOIN
    RIGHT JOIN

Not all DBMS implement all. For example SQLite does not implement RIGHT JOIN


Accessing related tables with JOIN

JOIN by default is = INNER JOIN
--> rows that match in both tables

LEFT JOIN by default = LEFT OUTER JOIN
--> rows in the felt

    like INNER JOIN if match in both tables
    + rows where not in right table are nulls



Using multiple related tables

It's very common to have many to many relationships btw tables

The ideal case is to have foreign keys in every table to have relationships with JOIN







Strings


About SQL strings

Standard SQL: String between ' '
Some accept " " but that is not standard
Escape wit double ' : 'Here''s a string'

Each DBMS tends to treat concatenation in a different way:

    SELECT CONCAT('string A','string B')
    SELECT 'string A' + 'string B'
    SELECT 'string A' || 'string B'
    Etc



Finding the length of a string

Standard SQL does not include a function for Length, but most DBMS implement it anyway, usually called LENGTH or LEN
Check DBMS doc



Selecting part of a string

Standard SQL does not include a function for Substring, but most DBMS implement it anyway, usually called SUBSTRING or SUBSTR
Check DBMS doc



Removing spaces with TRIM

Remove spaces or other characters from the beginning and end of srings

SELECT TRIM()
SELECT RTRIM() - for Right trim
SELECT LTRIM() - for Left trim
SELECT TRIM('...string....', '.') -> 'string'
Check DBMS doc



Making strings lowercase and uppercase

SELECT UPPER('StrIng') --> STRING
SELECT LOWER('StrIng') --> string
Check DBMS doc




Numbers


About numeric types

SQL datatypes are totally platform-dependent
We should always check the doc of our DBMS



Finding the type of a value

In SQLite: SELECT TYPEOF()
Check DBMS doc



Integer division and remainders

SELECT (17.0 / 5.0), 17 % 5
Check DBMS doc



Rounding numbers

SELECT ROUND()
Check DBMS doc






Dates


Dates and times

These datatypes have specific properties
They can be used for chronology and duration, and also for internal DB uses

Typical SQL datetime format is:
YYYY-MM-DD HH:MM:SS

Internally, SQL systems usually work with UTC times (Reykjavik, Iceland - Greenwich w/o summertime adjustments))

Typical types:

    DATE
    TIME
    DATETIME
    YEAR
    INTERVAL

Typical functions:

    DATE()
    TIME()
    DATETIME()
    STRFTIME()



Date- and time- related functions in SQLite

Check other DBMS doc

SELECT DATETIME('now')
SELECT DATETIME('now', '+1 month', '-3 years')




Aggregates


How aggregates work

Aggregate data is information dervied from more than one row at a time

The GROUP BY clause groups results before calling the aggregate function for this group

It also works on JOIN queries

To limit the output of the query we use HAVING. It's like WHERE, but for aggregate data



Using aggregate functions

SQL provides a number of functions to work on aggregate values:

    COUNT
    AVG
    MIN
    MAX
    SUM



Aggregating DISTINCT values

SELECT COUNT(DISTINCT column) FROM table

DISTINCT can be used with all the aggregate functions




Transactions


Why use transactions?

A transaction is a group of operations handled as one unit of work. If any operation fails, the entire group is treated as failed and rollback

START TRANSACTION
     statement 1
     statement 2
     statement 3
END TRANSACTION

We can also use ROLLBACK

Furthermore, transactions improve performance in the DB instructions, because the DBMS does not have to confirm that every individual operation has been performed successfully, just 1 confirmation in the end.



Using transactions

2 uses of transactions:

    ensure integrity of the database
    increase performance





Triggers


Updating a table with a trigger

Triggers are operations that are performed when a specific event occurs

A common use is to force an update in a table when a row is inserted in another table

Specific management depends on DBMS

Example in SQLite: 

CREATE TRIGGER TriggerName AFTER INSERT ON table1
     BEGIN
          UPDATE table2 SET last_id = NEW.id where table.id = NEW.table_id
     END



Preventing automatic updates with a trigger

Triggers nay also be used to prevent changes to rows that have already been reconciled or should not be changed for any reason

Example in SQLite: 

CREATE TRIGGER TriggerName BEFORE UPDATE ON table1
     BEGIN
          SELECT RAISE(ROLLBACK, 'cannot update table1') FROM table1
               WHERE id=NEW.id AND reconciled=1
     END

REAISE function can only be used inside triggers. It signals the DB to do sthg specific



Automating timestamps with a trigger

Triggers can also be used to create timestamps




Subselects and Views


Creating a simple subselect

Subselects are nested SELECT statements. A select statement may be used as a data source in another select statement

The idea is that a select statement gives a result that may be a table. With that result table, we construct another select:

SELECT subquery.whatever FROM (SELECT blablabla) AS subquery



Searching within a result

Example:

SELECT * FROM album WHERE id IN ( SELECT DISTINCT id FROM track WHERE duration <= 90 )



Creating a view

In SQL we can save a query as a view

Example:

CREATE VIEW trackView AS
     SELECT id, album_id, title, track_number, duration / 60 AS m, duration % 60 AS s FROM track

and we can then do

SELECT * FROM trackView

to delete the view:

DROP VIEW trackView



Creating a joined view

A view can be a simple query or a complex join query. The technique is the same




A Simple CRUD Application


Touring the CRUD application

This is a PHP application that updates a DB table through a web form



The SELECT functions

Shows how the SELECT queries are inserted in the PHP code



The INSERT, UPDATE and DELETE functions

Shows how the INSERT, UPDATE and DELETE queries are inserted in the PHP code

