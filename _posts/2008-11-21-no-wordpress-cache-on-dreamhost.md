---
title: No WordPress (Super) Cache on Dreamhost
author: Andrei
layout: post
categories:
  - Information Technology
  - Solution
tags:
  - blog
  - dreamhost
  - webhost
---
I've been having lots of 500 Internal Server Error messages on my blog lately.

Well, sometimes because of the way [WordPress eats up memory][1], sometimes because of something else.. the cache!

When you see that your blog is running a bit slow (it happens in [shared hosting][2], and especially with memory eaters) you immediately think about cacheing. If you don't think on your own, then you might complain to Dreamhost's Support Service, file a ticket, and they will do the thinking for you.

Now, what they don't know.. is that, while cacheing is a good concept, apparently the WordPress cacheing plugins are troublesome. After checking all of my plugins (of course, not checking exactly the right one) reading [about it][3] and then [some more][4], I tried disabling my [WP Super Cache plugin][5] (it's an enhanced version of WP Cache, but the later is still problematic. **Bingo! No more 500 Internal Server Errors.**

PS: Yes, I've been thinking of ditching Dreamhost for MediaTemple. But [no][6]! Stick with something good enough, willing to help out (Dreamhost's Support Service always seemed to have a collaboration attitude) and try to improve the situation. Moving around can only mean trial and error.

**UPDATE**

I have isolated the issue even more. It is not related to WP Super Cache per say, but to its compression feature. GZIP does take a lot of CPU time, and as a user puts it:

> Also, I understand that disabling GZIP compression, even though it reduces bandwidth, will increase the CPU time. Disable it. After all, on Dreamhost, bandwidth isn't the issue - CPU time is.

The problem is that for me, WP Super Cache didn't disable the GZIPing properly. After disabling the feature, and after disabling the plugin, under wp-content/cache I still had a .htaccess file that was telling the server to feed any requests from there with GZIP. After deleting the .htaccess and activating WP Cache, I'm quite confident to say I'm back on track.

 [1]: http://blog.andreineculau.com/2008/11/black-november-20/
 [2]: http://scott.yang.id.au/2006/01/the-dark-side-of-dreamhost/
 [3]: http://www.quickonlinetips.com/archives/2006/12/site-down-36-hours-how-i-fixed-internal-server-errors/
 [4]: http://www.vincentchow.net/1153/wordpress-internal-server-error
 [5]: http://ocaoimh.ie/wp-super-cache/
 [6]: http://news.netcraft.com/archives/2006/11/29/outages_for_mediatemple_grid_hosting_service.html