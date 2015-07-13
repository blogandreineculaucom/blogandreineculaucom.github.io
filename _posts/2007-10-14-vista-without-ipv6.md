---
title: Vista without IPv6
author: Andrei
layout: post
permalink: /2007/10/vista-without-ipv6/
categories:
  - Information Technology
  - Solution
tags:
  - windows vista
---
Not all equipments support [IPv6][1], and therefore cause problems - limited access, often network disconnections, etc.

In Vista, IPv6 is enabled by default, but given the current status - a very tiny part uses IPv6 - you should be able to disable its support without any disadvantages at all.

So here's how to do it.

1.  **Start Menu**
2.  Right click on **Computer**, select **Manage**
3.  Left Side List: click on **Device Manager**
4.  Application Menu: **View **-> **Show hidden devices**
5.  In the main list, under **Network Adapters**, you should now see *6to4*, *isatap.[..]*, *Teredo Tunneling Pseudo-Interface*
6.  Right click on each of them, and select **Disable**

All set. A computer restart would be nice though. Good luck!

 [1]: http://en.wikipedia.org/wiki/IPv6