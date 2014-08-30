---
title: Pidgin and MSN (certificate error for omega.contacts.msn.com)
author: Andrei
layout: post
permalink: /2010/11/pidgin-and-msn-certificate-error-for-omega-contacts-msn-com/
categories:
  - I/Me/My
  - Information Technology
  - Solution
tags:
  - messenger
---
**UPDATE 2010-11-21 (the final solution for me)**

1.  Download these two files: [PEM#1][1] and [PEM#2][2] (part of UPDATE 2010-11-19 #2),  
    and rename them to  
    "Microsoft\_Secure\_Server\_Authority\_2010.pem" and  
    "Microsoft\_Internet\_Authority_2010.pem"
2.  Copy the above to files to "C:Program FilesPidginca-certs" on Windows,  
    or "/usr/share/purple/ca-certs/" on Linux  
    NB! folder location may vary
3.  [Download another file][3] (part of UPDATE 2010-11-19 #1)  
    and rename it to  
    "omega.contacts.msn.com"
4.  Copy the last file to "%APPDATA%.purple" on Windows  
    or "~/.purple" on Linux  
    NB! folder location may vary
5.  Now re-enable your MSN account, or just quit and restart Pidgin altogether.

**UPDATE 2010-11-19 #2 (not tested personally, but it's the solution that has been [uploaded for Pidgin's next update][4])**  
Download two certificate files ([no1][1] and [no2][2]) and copy them this time into your Pidgin installation folder, under "ca-certs" (probably "C:Program FilesPidginca-certs" on Windows, or /usr/share/purple/ca-certs/ on Linux).

**UPDATE 2010-11-19 #1  
**Seems like Microsoft changed the SSL certificate again... Or I don't know, but the situation looks more like there's a different SSL certificate depending on the connection?! I uploaded a second one that people can try. At this moment, I use one certificate on one computer, and the second certificate on another computer (another Internet connection). You can thus try with [the 2nd certificate][3].

-

This morning, people started to have problems with [Pidgin][5] and their MSN accounts.

Apparently, Microsoft changed something (i.e. SSL certificate) on their servers.

*   **<span style="text-decoration: line-through;"><a href="http://files.andreineculau.com/projects/pidgin/omega.contacts.msn.com.txt">Download this file (2010-11-18)</a> or </span>  
    **
*   **[Download this file (2010-11-19)][3]**,
*   **delete the ".txt" extension (or ".2.txt")**, so that you end up with **"omega.contacts.msn.com" only**,
*   **copy the file** to your "**.purple/certificates/x509/tls_peers**" folder ([which you can find like this on Windows][6] / which is in your home directory on Linux), **replacing the old "omega.contacts.msn.com" file**,
*   and finally
*   **Quit** (from the menu: Buddies -> Quit) and restart your Pidgin.

PS: to put minds at rest, the SSL certificate is taken from <https://omega.contacts.msn.com> . If you have the knowledge, you can download it yourself there, and follow the rest of the steps.

 [1]: http://developer.pidgin.im/viewmtn/revision/downloadfile/cd236baf6d00f3e1561a40974ce1828b793ea187/share/ca-certs/Microsoft_Secure_Server_Authority_2010.pem
 [2]: http://developer.pidgin.im/viewmtn/revision/downloadfile/cd236baf6d00f3e1561a40974ce1828b793ea187/share/ca-certs/Microsoft_Internet_Authority_2010.pem
 [3]: http://files.andreineculau.com/projects/pidgin/omega.contacts.msn.com.2.txt
 [4]: http://developer.pidgin.im/viewmtn/revision/info/cd236baf6d00f3e1561a40974ce1828b793ea187
 [5]: http://www.pidgin.im
 [6]: http://developer.pidgin.im/wiki/Using%20Pidgin#Whereismy.purpledirectory