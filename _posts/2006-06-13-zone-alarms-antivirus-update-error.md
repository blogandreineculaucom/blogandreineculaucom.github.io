---
title: Zone Alarms - Antivirus Update Error
author: Andrei
layout: post
permalink: /2006/06/zone-alarms-antivirus-update-error/
categories:
  - Information Technology
  - Solution
tags:
  - firewall
---
If you get an update error for the antivirus module, then the answer is simple: somehow the update could not be downloaded, yet ZoneAlarms announces an update.

You need to go to <http://consumerdownloads-west.ca.com/myeTrust/autodownload/modules.txt> and check to see which is the latest version for the Vet.Signatures.

Then go and download http://consumerdownloads-west.ca.com/myeTrust/autodownload/sigs/vet.signatures-XXXX.zip (XXXX means the version number).

Boot into safe mode and replace boot.dat and vet.dat in WINDOWSSystem32ZoneLabs with the ones from the ZIP archive.

This will also solve the issue with having the software up-to-date, yet Security Center issueing warnings about it not being up-to-date.