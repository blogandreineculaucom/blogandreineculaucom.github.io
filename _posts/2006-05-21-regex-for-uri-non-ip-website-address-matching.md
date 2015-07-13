---
title: RegEx for URI (non IP) (website) matching
author: Andrei
layout: post
permalink: /2006/05/regex-for-uri-non-ip-website-address-matching/
categories:
  - Information Technology
  - Solution
tags:
  - developer
---
I've been trying to find a relatively good regular expression, but there wasn't one that did the trick for me.

My 2 hours work led me here (join lines before use):

<pre width="50">(?:(?:http(s)?://)|(www.))
((?:(?:(?:w|-|_)+.)+)(?:[a-z]{2,5}))
((?:/(?:(?:(?:(?:w|-|_)+.)*
(?:w|-|_)+/?)*))*)
(?(?:S*))?</pre>

* * *Let's take it step by step:</p> 

`(?:(?:http(s)?://)|(www.))`  
$1 - gives HTTP's security  
$2 - gives "www." or null

`(((?:(?:(?:w|-|_)+.)+)(?:[a-z]{2,5}))`  
$3 - gives the domain name, sometimes without "www."

`((?:/(?:(?:(?:(?:w|-|_)+.)*<br />
(?:w|-|_)+/?)*))*)`  
$4 - gives the path & filename

`(?(?:S*))?`  
$5 - gives parameters, preceeded by "?"

**Comments**:

*   Yes, I know. It only works for HTTP. Can be easily changed, but I needed it just like this, in order to replace it with a HTML link. You change it to your needs.
*   Domain name tries to be restrictive: the last domain part can be between 2 and 5 characters of length ("museum" is the longest one)
*   The address cannot end in a dot "." unless it is the address for a script that takes parameters
*   Parameters can only be "restricted" to have only non-spaced characters
*   The address starts with the "http://" or with "www." . Any other address does not match.

Now playing: **Black Eyed Peas Feat. Justin Timberlake - Where is the love**