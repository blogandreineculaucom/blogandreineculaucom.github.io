---
title: AJAX, onDemand JavaScript or Dynamic Script Tags
author: Andrei
layout: post
categories:
  - Information Technology
  - Solution
tags:
  - developer
  - javascript
---
Now, with Web 2.0 being closer and closer (actually it is already alive!) you don't just make asynchronious requests in order to get HTML or JSON… but ALSO JavaScript.

To be more exact… you make requests to get HTML with SCRIPT tags.

But the "beauty" is that the SCRIPT blocks don't get loaded/evaluated/ran. This if you AJAX for a response like

> <script type="text/javascript" src="my.js" id="myjs"></script><div>some other HTML</div>

<p dir="ltr" style="margin-right:0;">
  and put this in the innerHTML of a DIV element, then you will not get your my.js loaded. The same happens if you put actual scripting code inside the SCRIPT block.
</p>

<p dir="ltr" style="margin-right:0;">
  The first thing you think of (or at least I thought of) is to assign the response to a DIV element, then parse it to find any SCRIPT tags.
</p>

<p dir="ltr" style="margin-right:0;">
  For each SCRIPT element you do this
</p>

> <p dir="ltr" style="margin-right:0;">
>   for (var i in scriptElements) {<br /> var scriptElement = scriptElements[i];<br /> var newScript = document.createElement('SCRIPT');<br /> newScript.setAttribute('src', scriptElement.getAttribute('src'));<br /> newScript.setAttribute('type', scriptElement.getAttribute('type'));<br /> newScript.setAttribute('id', scriptElement.getAttribute('id'));<br /> newScript.data = scriptElement.data;<br /> if (_isMSIE_)<br /> {<br /> newScript.onreadystatechange = function ()<br /> {<br /> if (newScript.readyState == 'loaded')<br /> {<br /> _do your thing_<br /> newScript.onreadystatechange = null;<br /> }<br /> }<br /> }<br /> else<br /> {<br /> newScript.onload = function() {_do the same thing_}<br /> }<br /> scriptElement.parentNode.removeChild(scriptElement);<br /> var head = document.getElementsByTagName("head")[0];<br /> head.appendChild(newScript);<br /> }
> </p>

<p dir="ltr" style="margin-right:0;">
  Be sure to retain the IDs of the SCRIPT elements, so that you can eliminate them later, if you need to do this.
</p>

<p dir="ltr" style="margin-right:0;">
  This should fix it. BUT… there's also Internet Explorer! It always is.
</p>

<p dir="ltr" style="margin-right:0;">
  When you try to put the example AJAX response into an element's innerHTML, the SCRIPT tags dissappear!!! Why?! I do not know. Maybe it is because it will not load the SCRIPT anyway, so it erases it.
</p>

<p dir="ltr" style="margin-right:0;">
  The solution I came up with is: why should you need to use the SCRIPT tag when responding to the AJAX request? I respond with a normal "innocent" DIV tag like this:
</p>

> <p dir="ltr" style="margin-right:0;">
>   <div src="my.js" id="myjs" type="text/javascript"></div>
> </p>

<p dir="ltr" style="margin-right:0;">
  Then, when you search for "SCRIPT" elements, you can search for elements with type == "text/javascript", etc.
</p>

<p dir="ltr" style="margin-right:0;">
  Et voila! Enjoy!
</p>