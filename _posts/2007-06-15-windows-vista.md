---
title: Windows Vista
author: Andrei
layout: post
permalink: /2007/06/windows-vista/
categories:
  - Information Technology
  - Solution
tags:
  - windows vista
---
Here goes my experience of installing Windows Vista. I decided to give it a try (x64 version), so inevitably there were things to "learn".

First of all, if there's a need to mention this... No way to get it installed on a USB external HDD.

Secondly... installation was as smooth as possible.

But here go the problems:

> I have no idea why, but **installing Adobe Flash ActiveX was a pain in the ass**.  
> It may have been because I disabled *User Access Control* and then didn't restart immediately, but every time I tried to install the ActiveX I ended up with the *Information Bar* in IE7 saying "Your security settings do not allow..., and having only "More Information" on right-click.  
> Having IE7 as loose as possible, it was still impossible to install it.  
> Upon restart, having no UAC, it worked this time.

> **Managing partitions and previous folders.**  
> I must describe how my system was built:one partition - XP system, one partition - personal data (documents, music, etc.) All "My *" folders were in D:Documents (My Documents folder). At the end of the HDD, there was some unallocated space (for Vista).  
> A "big" problem came up - upon booting Vista, the 3rd partition becomes C:, the first one becomes D:, and the 3rd one becomes E:. Since most of the settings of small programes (Winamp, Winace, etc.) which were installed on the former D: had referenced to D: inside their .ini files, it was a problem - now D: was simply my former C:.  
> Changing drive letters was impossible, because D: was considered a system partition, and you cannot do anything about it.  
> But there's a very very fine solution, which many of you "loosers" (joke :p) don't know about. NTFS works with "*virtual folders*" (in UNIX - *Symbolic Links*), meaning that you can create a folder that will "transparently work" on another folder. All from reading to writing.  
> Therefore, recreate folders "*Documents*", "*Winace*", "*Winamp*" on the former C: (now D:) and create the links to the former D: (now E:).  
> I know, I know... I didn't forget: the software that helps you do that is called [SHJunction][1]. Enjoy and use carefully! :)

> What else?... Well.. **Winamp**! Winamp doesn't have full support for Vista. It works, but it has issues. One of them is that you need the some *VC++ Runtime Libraries*. Download them from [here ][2]and place the dlls where you have *winamp.exe*.  
> The other thing is that if you have shared settings (you have Winamp settings in a one directory, and not specific to each user), then you will notice that upon installation Winamp doesn't ask you about that. It has some issues detecting if it can have shared settings or not.  
> The solution comes from *SHJunction *again. After installing Winamp, in the "*Documents and Settings{user}Application Data*" you will notice a new directory "Winamp". Just empty that and create a link to the folder where you have the shared Winamp settings. Done!

> **DivX**. Another type of issue. But also related to dlls. The "Register Products" don't work. For that, you need to download *PX.DLL* from [here][3], and copy it to "*WindowsSysWOW64*", and copy *dpuGUI11.dll* and *dtu100.dll* from "*WindowsSysWOW64*" to "*WindowsSystem32*". Done!

More to come as I "learn".

> **UPDATE - Process Explorer**  
> If you are so wicked that you replaced your Task Manager with *Process Explorer*, then on Vista you might have a problem. When you hit "*Replace Task Manager*", not only it doesn't happen but, but you can't run even the old Task Manager by taskbar right-click or Ctrl-Alt-Del. What happens is that Process Explorer can't match the path to *procexp.exe* . So.. open *regedit*, go to *HKEY\_LOCAL\_MACHINESOFTWAREMicrosoftWindows NTCurrentVersionImage File Execution Optionstaskmgr.exe* and edit *Debugger* so that it is the full path to the *procexp.exe* . Close regedit and give it a try. It works!

 [1]: http://www.bitsum.com/shjunc.asp
 [2]: http://stashbox.org/18587/msvcp71.zip
 [3]: http://www.dll-files.com/dllindex/dll-files.shtml?px