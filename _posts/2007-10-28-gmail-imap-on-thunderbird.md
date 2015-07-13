---
title: Gmail IMAP on Thunderbird
author: Andrei
layout: post
permalink: /2007/10/gmail-imap-on-thunderbird/
categories:
  - Information Technology
  - Solution
tags:
  - email
---
**[LATER EDIT] [Gmail IMAP has problems with interpreting 8bit messages][1]**

**[UPDATE] **[**Gmail has a new User Interface**][2]**. It looks faster (preloads messages), has a new Contacts Interface, and unfortunately breaks **[**Gcaldaemon**][3]**.**

For a week or so Gmail has enabled IMAP support. Although the basics are generally easy to make it work with Thunderbird, in order to get it to work flawlessly, you need to make some adjustments that aren't available off the Google Help.



  
After figuring out on my own what I need to do, I found the steps online written [here][4]:

> The [Gmail] folder has sub folders containing the your actual primary set of folders of your Gmail account (Inbox, Starred, Sent Mail, Drafts, All Mail, Spam & Trash). All your labels are shown as folders outside of this. There is an easy method to map your primary folders correctly to Gmail's, but doing so will deprive you of access to your labels (which show up as folders in Thunderbird).
> 
> So the cleanest way to map the folders is to do the following:
> 
> 1. In Thunderbird select Tools->Account Settings and select the account that you are using for Gmail IMAP.
> 
> 2. Select Copies & Folders under that.
> 
> 3. Sent Mail: Choose ‘Other' for the "When sending messages, automatically: " and from the drop down select "AccountName"->[Gmail]->Sent Mail
> 
> 4. Drafts: For drafts as well, choose "Other" and from the drop down select "AccountName"->[Gmail]->Drafts
> 
> 5. Spam: Select "Junk Settings", check the "Move junk messages to", select "Other" and from the drop down select "AccountName"->[Gmail]->Spam
> 
> This fixes most of your folders. The only remaining one is "Trash" and fixing this folder is a bit cumbersome, but it is worth it. By default Deleting a message does not send it to your Gmails "Trash" folder, instead it sends it to Thunderbirds Trash folder. The way IMAP is set up is that Thunderbirds Trash folder is mapped to [IMAP]/Trash on Gmail. So here are your options
> 
> 1. Let it remain as is and you will have an extra label called [IMAP]/Trash in Gmail, under which all your deleted mails will reside.
> 
> 2. If you want your deleted mails to be removed from your inbox, but still exist (in your ‘All Mails' section) then map your trash to ‘[Gmail]/All Mails'
> 
> 3. If you want your deleted mails to be removed from your inbox, and actually be trashed then map your trash to ‘[Gmail]/Trash'
> 
> (1) requires no further action on your part, but (2) & (3) are essentially the same thing, only differing in folder names.
> 
> So here's how you go about fixing your trash folder:
> 
> 1. Close Thunderbird
> 
> 2. Go to C:Documents and Settings<windows\_username>Application DataThunderbirdProfiles<profile\_name>, where <windows\_username> is your windows logon and <profile\_name> is the current Thunderbird profile you are using.
> 
> 3. Open prefs.js in your favorite text editor and search for a line that says  
> `user_pref("mail.server.server#.directory-rel", "[ProfD]ImapMail/imap.gmail.com");`
> 
> Here server# refers to your server number. Basically we have to find out which server number is being used for our Gmail IMAP
> 
> 4. Just below that line, add an additional line that says  
> `user_pref("mail.server.server#.trash_folder_name", "[Gmail]/Trash");`
> 
> 5. Startup Thunderbird again and your Trash folder below the Inbox should no longer be there. Instead it will use [Gmail]/Trash. If it does show up, then restart Thunderbird a couple of times until the Trash folder below the Inbox goes away. I have no clue why this happens, but this is a quirk I've noticed.
> 
> Now anything you delete would go to the actual Trash. If you wanted it archived instead of trashing it, specify [Gmail]/All Mail as the trash\_folder\_name.
> 
> Thunderbird should now be configured to properly work with Gmail's IMAP.

 [1]: http://groups.google.com/group/Gmail-POP-and-Forwarding/browse_thread/thread/696b8d03c8893c83/e254c725125ac9f4?#e254c725125ac9f4
 [2]: http://googlesystem.blogspot.com/2007/10/gmails-new-version-is-now-available.html
 [3]: http://gcaldaemon.sourceforge.net/
 [4]: http://blog.rameshbhaskar.com/2007/10/27/configuring-thunderbird-for-gmail-imap-the-way-it-should-be-done/