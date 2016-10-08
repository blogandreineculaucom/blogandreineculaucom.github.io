---
title: Preloading JavaScript
author: Andrei
layout: post
categories:
  - Information Technology
  - Solution
tags:
  - developer
  - javascript
---
If you are starting to wonder with Prototype and Ajax, etc. then you might have noticed that the JavaScript libraries are getting too big.

If you haven't, then I'm telling you that Prototype and two other Effects libraries can take up to 300kb. Imagine the visitor sitting with a page for more than 1 minute in front of his eyes, that is simply blank.

If you're thinking that preloading is easy, it is not. Maybe I'm not using a proper term for this, but what I mean by preloading is that while the browser is loading the JavaScript libraries in his cache (hopefully it has a cache, otherwise it will load them over and over again for each page) the visitor doesn't get any input.

Don't get carried away saying that you just update a DIV or something, and tell the visitor what is happening in the background. Since these JS files need to be in the HEAD, you can't really control the loading of the BODY, plus depending on the browser JS files are loaded (a)sync.

The solution I'm proposing is to use a W3CDOM solution, which means that you in the BODY you have a script that creates DOM elements with tag SCRIPT, then add them to the HEAD element. You can also attach an onload/onreadystatechange (non-IE / IE) event to see when one library has loaded, and move on to the next one.

This way you are downloading the JS libraries (sync.) and can put a progress bar for the visitor. You should put this on an intro page, and then send the visitor to the main page, having all JS libraries already in his/her browser's cache.

Don't worry about not all browsers accepting W3CDOM. If they don't, then they should have nothing to do with Prototype and advanced scripting.

One last thing: if you think about visitors accesing your website through another page, other than your intro page, then simply check the REFERRER and if the domain is different from yours, then send him/her to the intro page automatically.