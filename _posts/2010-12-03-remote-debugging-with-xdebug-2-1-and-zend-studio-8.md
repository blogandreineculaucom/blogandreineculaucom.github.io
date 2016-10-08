---
title: Remote debugging with xdebug 2.1 and Zend Studio 8
author: Andrei
layout: post
categories:
  - Information Technology
  - Likes
  - Solution
tags:
  - apache
  - debug
  - eclipse
  - php
  - web server
  - zendstudio
---
**UPDATE 20110407**: If Apache crashes randomly when you activate debugging, make sure you run Apache with administrator rights. If you have it as a process (not as a service), just start xampp-control.exe by right-clicking and choosing "Run as administrator", and restart the Apache process

I'll put down some things I learned on the matter, along the question: how do you make it work?? solution!

So, to start from the beginning:

*   [Zend Debugger][1] does not work on the latest [XAMPP][2] 1.7.3, because it uses [PHP 5.3.1 VC6 Thread Safe][3]
*   Zend stopped producing the Zend Debugger for PHP thread safe versions, because along with Microsoft, they reached the conclusion that non-thread safe is the only way to go
*   The easiest way to get Zend Debugger and a Web Server up and running would be to download Zend Server (there's a Community Edition as well - free)
*   My problem was this: for some reason the Zend Server was slow, produced errors now and then.. leaving plenty of php-cgi.exe processes behind, and a slow or a broken option to restart the web server

So I wondered around and leaned towards [xdebug][4] as an option to have XAMPP back.

Installing xdebug in xampp is rather easy. Get the latest binary from[ xdebug.org][5] . With XAMPP 1.7.3 you will need the "*5.3 VC6 Non-thread safe (32bit)*" version. If you want to be sure, follow the instructions on [this page][6]. Put the downloaded binary under *xampp/php/ext* .

Step 1. Add/uncomment the following in *xampp/php/php.ini* (extract from my *php.ini*)

<pre>[XDebug]
zend_extension=<em>xamppphpextphp_xdebug-2.1.0-5.3-vc6.dll</em>
xdebug.profiler_enable = 1
xdebug.profiler_enable_trigger = 1
xdebug.profiler_output_dir = "<em>xampptmp</em>"
xdebug.profiler_output_name = "xdebug_profile.%p"
xdebug.remote_autostart = 0
xdebug.remote_enable = 1
xdebug.remote_handler = "dbgp"
xdebug.remote_host = "127.0.0.1"
xdebug.remote_log = "<em>xampptmpxdebug.log</em>"
xdebug.remote_mode = "req"
xdebug.remote_port = 9000</pre>

Online, you can find tutorials asking for a different port (i.e. 10000), yet I had problems making xdebug accessing that port. Also, if you have your web server on a different machine than the one you will debug one, change the *remote_host* variable to the debugger's IP address. This variable can only take on IP address (debugging can take place only from one machine).

Step 2. After restarting your XAMPP (from the XAMPP Control Panel), you should test your configuration. You can easily do that by going either accessing a phpinfo() script, or going to your XAMPP website (usually http://localhost ) and clicking on the left-side "phpinfo()" link. You should find the following, right after the first table: "This program makes use of the Zend Scripting Language Engine: Zend Engine v2.3.0, Copyright (c) 1998-2009 Zend Technologies **with Xdebug v2.1.0, Copyright (c) 2002-2010, by Derick Rethans**". If you see the xdebug reference, you're set to go.

Step 3. To test for connectivity, you will need [a Firefox extension][7] called *easy xdebug* (that triggers remote debugging; ) and [xdc (xdebugclient)][8]. **This test will only work if you debug and run the web server on the same machine.** After installation, go into xdc and tell it to start listening from the menu. Now, whenever you click on the green icon (lower right of the Firefox window) and it turns into a red circle, then refresh the remote page, you should end up in xdc, ready to step into, step over, step out of your coding lines. When the green icon has no red circle, it should run without triggering xdc.

Step 4. Everything works? Next, Zend Studio to be set up. Click Windows -> Preferences.  
Now, select **PHP > Debug** . Select **XDebug** under *PHP Debugger*, then click on *Configure...*, click *XDebug*, click *Configure* and change *Accept remote session (JIT)* to **any**.  
Go back to **PHP > Debug** . Click *PHP Executables...*, then *Add*, and fill in with the path to **xampp/php/php-cgi.exe** and **xampp/php/php.ini**, SAPI = **CGI** and Debugger = **XDebug**.  
Go back to **PHP > Debug** . Select your PHP Executable that you've just created.

Now, if I didn't forget anything, it should all work i.e. When the green icon in Firefox has the red circle (= you request the page to be debugged), ZendStudio should start debugging. Some mention that you get a popup window asking you to do some path mapping (where you associate the script path on your remote machine with the script path on your debugging machine, or with a ZendStudio project path), but I don't get that (maybe because localhost is my debugging machine and my web server; it used to happen with Zend Debugger, but not with XDebug).

PS: This blog post is based on many online references, like [this][9], or [this][10] and many others.

 [1]: http://www.zend.com/en/products/studio/downloads
 [2]: http://www.apachefriends.org/en/xampp.html
 [3]: http://php.net/downloads.php
 [4]: http://www.xdebug.org
 [5]: http://www.xdebug.org/download.php
 [6]: http://www.xdebug.org/find-binary.php
 [7]: https://addons.mozilla.org/en-US/firefox/addon/58688/
 [8]: http://code.google.com/p/xdebugclient/
 [9]: http://bogdan-albei.blogspot.com/2010/06/php-remote-debugging-with-xdebug-and.html
 [10]: http://devzone.zend.com/article/2930