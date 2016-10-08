---
title: ZoneAlarm and Internet Connection Sharing
author: Andrei
layout: post
categories:
  - Information Technology
  - Solution
tags:
  - firewall
---
I've had the chance to get into a situation where I had two computers, locally connected, one acting as a gateway to the Internet. Both of them had ZoneAlarm Pro running, set up correctly - one as a ICS/NAT client, the other as ICS/NAT gateway - yet the firewall on the gateway seemed to block access for the client to the Internet.

The solution is to add the DNS servers, that the gateway has been using, to the Trusted zone, on the gateway computer. Et Voila!