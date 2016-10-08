---
title: Trac on Dreamhost
author: Andrei
layout: post
categories:
  - Information Technology
  - Social
tags:
  - apache
  - dreamhost
  - fastcgi
  - php
  - python
  - sql
  - svn
  - trac
---
Of course, you can read a lot about it on <http://wiki.dreamhost.com/Trac>

[Trac][1], the open-source project management and bug-tracking system, is now a one-click install on [Dreamhost][2], after a big struggle with installation scripts.

What you cannot read on the wiki, is this:

*   change the date & time format by doing the following 
    *   look into your.trac.domain.com folder for index.fcgi
    *   edit the file, and add LC\_TIME="sv\_SE";export LC_TIME after the first line
    *   sv_SE is the locale identifier - you can see what locales you have available (Dreamhost has quite many) by typing "locale -a" in your SSH terminal



*   change from sqlite (file) database to MySQL by doing the following 
    *   create [your-trac-schema] in your [Dreamhost panel][3]
    *   look into [your.trac.domain.com]/conf folder for trac.ini
    *   edit the file and look for database=sqlite:db/trac.db and change it to database=mysql://[username]:[password]@[your.domain.com]/[your-trac-schema]
*   use the same users and passwords that allow access to your linked SVN, by doing the following 
    *   look into [your.trac.domain.com] folder for .htaccess
    *   edit it, and prepend these lines 
        *   AuthType Basic  
            AuthName "Trac"  
            AuthUserFile /home/[your-username]/svn/[your-svn-project].passwd  
            Require valid-user

* items between [] need to be changed with your information

 [1]: http://trac.edgewall.org/
 [2]: http://www.dreamhost.com
 [3]: http://panel.dreamhost.com