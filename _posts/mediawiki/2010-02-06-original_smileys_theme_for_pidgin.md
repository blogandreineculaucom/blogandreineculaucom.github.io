---
title: Original Smileys Theme for Pidgin
author: mediawiki
layout: post
permalink: /2010/02/original_smileys_theme_for_pidgin/
categories:
  - Uncategorized
---
{| align="right"  
|- valign="top"  
| \_\_TOC\_\_  
| <center>
  1.9 - 2010-02-06
</center>

  
[[Image:Original Smileys Theme.png|center]]  
<addhtml>

<hr style="width:150px" />

<hr style="width:150px" />
<fb:fan profile_id="107286711570" stream="1" connections="10" width="200"></fb:fan>
  
</addhtml>  
|}</p> 
# Abstract

The "'birth"': September 2007.

The "'scope"': \[http://www.pidgin.im Pidgin\] (multi-protocol messenger).

The "'innovation"': use the original emoticons/smileys of their respective messenger/protocol - Yahoo!, AIM, ICQ, etc.

The "'reasoning"': if emoticons show emotions, then different drawings show different emotions, no matter how many similarities they share.

The "'technical common-sense"': emoticons have grown to be proprietary to the protocol. So it is common-sense that when you are using a certain protocol to communicate, you use its emoticons too.

The "'e-collaboration principle"': WYSIWIS (What-you-see-is-what-I-see).

# Messengers/Protocols Supported

