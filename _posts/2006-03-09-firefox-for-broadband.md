---
title: Firefox for Broadband
author: Andrei
layout: post
permalink: /2006/03/firefox-for-broadband/
categories:
  - Information Technology
  - Solution
tags:
  - browser
---
Type "about:config"

Set "network.http.pipelining" to "true"

Set "network.http.proxy.pipelining" to "true"

Set "network.http.pipelining.maxrequests" to some number like 30.

Right-click anywhere and select New-> Integer. Name it "nglayout.initialpaint.delay" and set its value to "0"