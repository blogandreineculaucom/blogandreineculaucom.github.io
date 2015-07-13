---
title: WordPress.com Stats
author: Andrei
layout: post
permalink: /2008/06/wordpresscom-stats/
categories:
  - Information Technology
  - Solution
tags:
  - blog
---
When you switch from a wordpress.com blog to a self-hosted one, you sort of miss the statistical information that you had from WordPress - number of visitors, most viewed posts, referrers, clicks, etc.

[One plugin][1] does just that. It allows you to have the same interface, same WordPress quality (the interface is the exact same one, hosted at wordpress.com) by registering your blog in their database.

The only downside to it, is that it tries to load the interface in an inner frame, which not only looks bad, but is a bit uneasy for the user.

So I decided for some code changes: instead of loading it with iframe, why not just redirect to it? You can then simply go back to your self-hosted dashboard through the Dashboard link.



**Changes to stats.php**:

<pre name="code" class="php:firstline[125]">function stats_reports_load() {
	//add_action('admin_head', 'stats_reports_head');
	stats_reports_page();
}
</pre>

<pre name="code" class="php:firstline[1138]">function stats_reports_page() {
	if ( isset( $_GET['noheader'] ) )
		return stats_dashboard_widget_content();
	$blog_id = stats_get_option('blog_id');
	$day = isset( $_GET['day'] ) && preg_match( '/^d{4}-d{2}-d{2}$/', $_GET['day'] ) ? "&day=$_GET[day]" : '';

	//echo "";
	wp_redirect("http://dashboard.wordpress.com/wp-admin/index.php?page=stats&blog=$blog_id$day");
}
</pre>

 [1]: http://wordpress.org/extend/plugins/stats/