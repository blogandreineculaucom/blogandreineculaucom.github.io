---
title: Fix for Gmail Manager 0.5.7.2
author: Andrei
layout: post
categories:
  - Information Technology
  - Solution
  - Video
tags:
  - browser
---
The current version (0.5.7.2) of the Gmail Manager extension for Firefox has a small bug. It shows no unread messages after activating Gmail Offline, although it is not necessarily so.

Checking the HTTP responses, the extension actually fails to login when Gmail Offline is enabled. As far as I can tell, upon performing the login, because I am based in Sweden, the response is to force the browser to do a redirect to google.se and set a Session ID (SID) and then return the browser back to the login URL. But the extension doesn't follow the redirect instruction, and thus fails to login properly.

I tried tapping into the extension code, but I didn't manage to solve it. My current workaround is to enable Gmail Offline for HTTP connections, and to have it disabled for HTTPS connections (the extension always tries to login through HTTPS). That's possible because Google Gears keeps two separate databases, due to different ports being used, even if it's the same URL. The settings for the account in Gmail Manager are to open my Gmail interface in HTTP, where I do have Gmail Offline enabled.

Long story short: Gmail Manager logs in and checks through HTTPS, where Gmail Offline is not enabled. Gmail Manager opens up Gmail through HTTP, where Gmail Offline is enabled. Watch the clip to get a step-by-step guide. Enjoy ;)

<!--YouTube Error: bad URL entered-->