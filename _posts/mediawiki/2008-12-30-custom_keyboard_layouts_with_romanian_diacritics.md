---
title: Custom Keyboard Layouts with Romanian Diacritics
author: mediawiki
layout: post
categories:
  - Uncategorized
---
{| align="right"  
|-  
| [[Image:Romanian Diacritics.png|center]]  
Diacritics make a language what it actually is.

|-  
| \_\_TOC\_\_  
|}

## Introduction

"'Romanian has a handful (and I mean exactly 5) of diacritics"'. And because we have been put to the test in the 90s and adapted, nowadays we are very much accustomed to see text even without diacritics and we can still read it without major problems. The issue has a long story and doesn't make the case of this article.

With time, diacritics and Romanian keyboards have made it to general consumers though and it has been imposed in public administration. We have seen [http://secarica.ro/html/s-uri\_si\_t-uri.html the fights for that] and the improvements in the way the Windows OS handles the Romanian diacritics, may it be [http://secarica.ro/html/info\_winvista.html Vista] or [http://secarica.ro/html/ro\_keyboard.html fixes to versions prior to Vista].

Yet, there is one more issue that remains. And that is something related to globalization.

Nowadays you buy laptops. And laptops that are being built for the region where you live in, outside Romania, or a region that you are now visiting and has discounts.

So here you are, in UK for example, buying a laptop and you notice that when you switch the keyboard layout to Romanian, it is impossible to know which key is which.

Romanian keyboard layout is based on the US keyboard layout, so a US physical keyboard is quite easy to manage with a Romanian keyboard layout. But a UK physical keyboard, or a Swedish one will be problematic, because the keys are differently placed.

"'This is where I come in"'. I admit that my practice breaks rules and standards. Nevertheless keeping only to standards and rules may be counter-productive.

I have built some keyboard layouts that give access to the Romanian diacritics, while still respecting the basic arrangement of the physical keyboard - may it be Swedish/Finnish, British, French, Italian or Spanish.

## Swedish/Finnish

This is the keyboard layout that I am using daily, since my laptop has a Swedish keyboard. I have added Polish diacritics during [http://desiderius.wordpress.com my Erasmus student experience in Poland].

This keyboard layout strongly resembles "'Romanian (Standard)"', in regards to how it handles Romanian diacritics.

"'Basics"' - keeps all the Swedish/Finnish keys, except the following:

*Ã¶ becomes È (s with "'comma"')  
*Ã¤ becomes È (s with "'comma"')  
*Ã¥ becomes Ä  
*Â¨ becomes Ã®  
*' becomes Ã¢  
*Â´ becomes '  
\*\` (Shift + Â´) becomes \*

In "'detail"':

*AltGr + e builds â¬  
*AltGr + c builds Â©  
*AltGr + Ã¶ builds Å (s with "'cedilla"' - legacy)  
*AltGr + Ã¤ builds Å£ (t with "'cedilla"' - legacy)  
*Â´ is now a dead key only in combination with AltGr + Â´  
*\` is now a dead key only in combination with AltGr + Shift + Â´  
*Â¨ is now a dead key only in combination with AltGr + Â¨  
*^ is now a dead key only in combination with AltGr + Shift + Â¨  
*~ is now a dead key only in combination with AltGr + '

"'Polish"' features:

*AltGr + p becomes a dead key, allowing for the Polish Programmers layout to kick in  
*z, x, c, n, a, s, l, e, o, after typing and releasing AltGr + p, will become Å¼, Åº, Ä, Å, Ä, Å, Å, Ä, Ã³

This driver will install a keyboard layout under the name "'Swedish - Romanian (Standard), Romanian (Legacy) [AltGr], Polish (Programmers) [deadkey]"'

*"'AltGr"' because it allows "'Legacy"' diacritics with cedilla - Å and Å£ - by pressing AltGr+Ã¶ and AltGr+Ã¤  
*"'deadkey"' because you can have the "'Polish (Programmers)"' layout with the use of a dead key

\[[Image:Keyboard Se.png|400px|Before]\] \[[Image:Keyboard Se Ro.png|400px|After\]]

\[[Image:Keyboard Se Shift.png|400px|Before (Shift)]\] \[[Image:Keyboard Se Shift Ro.png|400px|After (Shift)\]]

\[[Image:Keyboard Se Altgr.png|400px|Before (AltGr)]\] \[[Image:Keyboard Se Altgr Ro.png|400px|After (AltGr)\]]

### Download

[http://files.andreineculau.com/projects/romanian-diacritics/ropl4swe.zip Download Swedish/Finnish Layout with Romanian Diacritics]

## Italian

This keyboard layout strongly resembles "'Romanian (Programmers)"', in regards to how it handles Romanian diacritics.

"'Basics"' - keeps all the Italian keys, except the following AltGr combinations:

*AltGr + s builds È (s with "'comma"')  
*AltGr + t builds È (t with "'comma"')  
*AltGr + a builds Ä  
*AltGr + i builds Ã®  
*AltGr + q builds Ã¢

This driver will install a keyboard layout under the name "'Italian - Romanian (Programmers)"'

\[[Image:Keyboard It Altgr.png|400px|Before (AltGr)]\] \[[Image:Keyboard It Altgr Ro.png|400px|After (AltGr)\]]

### Download

[http://files.andreineculau.com/projects/romanian-diacritics/ro4it.zip Download Italian Layout with Romanian Diacritics]

## French

This keyboard layout strongly resembles "'Romanian (Standard)"' by the use of AltGr, in regards to how it handles Romanian diacritics.

"'Basics"' - keeps all the French keys, except the following AltGr combinations:

*AltGr + ; builds È (s with "'comma"')  
*AltGr + ' builds È (t with "'comma"')  
*AltGr + [ builds Ä  
*AltGr + ] builds Ã®  
*AltGr + # builds Ã¢

This driver will install a keyboard layout under the name "'French - Romanian (Standard) [AltGr]"'

\[[Image:Keyboard Fr Altgr.png|400px|Before (AltGr)]\] \[[Image:Keyboard Fr Altgr Ro.png|400px|After (AltGr)\]]

### Download

[http://files.andreineculau.com/projects/romanian-diacritics/ro4fr.zip Download French Layout with Romanian Diacritics]

## Spanish

This keyboard layout strongly resembles "'Romanian (Programmers)"', in regards to how it handles Romanian diacritics.

"'Basics"' - keeps all the Spanish keys, except the following AltGr combinations:

*AltGr + s builds È (s with "'comma"')  
*AltGr + t builds È (t with "'comma"')  
*AltGr + a builds Ä  
*AltGr + i builds Ã®  
*AltGr + q builds Ã¢

This driver will install a keyboard layout under the name "'Spanish - Romanian (Programmers)"'

\[[Image:Keyboard Es Altgr.png|400px|Before (AltGr)]\] \[[Image:Keyboard Es Altgr Ro.png|400px|After (AltGr)\]]

### Download

[http://files.andreineculau.com/projects/romanian-diacritics/ro4es.zip Download Spanish Layout with Romanian Diacritics]

## United Kingdom

This keyboard layout strongly resembles "'Romanian (Standard)"' by the use of AltGr, in regards to how it handles Romanian diacritics.

"'Basics"' - keeps all the United Kingdom keys, except the following AltGr combinations:

*AltGr + ; builds È (s with "'comma"')  
*AltGr + ' builds È (t with "'comma"')  
*AltGr + [ builds Ä  
*AltGr + ] builds Ã®  
*AltGr + # builds Ã¢

This driver will install a keyboard layout under the name "'United Kingdom - Romanian (Standard) [AltGr]"'

\[[Image:Keyboard Uk Altgr.png|400px|Before (AltGr)]\] \[[Image:Keyboard Uk Altgr Ro.png|400px|After (AltGr)\]]

### Download

[http://files.andreineculau.com/projects/romanian-diacritics/ro4uk.zip Download United Kingdom Layout with Romanian Diacritics]

\[[Category:Projects]\] \[[Category:IT\]]