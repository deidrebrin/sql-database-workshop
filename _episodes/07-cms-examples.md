---
title: "MySQL for Drupal and Wordpress"
teaching: 15
exercises: 1
questions:
- "How do Wordpress and Drupal use MySQL?"
- "How can I backup and restore my database when using a CMS?"
objectives:
- "Understand how Drupal and Wordpress create and update a database."
- "Learn how to backup and restore when working with WordPress or Drupal."
keypoints:
- "Be sure you understand and test the backup AND restore process for any database you work on."
---

## WordPress MySQL and Drupal MySQL
The content management systems WordPress and Drupal use MySQL to store the structure and data of the websites. The CMS automatically builds out the data schema and enters data as you create pages, posts, and content on the front end. However, the first time you look at the database it can be intimidating. 

Let's look at the database for a WordPress site and a Drupal site using **phpmyadmin**.


### Things to keep in mind…
* Create and document your database user account and password somewhere secure
* Make sure the user has privileges to the database

### Backups
It is essential that you know how to backup AND restore your database. Make it a practice to perform a backup before executing any complex, large, or basically any operations you wouldn't want to repeat. Be sure to test the restore process also so you know what to do if something goes wrong. Strategize about how you can incorporate database backups into your version control procedures.

Drupal has some quirks that can cause issues when backing up the database. To avoid any issues when restoring a database follow the steps below:

1. Put site into maintenance mode
2. Turn off clean URLs
3. Log in to phpmyadmin and EMPTY each table that begins with the word ‘cache'
4. Export as SQL (compressed)
5. Make a note of how many tables and rows are in the database

When restoring DROP all of the tables in the database before import, check that the number of tables/rows imported are correct, turn clean URLs back on and take the site out of maintenance mode.

> ## Challenge
> Backup and restore a Drupal site
> > ## Solution
> > Follow the steps above
> {: .solution}
{: .challenge}
