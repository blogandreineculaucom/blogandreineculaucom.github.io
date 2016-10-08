---
title: Multiple websites using IIS 5.1 on Windows XP
author: Andrei
layout: post
categories:
  - Information Technology
  - Solution
tags:
  - developer
  - web server
---
Ever wondered how you can set up multiple websites in Windows XP (i.e. Proffesional)?  
Did you wonder at least if it possible?

Well, it is. Microsoft has it's own way of hiding things…from novice users, so that the system will not crash down… Hmm, just a small thought: is this how you should protect something? By not letting people get their hands on all of it?

Another small thought: Microsoft is more like…building this car, lots and lots of advertising to gather a big percentage of the market, you buy it, looks very nice with all those visual styles…iuhuu! :) …then, when something goes wrong with the car..and you just want to take a peak….uppps!… The hood is locked.  
But still, Microsoft is Microsoft and few wackos can deny this…

Back to our stuff.  
Inside the INETPUB folder that Windows XP creates when installing IIS, there's a folder called ADMINSCRIPTS…  
Open a Command Prompt in that folder.  
By typing "**adsutil.vbs enum w3svc /p**" you will get a list of websites created. Basically only the Default Website (W3SVC/1)

To create a new one, type  
"**adsutil.vbs create_vserv W3SVC/2**" (the last number can be anything; it is the index of the new website)  
"**adsutil.vbs copy W3SVC/1 W3SVC/2**"  
and go to the Internet Information Services/Computer Management and rename this new website, give it a new root folder and set it up however you like.

To delete one, type  
"**adsutil.vbs delete W3SVC/2**"

What you have to remember is that in Windows XP, you can only have one, and only one website running.

Of course, there is a simpler way - free software:  
<http://www.firstserved.net/services/iisadmin.php>  
<http://jetstat.com/iisadmin/>

You can also try <http://www.hairy-spider.com/multisite.aspx>, which is an ISAPI filter that can associate different domains to 127.0.0.1 and differenciates requests through that. It doesn't deliver website alternative configuration though.