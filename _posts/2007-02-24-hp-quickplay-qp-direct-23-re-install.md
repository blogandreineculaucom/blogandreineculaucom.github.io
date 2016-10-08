---
title: HP QuickPlay & QP Direct 2.3 Re-install
author: Andrei
layout: post
categories:
  - Information Technology
  - Solution
tags:
  - hewlett-packard
---
For some time now I haven't had this running, and now with a needed formatting of my hard-drive I wanted to have everything fixed.

My situation is like this - 1 HDD with 1 partition for the OS, another one for "my stuff" and another one for QuickPlay!

So, first of all, you must know that QP and QP Direct installing software are a bit dumm.

In order to install QP 2.3 fully I had to do it in safe mode.

You should do the same, but before that you should search for an update (at this moment there's a v3409 patch). So, enter safe mode - install QP 2.3. and apply the patch.

Now - the QP Direct installing software has a problem detecting where to put the mini-Windows (often given by error -2147418113, in the QuickPlay component). You have to create an empty partition (unformatted) at the end of your first hard drive, but make sure that it is a PRIMARY partition and not a logical one. Norton Partition Magic is perfect for this!!!

So… make sure you have 1GB free, unformatted at the end of your first HDD. Then run QP Direct install. It will ask you to restart in the end.

I don't know if the same scenario will be yours, but when I rebooted, my system said something about missing system32hal.dll (don't piss on yourself!)

Just put your Windows XP/Recovery CD and then go to Recovery console! Just run "fixboot c:" and "bootcfg /rebuild" and add all your Windows partitions. One of them is the newly created partition with QuickPlay Direct on it.

Then restart. Make sure you boot into your QuickPlay Direct mini-Windows. The system should install the basic drivers for the system, and maybe you will get some warnings about not being able to work with the hiberfil file (the hibernation file that it needs to speed up the boot process, but so far you haven't used QP Direct, and so there's no hibernation file! - again, very dumm).

You should now have QP Direct up and running!

The system should boot into YOUR windows normally, but start the QP Direct windows when you press the QP logo or DVD shortcut button!

Break a leg… tell me what happens!