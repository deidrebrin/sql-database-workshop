---
title: "Controlled Vocabularies and Thesauri"
teaching: 10
exercises: 1
questions:
- "What are controlled vocabularies?"
- "What is a thesaurus?"
objectives:
- "Understand the benefits of controlled vocabularies and thesauri."
keypoints:
- "Controlled vocabularies allow you to efficiently enter, update, and analyze data."
- "Thesauri offer ways to address different conventions such as spelling."
---


## Controlled vocabularies and thesauri

Relational databases allow you to leverage your normalized fields to make data entry a lot more efficient (i.e. faster and with less errors). One such way is through **controlled vocabularies**—lists of values that may be entered into a field. Vocabularies allow you to quickly update all entries if you need to change a term, quickly add translations of terms to build in some multilingual support, reduce typos and errors in entering data (drop down lists, select boxes, etc). 

**Thesauri** are great for humanists and the types of data we frequently work with in our careers. Thesauri provide records of defined terms with alternate spellings, translations, and frequently sources. Certain terms may have multiple spellings depending on conventions but a thesaurus allows data referencing the same term to be understood as the same. They can also be incorporated into search tools so a record comes up regardless of the spelling in the search. 

[Tiwanaku example](http://www.getty.edu/vow/TGNFullDisplay?find=tiwanaku&place=&nation=&prev_page=1&english=Y&subjectid=1020440)

> ## Challenge
> Identify fields that could utilize controlled vocabularies in our dataset
>
> > ## Solution
> > * Finds 
> >   * type (Human remains, Hat, Grave goods)
> > * Burials
> >   * type (Pit, Tomb)
> > * Hats
> >   * colors (Black, Orange, Blue, Yellow)
> > * Individuals
> >   * status (High, Low)
> {: .solution}
{: .challenge}

> ## Challenge
> Add the controlled vocabularies to our FileMaker Pro database and enter some data!
> 
> > ## Solution
> > Tip: While FileMaker Pro provides the value lists that can be used for controlled vocabularies, it is a good practice to build out a table for each controlled vocabulary and to link to that instead. This will make moving your database to another system faster and easier as there isn't a straightforward way to export value lists from FMP. 
> > 
> > Steps for FMP challenge (add details and screenshots)
> > * Add controlled vocab tables
> >    * burial_types
> >    * finds_types
> >    * colors
> >    * statuses
> > 
> > * Add these tables as value lists
> > * Enter burial record
> > * Enter finds records
> > * Enter hat record
> > * Enter individual record
> > 
> > * Add burial type to find record
> > * Add portal to finds to burial record
> >
> {: .solution}
{: .challenge}