---
title: "Relational Databases"
teaching: 15
exercises: 2
questions:
- "What is a flat file?"
- "What is a relational database?"
- "Why do unique identifiers matter?"
objectives:
- "Understand the role and significance of primary and foreign keys"
- "Understand what it means to normalize data"
keypoints:
- "Relational databases "
- "SQL queries have a basic query structure starting with `SELECT` field FROM table with additional keywords and criteria that can be used." 
---

## Flat file vs relational databases

**Flat file or spreadsheet database** is a single table or collection of tables that do not have connections built among them
* good for simple datasets that are primarily text based
* most common way researchers start to collect and work with data (i.e. Excel/Google spreadsheets)

> ## Challenge
> Evaluate the demo spreadsheets - where would they excel, where would they fail? Pun intended.
>
> > ## Solution
> > Single table:
> > * Portable, easy to share
> > * Lacks any controls over data entry, easy to introduce errors, ambiguous unit of analysis, versioning may be confusing, difficult to add analyses from specialists
> > 
> > Multiple tables:
> > * Portable, easy to share, elevant information readily visible
> > * No way to associate objects in one sheet with other sheets, lack of control over data entry, easy to introduce errors, analyzing would be challenging
> {: .solution}
{: .challenge}


**Relational databases** on the other hand, allow data to be stored in different tables but with explicit relationships between these tables that provide connections
* facilitate complex data management
* ability to simplify data entry while maintaining data integrity (i.e. reduce typos, update values across the entire dataset)
* manage changes (transactions) to the database to avoid conflicts

Relationships require **unique identifiers** - each row in a table needs to be identifiable in order for another table to reference it. For example, different publishers may enter authors names differently when filling out records about an article (i.e. D. Whitmore vs Deidre Whitmore). However, if I associate the publication with my [ORCID ID](https://orcid.org/) (Open Researcher and Contributor ID) which is unique to just me, not only can I gather all of the publications I've authored together but I can also prevent the dastardly Deidra Whitmore from getting credit for my work.

> ### NOTE: when working with physical items:
> Unique identifiers **must** to be associated in some way with the object (i.e. tag, label, etc) so you can know which sample you are looking at later, even if you have a flat file system. Take the time to label the object, simply photographing isn't sufficient. Trying to match objects to photographs later is time consuming and sometimes not possible.
>
{: .callout}

**Primary keys** - field in a table designated as the identifier; must contain a unique (non-null) value for each row. 

When a table is referencing an identifier from another table (thereby making that connection between the two tables), that field is called a **foreign key**.

> ### A brief note on rows vs records
> Records in a database typically mean a row of data in a table; however, with relational databases connecting different tables together a record in a user interface may actually contain data from a handful of different rows in different tables. 
> 
{: .callout}

> ### A brief note on normalization
> * To normalize is to structure a relational database so that data is standardized across tables
>     * this means values will be consistent, the potential for entry errors is minimized, and changes & analyses will be easier
>     * example: Mezaber Adimenaber site name - trench table + site table
>     * in this instance - individuals and hats are studied by different people and require different types of data but thinking through the collection process - finds are collected and recorded in the field before they reach a specialist. Additionally, non-experts might not be able to identify a textile as a hat until it has been cleaned and/or pieced back together. So having a general finds table that holds all of the finds and their contextual information allows additional analyses to add details without requiring significant changes to the data model
> 
{: .callout}

> > ## Challenge: 
> > Diagram connections between our tables and normalize our dataset!
> > ## Solution
> > Tip - start with your primary unit of analysis, finds in our case

