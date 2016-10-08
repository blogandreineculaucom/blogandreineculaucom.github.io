---
title: Windows Firewall/Internet Connection Sharing  - Missing Service
author: Andrei
layout: post
categories:
  - Information Technology
  - Solution
tags:
  - firewall
  - windows xp
---
I don't know how I managed - must have been a Microsoft Update or some virus?! - but the "Windows Firewall/Internet Connection Sharing" Service was missing on my Windows XP.

Solution?  
A very good one on <a href="http://www.experts-exchange.com/" target="_blank">Experts-Exchange</a>.

Go to a computer that is working ok. Start "regedit". Go to HKEY\_LOCAL\_MACHINESYSTEMCurrentControlSetServices and export the branch SharedAccess. Then copy it to the system which lacks the service, and double-click it. That does it. <a href="http://www.experts-exchange.com/Operating_Systems/Q_21248930.html" target="_blank">More info</a>