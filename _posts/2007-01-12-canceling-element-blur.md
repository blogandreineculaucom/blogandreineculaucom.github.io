---
title: Canceling element Blur
author: Andrei
layout: post
permalink: /2007/01/canceling-element-blur/
categories:
  - Information Technology
  - Solution
tags:
  - designer
  - javascript
---
When you want to keep focus to an element, you might find it hard to do because the BLUR event is linked with an immediate FOCUS event.

So.. when you click outside an element (usually a form field) you blur that element, and focus another.

If you call element1.focus(); inside its BLUR event function, the browser will focus that event, but immediately afterwards it has to access the FOCUS event function for element2, thus focuses on another element in the end.

The solution comes from Jon at http://blog.thinkature.com/index.php/2006/11/26/escaping-the-javascript-call-stack-with-settimeout/ .  
The solution is to use setTimeout(function() {element1.focus();}, 0);

The events happen like this:  
- element1.BLUR  
- element2.FOCUS  
- timeout stack -> thus focusing back on element1!

> Jon handles most of the client-side coding for Thinkature. He's proud to be a graduate of the inaugural class of 2006 at Olin College and hopes to one day make the world a better place by working with renewable energy.