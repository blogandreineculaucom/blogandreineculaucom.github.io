---
title: IIS Multiple ASP Requests gets your application into stalling
author: Andrei
layout: post
categories:
  - Information Technology
  - Solution
tags:
  - developer
  - web server
---
If you've tried at least once to use CDO's procedure called CreateMHTMLBody and passed another local ASP script as parameter… and that got you waiting for a couple of minutes before receiving a message saying "Operation aborted" due to timeout, then here's the reason.

You probably have activated the ASP server-side debugging.  
And, as every IT proffesional does, you didn't read what that means exactly, by clicking on Help.

When you activate this option you will get your requests into single-thread mode, in order to get the debugger attached to the process. That means that the server respondes to only one request at a time. If a second request is made, it is being made secondary, and has to wait for the first to finish, and then it will get processed.

By using CreateMHTMLBody "**http://localhost/script2.asp**" from "**script1.asp**" you are initiating a second request. But this second request has to wait for "**script1.asp**" to finish, which in turn expects a reply from "**script2.asp**"…therefore the "dog running for its tail" situation.

The same situation will happen if you use the XMLHTTP object, or any other object that initiates a second request to the same server, and I may add same application. I am not sure, but it would be logical to be able to do that if you're using a different application with High (Isolated) Application Protection, thus having a different thread.
