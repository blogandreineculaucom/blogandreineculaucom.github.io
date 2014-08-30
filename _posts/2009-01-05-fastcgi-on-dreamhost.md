---
title: FastCGI on Dreamhost
author: Andrei
layout: post
permalink: /2009/01/fastcgi-on-dreamhost/
categories:
  - I/Me/My
  - Information Technology
  - Likes
  - Solution
tags:
  - dreamhost
  - php
  - webhost
---
**UPDATE 2009-01-11**: Dreamhost made FastCGI a default feature

For a while now, I got quite annoyed by the way a simple web app like a WordPress blog can be such a memory and CPU hog on Dreamhost. But that's what you get on a shared host with a CPU usage limit..

But wait! They are advertising this [FastCGI][1] option.. :)

So starting today I've enabled FastCGI on all my Dreamhost hosted sites. I can tell you it wasn't a piece of cake, but it was fairly easy.

In short, after reading [this][2] and more, this is what it is to be done:

*   tick the FastCGI option in the Panel (Domains - Manage Domains - Edit)
*   create a file named "dispatch.cgi" placed in the root of your (sub)domain or parent folder on which you want to enable FastCGI: 
    <pre>#!/bin/sh
export PHP_FCGI_CHILDREN=1
#export PHP_FCGI_MAX_REQUEST=100
exec /dh/cgi-system/php5.cgi</pre>

*   give the file execute permissions
*   create a file named ".htaccess" placed in the root as well: 
    <pre>Options +ExecCGI -Indexes +FollowSymLinks
AddHandler fastcgi-script fcg fcgi fpl
AddHandler php5-fastcgi .php
Action php5-fastcgi /dispatch.fcgi</pre>

Now, to explain a bit..

FastCGI optimizes the processes in many ways, but the most clear one is giving persistent MySQL connections by default, even to mysql\_connect PHP calls. Along that line, you can have multiple "host" or spawn processes. PHP\_FCGI\_MAX\_CHILDREN limits that. I have limited it to one child. First of all, I don't have that many concurrent visitors, and second of all, the processes are quite fast at finishing (seconds). So, overall, I think it's enough.

PHP\_FCGI\_MAX_REQUESTS is commented out because for some reason this is messing up Dreamhost. With that on, I get no FCGI processes. In essence, as read [here][3], this variable would have limited the number of requests that a host process could run. Supposedly, let's say, after 100 hits of a certain index.php, the host process would be killed, and with the 101st hit, a new host process would have been created. I liked the low limit, because.. it seems that some of the php5.cgi "child" processes don't get killed. And doing a cron with *killall -9 php.cgi* would.. in plain English, render the website unusable for a couple of minutes. Not to mention giving an Internal Server Error to all those that are visiting the website in that moment.

Bottom line is that on Dreamhost you can't use your own build of PHP CGI, but, even so, for sure it renders the whole process faster.

Having said that, I think this fixes all those nasty issues - slow website, server errors, etc, etc. - that I've been seeing and heard of.. :D

 [1]: http://www.fastcgi.com
 [2]: http://wiki.dreamhost.com/PHP_FastCGI
 [3]: http://redmine.lighttpd.net/wiki/lighttpd/Docs:ModFastCGI