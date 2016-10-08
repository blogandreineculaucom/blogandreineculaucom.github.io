---
title: Database Column Naming
author: mediawiki
layout: post
categories:
  - Uncategorized
---
This has been a topic for quite a while, and still is. What is the best (safe & practical) way to name your table columns for a project?

There are conventions, there are rules, but so far I haven't read a full "lesson". I don't want to look like a guru. I'm just sharing my best practice!

Firstly, let's take a look at general rules.

#No CamelCase, no capital letters.  
#Use underscore to separate words.  
#Name your tables by using using initials/abbreviations as prefix, an optional grouping word/abbreviation, and with a full word.  
E.g. : ms\_auth\_users, ms\_auth\_groups  
#*ms - initials of Management System  
#*auth - table group (optional)  
#*users  
#Try to name your tables in a such way so that you don't have the same initials (coming from the group and full word) for two tables.  
E.g.: ms\_auth\_users (au), ms\_space\_units (su), NOT ms\_area\_units (au)  
#Never reference the table the same way you refer to its items. If the item is user, then the table has users, thus table = users.  
E.g.: ms\_auth\_users, NOT ms\_auth\_user

And now column naming

#Identification column should not be just id, but also prefixed with the table's initials. E.g. : au\_id (initials of auth\_users)  
#Try to use only one word that describes the column. Using two should be a highly rare exception.  
#Talking about the rare exception, the following is not. In some cases, it is good to know the "type" of the column not by looking at the column's type, but at the column's name. So if the column is date or is counting something or similar, prefix the name by date/count/etc. E.g.: date\_registered, count\_students  
#Foreign keys should be suffixed with fk. While doing this you may have to write an additional equal sign and column name when joining tables (instead of "ON au\_id" you would write "ON au\_id\_fk = au\_id), but it does give you a good perspective on how your columns relate to others. E.g.: au\_id\_fk

A few other good?! tips:

#Identification column should never be BIGINT. Trust me, MEDIUMINT is enough.  
#The same goes for Blob/Memo type. MEDIUMBLOB or MEDIUMTEXT is enough.  
#Identification columns and foreign keys for them should always be UNSIGNED. You would never have negative IDs anyway.

Note! This post was written while having MySQL in mind. Certain differences might apply.  
\[[Category:Defines me]\] \[[Category:IT\]]
