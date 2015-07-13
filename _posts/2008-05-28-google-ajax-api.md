---
title: Google AJAX API
author: Andrei
layout: post
permalink: /2008/05/google-ajax-api/
categories:
  - Information Technology
  - Likes
tags:
  - browser
  - developer
---
<img class="alignright" style="float: right;" src="http://www.google.com/intl/en_ALL/images/logo.gif" alt="" />**Two years ago (May 2006)**, I was writing the following about the [Future of web browsers][1]:

> I don't know if I'm simply day-dreaming, but I guess that future browsers will offer full support for updatable JS libraries.
> 
> Thus, no more SCRIPT tag for loading Prototype and other AJAX / Effects libraries.
> 
> Why? Because web concepts are exploding quite fast nowadays, and simply having support for ECMA script is not enough. Plus these libraries are getting to be widely used, thus a question comes up: why should we download 200kb off every website we visit, which are the same 200kb every time? 200kb is not that much when you're using at least a Cable connection, but what about DialUp ?
> 
> I may not have time to go into building an extension for Firefox, but one that searches through SCRIPT tags and replaces those connecting to Prototype, Rico, etc with locally hosted files… that would be nice, right?

**Today**, I read how [Google Hosts Popular Javascript Libraries][2] and gives access to them through its [wiki:en:Content\_delivery\_network|CDN], the same way [YUI is distributed through Yahoo! CDN since February 2007][3].



And Ajaxian completes the picture:

> I just got to announce the Google AJAX Libraries API which exists to make Ajax applications that use popular frameworks such as Prototype, Script.aculo.us, jQuery, Dojo, and MooTools faster and easier for developers.
> 
> ...
> 
> **The Future**
> 
> This is just the beginning. We obviously want to add more libraries as you find them useful. Also, if you squint a little you can see how this can extend even further.
> 
> If we see good usage, we can work with browser vendors to automatically ship these libraries. Then, if they see the URLs that we use, they could auto load the libraries, even special JIT'd ones, from their local system. Thus, no network hit at all! Also, the browser could have the IP addresses for this service available, so they don't have the hit of a DNS lookup. Longer lived special browser caches for JavaScript libraries could also use these URLs.
> 
> The bottom line, and what I am really excited about, is what this could all mean for Web developers if this happens. We could be removed of the constant burden of having to re-download our standard libraries all the time. What other platform makes you do this?! Imagine if you had to download the JRE everytime you ran a Java app! If we can remove this burden, we can spend more time flushing out functionality that we need, and less time worrying about the actual download bits. I am all for lean, but there is more to life.
> 
> <p style="text-align: right;">
>   <a href="http://ajaxian.com/archives/announcing-ajax-libraries-api-speed-up-your-ajax-apps-with-googles-infrastructure">Announcing AJAX Libraries API...</a>
> </p>

 [1]: http://andreineculau.wordpress.com/2006/05/19/future-of-web-browsers/
 [2]: http://googlesystem.blogspot.com/2008/05/google-hosts-popular-javascript.html
 [3]: http://yuiblog.com/blog/2007/02/22/free-yui-hosting/