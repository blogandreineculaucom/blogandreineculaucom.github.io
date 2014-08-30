---
title: Making Firefox faster
author: Andrei
layout: post
permalink: /2006/03/making-firefox-faster/
categories:
  - Information Technology
  - Solution
tags:
  - browser
---
Did you notice how Firefox doesn&rsquo;t load pages from the local cache upon hitting the Back button? This is what IE and Opera do, but not Firefox.

In order to speed things up, you need to trick Firefox into doing that. No obvious option exists.

Go to &ldquo;about:config&rdquo;. Right click inside the window and select New Integer. Enter &ldquo;browser.sessionhistory.max_viewers&rdquo; with a value of 5.

Test it. If you don&rsquo;t like it, or you have problems having this feature on, then just delete the new option from the list.