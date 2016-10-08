---
title: Switching from PHP 4 to PHP 5
author: Andrei
layout: post
categories:
  - Information Technology
  - Solution
tags:
  - developer
  - php
---
If you use super globals, then you might have noticed that they changed the names for the super globals (i.e. $HTTP\_GET\_VARS turned into $_GET, etc)

For small scripts or future scripts, you should simply replace/use the new names.

But what do you do when you have big applications, or you use someone else's applications?

The solution lies in references. Simply put at the beginning of your PHP code:  
[sourcecode language="php"]  
$HTTP\_GET\_VARS &= $_GET;  
$HTTP\_POST\_VARS &= $_POST;  
...  
[/sourcecode]

[LATER EDIT]  
Thanks to Rique for pointing out the erroneous variable switch.