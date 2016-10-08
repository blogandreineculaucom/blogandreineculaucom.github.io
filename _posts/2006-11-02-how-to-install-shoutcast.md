---
title: Install ShoutCast
author: Andrei
layout: post
categories:
  - Information Technology
  - Solution
tags:
  - music
---
In a few words, ShoutCast let's you "air" your music!

It has been known for some time as the FREE RADIO - commercial radio stations actually use the same technology to broadcast themselves over the Internet.

But now, with so many communities around us, and especially with LAST.FM coming up so swell, it can be a tool in order to let your friends listen to what you're listening, and not just having a Yahoo/Live Messenger status with the title of the song.

You don't even have to go public with your radio station - it can be your and your friends' secret.

I will go through the steps. I will not get into fancy situations (firewall, etc), meaning that these steps are just for those who have a direct connection to the Internet.

And one more thing: you must have Winamp.

*   Go to <http://www.shoutcast.com/download/serve.phtml#scdownload> and click on the link [PROCEED TO LICENSE AGREEMENT TO DOWNLOAD SHOUTCAST DNAS] and then follow the steps to download ShoutCast server (probably the first in the list, which would be for Windows Operating System)
*   Install the newly downloaded software.
*   Run it from the Start Menu (SHOUTcast DNAS group). You might get a notice from your Firewall asking you to Allow/Unblock the application to transmit data.
*   Click on the menu's EDIT CONFIG. A text file would be opened. Search inside for these:

*   *   "MaxUser=" - set it to how many users you would like to connect to your radio station; I would suggest 2/3 if you are planning to broadcast only to a few friends, in order to share listening to your music
    *   "Password=" - set a password of your own
    *   "TitleFormat=" - remove ";" from the beginning of the line and change the title as you wish, maybe just replacing "Justin" with your nickname is a good idea
    *   "PublicServer=" - if this is just for friends, set it to "never"

*   Save the text file's changes and close it.
*   In the window "Nullsoft SHOUTcast Server Monitor", click on KILL SERVER from the menu and restart the application.
*   Go to <http://www.shoutcast.com/download/listener.phtml> and download the plugin for Winamp. Install it.
*   Open Winamp. Go to Preferences - Plugins - DSP/Effect. Select "Nullsoft SHOUTcast Source DSP" and then click on "Configure active plug-in".

*   *   Go to the OUTPUT tab in the plugin's window.
    *   Choose to Connect at (Winamp's) Startup or not.
    *   Under OUTPUT CONFIGURATION put your own IP address (you can find it easily by going to <http://www.whatsmyip.org/>), fill in with your password and check "Automatic Reconnection on Connection Failure".
    *   Click on YELLOWPAGES, right above where you filled in with your IP address. Uncheck "Make this server public" so that you won't let general audience find your radio station.
    *   Go to the ENCODER tab in the plugin's window.
    *   Select MP3 Encoder and probably "48kbps, 44100 kHz, Mono" will be enough. you can increase the quality, but this would mean that your friends might risk having pauses because the connection is not working swell. You can also decrease it, but it would mean that sound is going to be crappy. This is something you have to play with, along with your friend(s) who will listen to your radio station.
    *   You're SET!

*   All you have to do now is let your friend know that he/she can connect to your radio station at xxx.xxx.xxx.xxx:8000 (fill in with your IP address).
*   It should work! :)

PS: success <a href="http://www.fotolog.com/ella_girl" target="_blank">elarocks</a>! :p

**Now playing:** [Robbie Williams][1] - [Let Love Be Your Energy][2]

 [1]: http://phobos.apple.com/WebObjects/MZSearch.woa/wa/advancedSearchResults?artistTerm=Robbie%20%20Williams
 [2]: http://phobos.apple.com/WebObjects/MZ%3Cp%3E%3Cp%3ESearch.woa/wa/advancedSearchResults?songTerm=Let%20Love%20Be%20Your%20Energy&artistTerm=Robbie%20%20Williams
