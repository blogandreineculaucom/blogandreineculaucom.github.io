---
title: Missing My Documents/Music/Pictures icons
author: Andrei
layout: post
categories:
  - Information Technology
  - Solution
tags:
  - windows xp
---
If you move your Documents/Music/Pictures or you play with their desktop.ini file then you might end up having "normal" folder icons instead of their special ones. The thing is that usually if you miss those, probably there is some other information not running ok.

In order to fix this, simply open a command prompt and run the following:

> rundll32 mydocs.dll,PerUserInit