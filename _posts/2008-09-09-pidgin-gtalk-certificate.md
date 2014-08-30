---
title: Pidgin & Gtalk certificate
author: Andrei
layout: post
permalink: /2008/09/pidgin-gtalk-certificate/
categories:
  - Information Technology
  - Solution
tags:
  - messenger
---
I have two Gtalk accounts set up in Pidgin, but until today (since some weeks/months) I was annoyed by a dialog window popping up and asking me whether I accept some Gtalk certificate.

Today, I figured it out. It is related to the fact that Pidgin will "try" to have two certificates for the same address talk.google.com . And Pidgin won't use the correct certficate for each account.



**What you need to do is to **edit the settings for one of the accounts**, go to the **Advanced** tab, and use **talk.l.google.com** as server. That is a Google **redirect to the same talk.google.com** server, but Pidgin doesn't know that.**

Make sure you disable the account first, otherwise you cannot edit the settings for that account.