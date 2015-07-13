---
title: The Bat! - Unknown CA Certificate
author: Andrei
layout: post
permalink: /2006/06/the-bat-unknown-ca-certificate/
categories:
  - Information Technology
  - Solution
tags:
  - email
---
If you're having problems while connecting with The Bat! to get your mail through secure channels… meaning that you get a popup window saying that the client couldn't get the certificate, etc.

THEN the answer is to go to your Data folder, and delete IntermCA.ABD and RootCA.ABD.

The software has some troubles accessing those files. It will rebuild them upon the next startup. And it will work OK once again with secure channels.