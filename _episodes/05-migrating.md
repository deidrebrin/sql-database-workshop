---
title: "Migrating Data"
teaching: 15
exercises: 1
questions:
- "How do I migrate data from FileMaker Pro to MySQL?"
- "How do I create tables, primary keys, and foreign keys using SQL?"
objectives:
- "Understand how to get data out of one system and into another using your data model"
- "Learn how to use SQL to quickly build structure and import data"
keypoints:
- "Migrating data potentially introduces errors and requires careful attention." 
---

## Migrate data and learn basic SQL
A handful of the projects explicitly called out that they were using MySQL or content management systems like Wordpress/Drupal which utilize MySQL. Let’s get familiar with SQL by migrating the data we collected in FileMaker to MySQL! 

We'll use the popular tool **phpMyAdmin** to write and execute SQL queries. phpMyAdmin is a free tool used to interact and administer MySQL. It provides an interface to conduct certain operations but also allows users to directly execute SQL. 

> ## Challenge
> Export data out of FileMaker Pro and import into MySQL
>
> > ## Solution
> > 1. Create table statement, add columns, datatypes
> > 2. Set up primary and foreign keys
> > 3. Add data!
> {: .solution}
{: .challenge}

> ## Datatypes
> The types of characters that are stored in a column, impacts how the database is able to interact with the data in those columns and how much can fit.
> Considerations
> * If your primary key contains text characters use VARCHAR(max size of values)
> * Sorting (think numeric vs alphabetical, leading zeros)
> * Different systems support different datatypes (SQLite vs MySQL)
> 
{: .callout}

## Breakdown of the process
1. Create table statement, add columns, datatypes

~~~
CREATE TABLE burials (burial_id VARCHAR(2), type TEXT)
~~~
{: .sql}

~~~
CREATE TABLE finds (find_id VARCHAR(2), burial_id VARCHAR(2), type TEXT)
~~~
{: .sql}

2. Set up primary and foreign keys

~~~
ALTER TABLE burials
ADD PRIMARY KEY (burial_id)
~~~
{: .sql}

~~~
ALTER TABLE finds
ADD PRIMARY KEY (find_id)
~~~
{: .sql}

~~~
ALTER TABLE finds
ADD FOREIGN KEY (burial_id) REFERENCES burials(burial_id)
~~~
{: .sql}


3. Add data!
    1. Export csv file from FileMaker
        1. Check order of columns in MySQL and match export
    2. Import csv file into MySQL
    3. If we have the time - run through importing without creating table & columns first to show what happens

> ## CSV or comma separated value and TSV or tab separated value
> * The comma or tab are delimiters (what is being used to deliminate between one cell and the next) but you can also determine qualifiers or ways to enclose the contents of a cell in case the delimiter may occur within the cell contents. 
> * Ideal for preservation and dissemination as most applications are able to read.
{: .callout}