---
title: Kasperky freezes when resuming from standy/hibernation
author: Andrei
layout: post
permalink: /2006/11/kasperky-freezes-when-resuming-from-standyhibernation/
categories:
  - Information Technology
  - Solution
tags:
  - firewall
---
I'm trying out Kaspersky Internet Security, and there's a funny thing that happened to me.

When I got my computer into standby/hibernate, upon re-entering the password, the computer freezed.

What was happening was that there was a modified module being loaded by winlogon.exe. And in the background (meaning - in the back of the logon "window") Kaspersky was asking me whether to allow it or not. I forgot to mention that this was in TRAINING MODE…

But as a good practice, go to Setting - Proactive defense - Application Integrity Control - Settings, and change winlogon.exe : content change — **ALLOW**! and not PROMPT FOR ACTION, because prompting for action happens in an invisible way (under the logon window that occupies all of the screen).