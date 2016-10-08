---
title: Organize Series for WordPress 2.6
author: Andrei
layout: post
categories:
  - Information Technology
  - Solution
tags:
  - blog
  - php
---
[My series plugin][1], that proved great so far, started to fail on me a bit after installing WordPress 2.6, but this evening I found some fixes.

One of the bugs is that the administration menus don't link correctly any longer.

Open **orgSeries.php**, and replace the function series\_organize\_options (line 156) with the following:



<pre name="code" class="php:firstline[156]">// ANDRIE
function series_organize_options() {
	global $wp_version;
	if (function_exists('add_options_page')) {
		if ( isset( $wp_version ) && $wp_version &gt;= 2.5 )
			add_options_page('Organize Series Options', 'Series Options', 9, SERIES_DIR . '/' . 'orgSeries-options-new.php');
		else
			add_options_page('Organize Series Options', 'Series Options', 9, SERIES_DIR . '/' . 'orgSeries-options.php');
	}
	if (function_exists('add_management_page'))
		add_management_page('Organize Series Management', 'Series', 9, SERIES_DIR . '/' . 'orgSeries-manage.php');
}
//END</pre>

Then there's another bug related to WordPress Revisions. If you have them [turned off][2], then things are ok. Otherwise, the plugin starts counting revisions as well as part of the series, which ends up with numbering gone wrong.

Open **series-taxonomy.php** and replace line 384

<pre name="code" class="php:firstline[384]">$post_ID = (int) $post_ID;</pre>

with the following

<pre name="code" class="php:firstline[384]">$post_ID = (int) $post_ID;
// ANDRIE
$post = get_post($post_ID);
if ($post-&gt;post_type == 'revision'){
return;
}
//END</pre>

This fix doesn't take care of the previous revisions though, that are already marked as part of the series. There is a fix for that as well, but that will be in an update to this post later this week ,)

 [1]: http://unfoldingneurons.com/neurotic-plugins/organize-series-wordpress-plugin
 [2]: http://blog.andreineculau.com/2008/07/delete-wordpress-26-revisions/