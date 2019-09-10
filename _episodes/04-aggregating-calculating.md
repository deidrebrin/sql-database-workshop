---
title: "Usability and Preservation"
teaching: 10
exercises: 1
questions:
- "How can I make sure my data is usable- to me and others?"
- "Why does documentation matter?"
objectives:
- "Understand how use, reuse, and preservation are related"
- "Understand what to document and how this facilitates reuse."
keypoints:
- "SQL can be used for reporting purposes."
- "Queries can do arithmetic operations on field values."
---

## Notes on usability, reusability and preservation
Planning for preservation from the beginning almost always results in better data overall. Throughout the course of a project, the technologies and resources available to a researcher will change. 

There are different strategies to digital preservation that are selected based on the needs of the project. **Technology preservation**—maintaining hardware and software components so that the data can continue to be read and used—is often not an option for researchers as hardware becomes obsolete quickly. Similarly, an **emulation strategy** in which custom software is developed to run on more modern hardware while simulating the same type of interactions and interfaces of the older systems. This gets more complex as time passes and quickly becomes rather expensive to even attempt (aka not likely to happen in research domains). The last strategy, **migration**, is the most common. This means moving data from one system to another and keeping data in formats that support these migrations (i.e. nonproprietary). By acknowledging that your data is likely to move to an entirely different database system over the course of your research changes how you invest your time and resources. 

## Use, reuse, and preservation are all related
* The techniques that support the preservation of research data also facilitate the use and reuse of the data. 
    * non-proprietary file formats mean you and your colleagues can open and read the data on most computers
    * being able to export a data schema from a database means you can migrate to a new system when you pick up where you left off 10 years from now and your old software is defunct
    * other researchers studying related but slightly different topics can use your data model to understand how your data is structured and whether or not they can use it to answer their own research questions 

## Standards & Guidelines
You don’t have to start from scratch - many research domains have standards surrounding data collection and management. Talk to folks in your field, research repositories for your domain-their documentation will frequently describe what standards they have built their infrastructure around, and you can always ask subject librarians! If your field doesn’t have set standards, there are likely efforts out there to develop them. Before standards are widely adopted, groups will build guides or guidelines to flesh out what the standards should be (see [Guides to Good Practice](https://guides.archaeologydataservice.ac.uk/g2gpwiki/)). Following these guides or standards means you are less likely to miss something important (oops should have recorded which burial this hat came from…) and more likely others in your domain will be able to reuse your data. Granting agencies frequently want to know what standards you’ll be using and where you will be depositing your data.

## Documentation is essential for use/reuse/preservation
* Document codes or shorthand that are used in the recording process
    * makes it easier for you and others to read and understand the data
* Document collection practices, processing procedures, and any cleaning that has taken place 
    * integrity and trust (i.e. how status is determined in our example)
    * usability (i.e. how are we defining blue in our example)

> ## Challenge
> Document our dataset!
>
> > ## Solution
> > ### Project documentation 
> > * Deidre's Hat Project
> > * Project background: In 2500 Deidre's archaeological project began investigating the hat practices of the ancient HumTech culture. Excavations took place from 2500 - 2505 uncovering a variety of burials containing individuals with well-preserved hats. 
> > * Methodology: Excavation following Museum of London Archaeology Service practices. Data was collected and maintained in a variety of systems starting with Excel spreadsheets (2500) before migrating to a FileMaker Pro database in (2502) and finally a MySQL database in (2504). 
> > * Site information: HumTech Site coordinates, also referred to as CDH or Center for Digital Humanities
> > ### Data documentation
> > * Burials - prepared grave containing human remains. 
> > 	* Tomb burial - enclosed with stone
> > 	* Pit burial - earthen enclosure
> > * Finds - each find recovered during the excavation was recorded in the primary finds table. After entry, the finds were distributed to the relevant specialist and further analyzed.
> > * Specialist analyses 
> > 	* Hats - textiles identified as hats through an examination of their shape, weave, and hatness. Reference for what makes a hat a hat (someone has...).
> > 		* Colors were categorized by running elmental analyses to identify the dyes found in the textiles. Insert list of dyes and the associated colors. 
> > 	* Individuals - human remains with 40% or more of what was determined to be a single individual were given a unique record. Describe osteological methods used to determine one individual from another (aging, sexing, metrics, etc). Reference any standards used in this analysis. 
> > 		* Status was determined by the type of burial an individual was discovered in and the presence or abscence of grave goods. Tomb burials with grave goods were deemed "High" status while pit burials without grave goods were "Low". In cases where a tomb burial did not contain grave goods or pit burial did contain grave goods, the status was deemed "Low" as well. 
> > 
> {: .solution}
{: .challenge}












