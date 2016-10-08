---
title: 'Pidgin ICQ: The client version you are using is too old'
author: Andrei
layout: post
categories:
  - Information Technology
  - Solution
tags:
  - messenger
---
A couple of days ago, my Pidgin wouldn't connect to ICQ any longer.

It seems that the "lovely" ICQ team pushes people to upgrade their ICQ messenger, or else.. to switch to ICQ.

[pidgin.im][1] seems to be down, and there's no solution anywhere, except for [a patch][2]. <strike>But most of us don't do ICQ builds every time we pee, so that's practically of no help. But there's hope!</strike> Seems like the ticket patch comes along with a patched liboscar.dll as well



[Carsten Knobloch][3] to the rescue! [He published a compiled liboscar.dll][4] that has the patch. So what you need to do is:

*   download the DLL
*   quit Pidgin
*   copy the DLL to your Pidgin installation directory (Program FilesPidgin ?!)
*   start Pidgin
*   if you see the same message, just click *Re-enable*

That should do it for Windows. The same post has a solution for Ubuntu as well.

**UPDATE**: Although pidgin.im is down, it seems that they released **2.4.3** today which fixes the ICQ problem as well. [Download it here][5].

> **Changelog**
> 
> * **libpurple**  
> o Yahoo! Japan now uses UTF-8, matching the behavior of official clients and restoring compatibility with the web messenger (Yusuke Odate)  
> o Setting your buddy icon once again works for Yahoo! accounts.  
> o Fixes in the Yahoo! protocol to prevent a double free, crashes on aliases, and alias functionality  
> o Fix crashes in the bonjour protocol  
> o Always use UTF-8 for Yahoo! (#5973)  
> o Fix a crash when the given jabber id is invalid.  
> o Make the IRC "unknown message" debugging messages UTF-8 safe.  
> o Fix connecting to ICQ (#6220)  
> o Fix a memleak when handling jabber xforms.
> 
> * **Pidgin**  
> o Include the send button plugin in the win32 build  
> o Various memory leak fixes

 [1]: http://pidgin.im
 [2]: http://developer.pidgin.im/ticket/6220
 [3]: http://stadt-bremerhaven.de
 [4]: http://stadt-bremerhaven.de/2008/07/01/die-client-version-die-sie-nutzen-ist-zu-alt-lsung-fr-windows/
 [5]: http://sourceforge.net/project/showfiles.php?group_id=235&package_id=230234&release_id=610742
