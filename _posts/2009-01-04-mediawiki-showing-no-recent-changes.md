---
title: MediaWiki showing no Recent Changes
author: Andrei
layout: post
categories:
  - I/Me/My
  - Information Technology
  - Solution
tags:
  - sql
  - wiki
---
While playing with my new [wiki subdomain][1], I saw that my chances were being marked with rc_bot. In plain English, the changes were marked as if they were done by wiki bots.

This was (almost) due to the [GroupPermissionsManager][2] extension. I didn't care that much when I assigned permissions to groups, and by mistake I also assigned the "permission" markbotedits. This was triggering an empty Recent Changes page and RSS feed, because all bot changes are ignored by default.

Put that permission to False and you're done! Your new changes will show up under the Recent Changes page.

If you want to make the previous changes show up, then you will need to edit the mw_recentchanges SQL table and run

<pre name="code" class="sql">UPDATE mw_recentchanges SET rc_bot = 0</pre>

 [1]: http://wiki.andreineculau.com
 [2]: http://www.mediawiki.org/wiki/Extension:GroupPermissionsManager