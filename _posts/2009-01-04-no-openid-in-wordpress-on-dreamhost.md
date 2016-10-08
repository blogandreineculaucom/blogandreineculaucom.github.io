---
title: No OpenID in WordPress on Dreamhost
author: Andrei
layout: post
categories:
  - I/Me/My
  - Information Technology
  - Solution
tags:
  - dreamhost
  - php
  - web server
  - webhost
---
While I have been moving my blogs, and implemented some new subdomains, etc, etc.. I discovered the following:

My blog was having the [wiki:en:OpenID] plugin enabled. We all?! like open source, and one login for all, and innovative whistles and bells.. So I was happy with that.

But I was also unhappy about my blog receiving so many hits and seeing php5.cgi processes going like mad, and since PHP runs as CGI on Dreamhost you can't really track down the information that you would need. Yet you have Apache logs.. and there were lots and lots of "Successfully fetched" records, all hinting to pornographic websites.

It was clear that something was making requests to the outside, on my expense (all PHP processes on Dreamhost take CPU time, and thus can render, if the number is high, your domain unreachable), but what is it? After some investigation, the OpenID plugin for WordPress came out of the crowd, raised its hand and admitted: "**It's me!**"

This was later confirmed by [an article stating the exact same thing: lots of PHP requests, Apache logs, etc.][1]

So the bottom-line, since I found absolutely no article/patch to fix this situation, is to deactivate the OpenID plugins, whether they are for WordPress, for MediaWiki, etc. I'm sure that [wiki:en:Facebook_Connect|Facebook Connect] will take over in a matter of months, anyway.

 [1]: http://robrohan.com/2008/10/31/openid-maybe-not-as-cool-as-i-thought/