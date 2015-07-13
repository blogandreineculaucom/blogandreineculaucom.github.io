---
title: Gmail IMAP in Windows Mail/Outlook
author: Andrei
layout: post
permalink: /2007/11/gmail-imap-in-windows-mailoutlook/
categories:
  - Information Technology
  - Solution
tags:
  - email
---
Recently I have figured out the best way to have Gmail IMAP in Windows (Live) Mail/Outlook (Express).

Other than the [usual settings][1] you can do, there is something that it is not specified in the basic configuration. The Gmail IMAP inbox is structured to have Inbox, [Gmail], and other folders which are nothing else than your defined labels.

The way these Microsoft products are built, they do not allow to specify a special folder to point to [Gmail]X (a subfolder). Therefore you cannot link (tell Mail/Outlook) a special item (sent, deleted and junk) to point to your real folders, residing on the IMAP account.

But there is a.. semi-trick. Something that maybe it is not that obvious to start with. There's an option that says "Root folder path", under the IMAP tab of the Account properties window.

If you choose "[Gmail]" for that, deselect "Check for new messages in all folders", then select "Store special folders on IMAP server" and fill in with Sent Mail, Drafts, Trash, Spam - there you go.. you will see some nice usual folders in your Microsoft E-mail client. The only disadvantage is that you won't be able to take advantage of labeling (since the label folders are not made visible).

* This has been tried on Windows Live Mail

 [1]: http://mail.google.com/support/bin/topic.py?topic=12760