---
title: WLW & WordPress
author: Andrei
layout: post
permalink: /2008/01/wlw-wordpress/
categories:
  - Information Technology
  - Solution
tags:
  - blog
---
For some time now I've switched from [BlogJet][1] to [Windows Live Writer][2] for blogging.

It's more than ok to write online, but sometimes you don't have a connection (yes, you could very well write in notepad, but there are things like categories, timestamp, etc), or it's simply easier to post from flickr, youtube, etc.

Getting back to the main topic. Everything performs flawlessly. You even have the option to write in a web-preview, so you know how much to resize photos, etc.

One exception: for WordPress, WLW starts writing HTML code. And so, when you publish an image.. the WordPress RPC expects XHTML and has problems when showing the image - both on the blog, and in the editing interface of WordPress.

But if you go to Tools - Accounts, and edit your account, under Advanced you will find the option to set the Markup Type. Set it to XHTML and things should be just fine!

 [1]: http://www.blogjet.com
 [2]: http://get.live.com/writer/overview