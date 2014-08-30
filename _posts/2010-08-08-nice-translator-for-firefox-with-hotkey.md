---
title: Nice Translator for Firefox (with Hotkey)
author: Andrei
layout: post
permalink: /2010/08/nice-translator-for-firefox-with-hotkey/
categories:
  - Information Technology
  - Solution
tags:
  - browser
---
The Nice Translator Firefox Extension is an adaptation of the original [Nice Translator website][1].

It allows a user to translate into multiple languages at a time, as they type right from within a website. Select text and immediately have it translated with just a few clicks.

But there's a problem. Because it was designed for selected-text translation, the only way to access it is to right-click a page: no hotkey, no toolbar button.

Since it's a really good language tool, today, I've spent a few minutes to make this compatible with Firefox 3.* and add a hotkey to [the original Firefox extension (ver. 0.3)][2] - Ctrl+Q.

[Click to download - Nice Translator (with Hotkey) 0.3][3]

PS: if you are not ok with this key combination, you can just

1.  download the .xpi (right click, Save as...)
2.  rename the .xpi file to .zip
3.  edit the file within named *chrome/content/ntff.js* and change line 114 to suite  your needs
4.  rename back to .xpi
5.  drag-and-drop the changed file on Firefox

 [1]: http://nicetranslator.com/
 [2]: https://addons.mozilla.org/en-US/firefox/addon/11458/
 [3]: http://files.andreineculau.com/projects/firefox/nice_translator_w_hotkey.0.3.xpi