*[[wikipedia:Aol\_Instant\_Messenger|AIM]]  
*[[wikipedia:Gadu-Gadu|Gadu-Gadu]]  
*[[wikipedia:Google_Talk|Google Talk]]  
**hidden emoticons (all visible)  
**round emoticons  
**square emoticons  
**colored emoticons  
*\[[wikipedia:Facebook|Facebook]\] (requires the [http://code.google.com/p/pidgin-facebookchat/ Facebook Chat plugin for Pidgin])  
*[[wikipedia:ICQ|ICQ]]  
*[[wikipedia:Windows\_Live\_Messenger|MSN/Live!/WLM]]  
**hidden emoticons (all visible)  
**support for [http://code.google.com/p/msn-pecan/ MSN Pecan] plugin  
**support for [http://sipe.sourceforge.net/ Microsoft OCS/LCS] plugin  
*[[wikipedia:MySpaceIM|MySpaceIM]]  
*[[wikipedia:IBM\_Lotus\_Sametime|Sametime]]  
*\[[wikipedia:Skype|Skype]\] (requires the [http://eion.robbmob.com/ Skype plugin for Pidgin])  
**hidden emoticons (all visible, except the flags)  
**support for D-Bus plugin  
*\[[wikipedia:Tencent_QQ|Tencent QQ/Messenger]\] (experimental; looking for feedback!)  
*\[[wikipedia:Tlen.pl|Tlen.pl]\] (thanks to Kasper Wieczorek)  
*[[wikipedia:Yahoo!_Messenger|Yahoo!]]  
**hidden emoticons (all visible)  
**big emoticons

<google>HEADING</google>

# Download

*[http://files.andreineculau.com/projects/pidgin/original-smileys/pidgin-original-latest.tgz Latest Version]  
*[http://files.andreineculau.com/projects/pidgin/original-smileys/ Browse legacy Versions]

# Installation

*Open Pidgin, click "Tools "from the main menu, then "Preferences "(or simply Ctrl+P in the Pidgin window)  
*Go to the "Smiley Themes" tab  
*Drag and drop the downloaded "tgz" archive (i.e. pidgin-original-x.x.x.tgz), or click "Add "and point to the archive  
*Select "Original Smileys" from the list, and click OK

If you want to install the smileys for all users, read how to do it in the [[#FAQ]] Section.

# Roadmap & Changelog

Excerpt from changelog.txt included with the download.

<pre># ROADMAP
# - find a way to switch between smiley versions
# - all GTalk smileys should be transparent (I don't have the time for it. Anyone?)
# - some GTalk smileys loop forever (I don't have the time for it. Anyone?)
#
# version 1.9
# - fixed notworthy and ohgoon under Yahoo Big (swap needed)
# - changed indicator from "Microsoft OCS/LCS" to "Office Communicator"
# - added some GTalk smileys and improved some others thanks to Edward Deutsch &lt;edward.deutsch@gmail.com>
#
# version 1.8
# - added Facebook penguin smiley
# - fixed some Skype smileys
# - fixed tancze Gadu-Gadu smiley
# - added NateOn (http://nateon.haz3.com/ or http://code.google.com/p/nateonpidginbranch/) smileys thanks to Matthew McCorry &lt;mccorry@gmail.com>
#
# version 1.7
# - added Facebook shark smileys
# - fixed transparency for some Facebook smileys
# - added Microsoft OCS/LCS smileys - http://sipe.sourceforge.net/
#
# version 1.6
# - moved smileys in pidgin-original-default to pidgin-originaldefault for consistency
# - improved MSN smileys thanks to Chris Baker - http://www.chrisbaker.ca/
# - improved GTalk colored smileys thanks to Aditya Pandya
# - improved theme file
# - corrected Yahoo9 Big typo
#
# version 1.5
# - fixed Facebook missing emoticons
</pre>

<google>HEADING</google>

# FAQ

## TGZ

Even if 0.8.3+ versions have changed to TGZ format (instead of ZIP), this doesn't make the theme UNIX specific. You can install it the same way under Windows too. The file it is still an archive and you can easily convert it to ZIP, if you feel like it, by using many archive converters (e.g. like the freeware [http://archivconvert.sourceforge.net/ ArcConvert] for Windows).

## Transparency Issues

On dark backgrounds, you may notice that the smileys are not perfectly transparent. Stop wining about it! First of all, a light background is perfectly fine. The fact that you want a dark background is your issue! If you have the time and knowledge to improve the transparency of the smilies, you're most welcome to do it on your own and then send me some updates.

## Duplicate themes

If you had the 0.8.2 or lower version, after you performed the "easy installation" of newer versions, you might find yourself with "duplicate" Original Smileys themes. One is the new version, one is the old version. That is because previous versions were being installed for all users, while the "easy installation" (drag & drop) performs the installation in the user's profile. Read below if you want to perform an [[#Installation\_for\_All_Users]]. - In order to delete the old version, installed for all users, you must

#"'Exit Pidgin!"' (not just the Buddy List Window)  
#First, you need to "'find out where Pidgin is installed"' on your system.  
On "Windows" systems, the default path is C:Program FilesPidgin . You can also just right click the Pidgin shortcut, and you will see to which path it points to (without pidgin.exe or pidgin-portable.exe) .  
On "UNIX" systems, the default path is /usr/lib/purple .  
OK, so whatever path you found, "'we will call it {Pidgin_install}"'.  
#Go to  
"Windows" systems: {Pidgin_install}pixmapspurpleemotes  
"UNIX" systems: "'{Pidgin_install}/pixmaps/purple/emotes/"'  
#"'Delete any folder starting with "pidgin-original""'

## Installation for All Users

There is no "easy installation" (drag and drop) for all users, but it's not that hard either.

#"'Exit Pidgin!"' (not just the Buddy List Window)  
#First, you need to "'find out where Pidgin is installed"' on your system.  
On "Windows" systems, the default path is C:Program FilesPidgin . You can also just right click the Pidgin shortcut, and you will see to which path it points to (without pidgin.exe or pidgin-portable.exe) .  
On "UNIX" systems, the default path is /usr/lib/purple .  
OK, so whatever path you found, "'we will call it {Pidgin_install}"'.  
#Secondly, you need to "'find a way to decompress the TGZ archive"' you've just downloaded. For Windows systems, read the above [[#TGZ]]  
#"'Copy (decompress) the contents of the archive"' to  
"Windows" systems: {Pidgin_install}pixmapspurpleemotes  
"UNIX" systems: "'{Pidgin_install}/pixmaps/purple/emotes/"'  
#Make sure you delete the theme installed in the user's (or users') profile. Read the above [[#Duplicate_themes]]

<google>HEADING</google>

# Interested in my Pidgin setup?

If you want to know the outline of my Pidgin setup, go [[:My Pidgin Setup|here]] and see my graphics and plugins that I use.

\[[Category:Projects]\] \[[Category:IT\]] [[Category:Pidgin]]