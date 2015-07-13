---
title: PHP and register_globals ON!!!
author: Andrei
layout: post
permalink: /2006/05/php-and-register_globals-on/
categories:
  - Information Technology
  - Solution
tags:
  - developer
  - php
---
**Context**: register_globals is a configuration flag for PHP, inside php.ini that that instructs PHP to take all the variables sent to the script through GET, POST, etc. to be registered as PHP variables

**Example**: you access info.php?day=5. Inside this script, with register\_globals turned On, you can test like this: if ($day == 5) {…}. If you have it Off, then you should do this: if ($\_GET['day'] == 5) {…}

**Advice**: turn if Off. It is the default for PHP 5 and higher! Why? It is a security whole letting visitors inject variables into your code, and in turn, while it first makes your job easier, you get less secure code! Therefore, if you are a good programmer, you will spend more time testing and improving security.

If you use a webhost that has this setting turned On, then ask them to help you turn it Off for your website, or even better convince them to turn it Off for every client. THIS SETTING IS OBSOLETE STARTING WITH PHP 5, and will NOT EXIST IN PHP 6 AT ALL!!!

If the webhost is running PHP as an Apache module, then you can simply create a .htaccess file and fill it with "php\_flag register\_globals 0". On Apache 2 this will not work, but give an Internal Server Error. It has to be put by your host in the VirtualHost handler for your website.

If you really want to stick with that specific webhost, and there's no solution to turn it Off (i.e. they are running PHP as CGI) use the code bellow.

**Explanation**: it will first take all global variables, and unset everything that shouldn't be there. Do not worry about your code still being accesible for changes (i.e. info.php?\_ENV[OS]=NewOS ). The PHP queue works like this: first it registers variables from GET, etc. and then it fills in the global variables \_GET, _POST, etc. (I wonder why the hack they are not READ ONLY!) Therefore you will have the correct associative arrays, without any injected modification.

[sourcecode language="php"]if (ini\_get('register\_globals')){  
foreach($GLOBALS as $s\_variable\_name => $m\_variable\_value){  
if (!in\_array($s\_variable_name, array('GLOBALS', 'argv',  
'argc', '\_FILES', '\_COOKIE', '\_POST', '\_GET', '_SERVER',  
'\_ENV', '\_SESSION', '_REQUEST',  
's\_variable\_name', 'm\_variable\_value')  
)){  
unset($GLOBALS[$s\_variable\_name]);  
}  
}  
unset($GLOBALS['s\_variable\_name']);  
unset($GLOBALS['m\_variable\_value']);  
}  
[/sourcecode]

**Links**:  
<http://ro2.php.net/manual/en/security.globals.php>  
<http://en.wikibooks.org/wiki/Programming:PHP:Register_Globals>  
<http://www.sitepoint.com/print/php-security-blunders>  
[http://www.simiandesign.com/blog-fu/2004/08/php\_register\_gl.php][1]  
<http://www.securephpwiki.com/index.php/Global_Variables>  
<http://www.filipdewaard.com/php/real-life-php-security-breach/>

* the above code is not mine. I found it on the Internet, while I was looking for a solution.

[LATER EDIT]  
Switched to WordPress's sourcecode tag

 [1]: http://www.simiandesign.com/blog-fu/2004/08/php_register_gl.php