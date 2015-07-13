---
title: Delete WordPress 2.6 Revisions
author: Andrei
layout: post
permalink: /2008/07/delete-wordpress-26-revisions/
categories:
  - Information Technology
  - Solution
tags:
  - blog
  - sql
---
WordPress 2.6 introduces [revisions][1] to each post.

That actually caused my series plugin to break down, but that was fixed by me with two edits.

But the main part is that.. weirdly.. the WordPress team didn't put an option to disable these, as they can create useless data records. I, for one, like the feature, but I don't see myself using that.

It's neat for publishers and multi-user blogging, when people review and edit and add photos, etc.. one person at a time. But when there's just one person doing it.. it's close to useless. I couldn't care less how this post looked like one day or one month ago..

So the only way to turn the feature off is to edit your **wp-config.php** file and put

<pre name="code" class="php">define ('WP_POST_REVISIONS', 0);</pre>

But what about those revisions left in your database? [Several][2] [posts][3] look as if they found the true answer, but it's one of those "The one who laughs last, laughs best" situations. Didn't those people hear about post meta? Or about post terms (tags, categories, or series?! )? (No offense intended, just disappointment..)

Here's the proper way to clean your MySQL DB for WordPress from post revisions.



<pre name="code" class="sql">DELETE a,b,c
FROM wp_posts a
LEFT JOIN wp_term_relationships b ON (a.ID = b.object_id)
LEFT JOIN wp_postmeta c ON (a.ID = c.post_id)
WHERE a.post_type = 'revision'</pre>

This should be all. And luckily, there's no typo..

 [1]: http://wordpress.org/development/2008/07/wordpress-26-tyner/
 [2]: http://lesterchan.net/wordpress/2008/07/17/how-to-turn-off-post-revision-in-wordpress-26/
 [3]: http://www.mydigitallife.info/2008/07/22/how-to-delete-existing-wordpress-post-revisions-storedsaved/