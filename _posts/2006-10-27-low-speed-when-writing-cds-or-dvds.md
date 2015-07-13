---
title: Low Speed when writing CDs or DVDs
author: Andrei
layout: post
permalink: /2006/10/low-speed-when-writing-cds-or-dvds/
categories:
  - Information Technology
  - Solution
tags:
  - burn
---
I ran into a problem with my DVD-RAM unit. Low writing speed.

Why? Because DMA wasn't active.

Why it wasn't active? Because of the "best" mounting software - DAEMON TOOLS.

Just uninstall it, and your DMA will most probably be active once again, and you will write DVDs at 8x, and not 2x!!!