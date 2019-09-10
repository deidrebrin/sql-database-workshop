---
title: "Interact with the Data"
teaching: 20
exercises: 0
questions:
- "How do I query data using SQL?"
- "How do I make changes to the data using SQL?"
objectives:
- "Understand basic SQL statements and what sources to reference."
keypoints:
- "SQL statements provide powerful ways of viewing and interacting with your data."
---


## SELECT statements (queries)
* SELECT is how you grab data from the tables in your database and display the results. You can view entire tables, specific columns, and subsets determined by simple or complex queries.

**Wildcards**
* Allow you to substitute one or more characters in a string for the wildcard
    * List of wildcards available [here](https://www.w3schools.com/sql/sql_wildcards.asp)

~~~
SELECT * FROM burials
~~~
{: .sql}

## Applying conditions 

~~~
SELECT burial_id, type
FROM burials
WHERE type=‘Tomb’
~~~
{: .sql}

## Applying multiple conditions (AND/OR/NOT)

~~~
SELECT burial_id, type
FROM burials
WHERE type=‘Tomb’ AND burial_id=‘B3'
~~~
{: .sql}

## Making changes

~~~
UPDATE burials
SET type=‘Pit’
WHERE burial_id=‘B3'
~~~
{: .sql}

## Joins 
Let’s check if all of the burial_ids have been entered in the finds table and produce a quick visual of find types and burial types.

~~~
SELECT * FROM finds //see number of results
~~~
{: .sql}

~~~
SELECT finds.find_id, finds.type, burials.type
FROM finds
INNER JOIN burials ON burials.burial_id=finds.burial_id
~~~
{: .sql}

### Join types
* (INNER) JOIN: Returns records that have matching values in both tables
* LEFT (OUTER) JOIN: Returns all records from the left table, and the matched records from the right table
* RIGHT (OUTER) JOIN: Returns all records from the right table, and the matched records from the left table
* FULL (OUTER) JOIN: Returns all records when there is a match in either left or right table

[Visual depiction of the different types of joins](https://www.w3schools.com/sql/sql_join.asp)