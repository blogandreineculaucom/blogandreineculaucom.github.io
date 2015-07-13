---
title: Vista x64 - Learnings
author: Andrei
layout: post
permalink: /2007/06/vista-x64-learnings/
categories:
  - Information Technology
  - Solution
tags:
  - windows vista
---
User Account Control (UAC)

*   Do not go in Control Panel - User Accounts and turn it off. Instead search in Start Menu for "Local Security Policy" or "secpol.msc", go to Local Policies - Security Options. On the right-side list look for "User Account Control: Behavior of the elevation prompt for administrators in Admin Approval Mode" and change that to "Elevate without prompting"

Hibernation, Sleep, etc. - Power Profiles

*   Before going mad about your computer not hibernating, or acting weird upon sleep, etc. make sure that your BIOS Flash is up-to-date. Well-known manufactures strive to make comprehensive updates continuously (e.g. HP).
*   Enable hibernation by typing "powercfg -h on" in an Elevated Command Prompt.

Folder related problems

*   If you use applications that don't properly detect System folders, then just let them install wherever they want, and then use [SHJunction][1] to redirect those folders to wherever it is needed.
*   Example and solution: Winamp doesn't detect properly that you can have a Shared Settings Folder, so it automatically start building up a new folder in your Application Data folder. Instead of reconfiguring Winamp, just delete everything inside Application DataWinamp and link that with SHJunction to your Shared Settings Folder.
*   The same solution applies if you're running two Windows versions. Instead of having software configured twice, just link one folder to the other inside Application Data or Local SettingsApplication Data.
*   One important thing is to run the software as Administrator. Just right-click - Properties and change Compatibility to "Run as administrator".

DivX

*   In order to register DivX (fixing the missing dtu100.dll) you should copy dtu100.dll from WindowsSysWow64 to WindowsSystem32

Apache Monitor

*   Apache install correctly, but upon launching "Apache monitor" you get a "Operation completed successfully" message and the application closes. Just right-click - Properties. Change compatibility to run in a Windows XP SP2 environment.

WinACE

*   If the context menu is not showing for archives, just run WinACE as Administrator and then go into Options and fix file associations!

PowerISO

*   If the context menu is not showing for images, just run PowerISO as Administrator and then go into Options and fix file associations!

Yahoo Messenger

*   For now, it seems like it doesn't detect webcams ?! Though Live and Skype do!

Mouse

*   If your mouse doesn't have drivers/software for Vista (x64) and you miss giving other meanings to the extra buttons, then just download [XMouseButtonControl][2] and go with that. Remember that in order to act on elevated applications, you must elevate (run as administrator) XMouseButtonControl.
*

 [1]: http://www.bitsum.com/shjunc.asp
 [2]: http://www.highrez.co.uk/downloads/XMouseButtonControl.htm