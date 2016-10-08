---
title: Still ASP & IIS - Locale
author: Andrei
layout: post
categories:
  - Information Technology
  - Solution
tags:
  - developer
  - web server
---
First you need to set Session.LCID and then Session.CodePage  
Otherwise, you will reset the CodePage by setting LCID

For example, I set 65001 as CodePage (UTF-8), then 2057 as LCID, as in UK English. But then UTF8 characters weren't displayed correctly.