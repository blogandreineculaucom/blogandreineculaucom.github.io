---
title: Hej då Dreamhost, Hallå Glesys!
layout: post
categories:
  - Information Technology
  - Solution
tags:
  - blog
  - dreamhost
  - glesys
  - webhost
---

**UPDATE**: "We cannot provide refunds beyond your initial 97 days" - so there goes 55 USD of prepayment as well.

I've been a [Dreamhost](http://dreamhost.com) customer (both privately, and for [www.life-link.org](http://old.life-link.org)) for ~7 years, after moving from the Swedish [CrystOne](http://crystone.se).

Pleasant in the beginning, fast servers, live chat, quick customer support.

Slowly, the shared hosting became slow. No surprise there, it's shared. Moved to VPS. Better.

Quickly after, the VPS became slow. Increased resources, despite not many visitors, caching was in place, etc. Alternative hosts seemed unsure, expensive, there was no time to invest into moving to another host.

Yet it got so slow, that the server couldn't even deal with a `du -hcs` (i.e. calculate folder size) and Dreamhost was force-rebooting it every time that command was ran.

Earlier this year, I got introduced to the Swedish [Glesys](http://glesys.se). No bloatware, very much "WYSIWYG". Decide for yourself.

## Dreamhost snapshot - 400 MB

4 PHP websites (out of which 2 slim wordpress blogs) running on Apache, each with a MySQL schema, were constantly taking 400 MB. The spike is me running `rsync` (transferring to Glesys). Notice that I had to increase memory resources to 800 MB, so that I don't experience a forced-reboot.

![Apache memory on Dreamhost](/wp-content/2014-09-14-dreamhost.png)

After I moved to Glesys (running on Nginx), I thought of seeing if the difference in using Apache vs Nginx on Dreamhost. Even higher memory usage.

![Nginx memory on Dreamhost](/wp-content/2014-09-14-dreamhost-2.png)

## Glesys snapshot - 150 MB

Same things running on Nginx.

![Nginx memory on Glesys](/wp-content/2014-09-14-glesys.png)

