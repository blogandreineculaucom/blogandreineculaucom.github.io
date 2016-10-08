---
title: KTH/DSV New IPv6 Wireless
author: Andrei
layout: post
categories:
  - I/Me/My
  - Information Technology
  - Solution
  - Sweden
tags:
  - kth
  - windows vista
---
For some reason, KTH/DSV awakened and decided to improve their access points over the summer. In doing so, they went from 3 network SSIDs (eduroam, KTHOPEN-WPA and KTHOPEN) to... yes, 4 network SSIDs (eduroam, KTHOPEN-WPA, KTHOPEN and KTHOPEN-OLD). Wow! Now that's an improvement. Anyways...

One thing that I've noticed only now (and I guess it's due to their changes; maybe IPv6 ) is that now my Vista can connect to multiple access points. I'm being ironic, since it could do it before as well, but now I \_see\_ it. Vista's Network Identification thinks that I'm connected to multiple networks -  same SSID but different gateway MAC address. That's why you get prompted to choose your network profile (Home/Work/Public) so many times, and then you can also see that you are connected to 11+ networks.

My fix was to disable IPv6 support for my Wireless connection. For current times it's useless anyway. Read [here][1] how to do it yourself.

 [1]: http://www.mydigitallife.info/2007/09/09/disable-and-turn-off-ipv6-support-in-vista/