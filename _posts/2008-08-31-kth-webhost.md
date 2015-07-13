---
title: KTH Webhost
author: Andrei
layout: post
permalink: /2008/08/kth-webhost/
series_part:
  - 4
  - 4
categories:
  - I/Me/My
  - Information Technology
  - Solution
  - Sweden
tags:
  - kth
---
It's common that universities give you also some web-space along with your E-mail address. Why? To host your projects, presentations, individual research/projects, etc.

You can publish both in private and public mode. Basically you get a UNIX shell account.

The basic information, as it was with my situation, is as follows:



*   **Web** 
    *   Address: <http://www.isk.kth.se/~neculau/>
    *   No mod_rewrite available for .htaccess 
        *   This is how my .htaccess looks like right now:  
            `DirectoryIndex index.htm<br />
Redirect 301 /~neculau/index.htm http://andreineculau.com/`
    *   You should be able to get a MySQL database, but the link doesn't work
    *   [Read more][1]
*   **Shell** (use PuTTY, WinSCP, etc.) 
    *   Server: shell.it.kth.se
    *   Web folder: public_html
    *   Backup folder: .OldFiles
    *   Other folders: Public, Private
    *   Quota: 50MB
    *   [Read more][2]

 [1]: http://www.kth.se/student/support/ict/1.4789?l=en
 [2]: http://www.kth.se/student/support/ict/2.1299?l=en