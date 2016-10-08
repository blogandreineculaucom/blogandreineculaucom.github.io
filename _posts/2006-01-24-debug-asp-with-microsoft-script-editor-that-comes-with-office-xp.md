---
title: Debug ASP with Microsoft Script Editor (that comes with Office XP)
author: Andrei
layout: post
categories:
  - Information Technology
  - Solution
tags:
  - developer
  - office
---
Pff…..today, after working a way out of a crazy thread-related situation (when you have debugging enabled, you have a single-thread situation on your IIS server)….

I have also found a way out of another crazy situation!  
Setting Microsoft Script Editor to debug ASP once again!

I don't need any fancy debugger, and I don't actually enjoy Visual Studio, so the Script Editor that comes with Office XP is the best thing for me. It gives me a perspective on local variables when the error comes up, loads fast, it doesn't let me modify sources (which is good - I'm modifying them only in my coding environment), let's you stop the process safely.

Setting it up again… believe you ME… it wasn't easy at all!  
After "playing" with the Machine Debug Manager and reinstalling IIS over and over again…I found the solution. It is funny that I had to search everywhere and try everything… There's almost no post on the Internet about it. Microsoft has one (article 814714).. entitled <<PRB: "Jview.exe Failed to Launch" Error Message When You Debug a Visual J++ Application After You Remove Office XP>> — very hard to find.

Stop your World Wide Web Publishing, and Machine Debug Manager from the Services window.

Now, find "**vs7jit.exe**", usually in Program FilesCommon FilesMicrosoft SharedVs7debug  
At the Command Prompt, type "**vs7jit.exe /regserver**". This will set it up.

In the Internet Information Services, check that your application configuration has enabled server-side/client-side debugging. Do not start the application (website).

Now start the Machine Debug Manager again. Then the World Wide Web Publishing.

Pfiu. That does it!