---
title: A developer's review of webligo's SocialEngine
author: Andrei
layout: post
categories:
  - Dislikes
  - Information Technology
tags:
  - cms
  - css
  - developer
  - html
  - javascript
  - php
  - sql
---
I will start with a humble *mea culpa* , making it clear that the following are my opinions (put together during some lunch breaks) and not a carefully written review. I'm doing this because there is actually no minimum review of this product.

I've started engaging with webligo's [SocialEngine][1] 2-3 months ago. SocialEngine is a social network framework that allows users to deploy a self-hosted social network, that wants to be easy to customize. The end goal of my job related to SocialEngine was to customize it according to some rather small requirements. This is what I can tell you after these months:

**1. Context** - It is important to state from the beginning why my team and I went ahead with SocialEngine. The frameworks that aid building a self-hosted social network are not many, apply some filters like +php +mysql +mvc -cms and you end up with one, if I'm not mistaken. There's [BuddyPress][2] (built on WordPress) , and I-dont-recall-the-name built on Drupal, and many others but I said no to general CMS. There's also [Elgg][3] , but when you end up looking at the source code (especially the code of plugins), you realize that the software is loose. [Diaspora][4] is promising, but it will be a long time before it comes out as a trustworthy platform. Today I read about [Anahita][5], but it is also a baby. Long story short, there is simply no good social network platform out there that keeps it simple with PHP&MySQL support. Please tell me if I'm wrong.

**2. Architecture**

<p style="padding-left: 30px;">
  2.1. SocialEngine is based on <a href="http://zendframework.com">Zend Framework</a>. Hurray! Except, if you read a few reviews online, Zend Framework is not a MVC platform, but more of a MVC helper if you will. It gives you too much freedom, not leading you (you=a ZF newbie).
</p>

<p style="padding-left: 30px;">
  2.2. SocialEngine uses MooTools for javascript. Hurray, some of you might say. Except, if you start coding with MooTools, after knowing the magic you can do with jQuery, you end up in a disgraceful situation. MooTools has its advantages, but overall, especially when you end up using some plugins.. Uff!
</p>

<p style="padding-left: 30px;">
  2.3. SocialEngine should use Smarty - ref <a href="http://www.socialengine.net/support/faq#faq38">http://www.socialengine.net/support/faq#faq38</a> yet it does NOT. Advantages and disadvantages occur. The negative part is that the templates being to look (not just visually) less of templates, and more like code.
</p>

<p style="padding-left: 30px;">
  2.4. SocialEngine uses <a href="https://github.com/sunny/csscaffold">sunny's CSScafold</a> and again Hurray! This time it is a true hurray! Coding big apps without a CSS platform is pain in the.. But SocialEngine uses the platform just for some folder parsing and CSS include. So you end up loading a library for nothing.
</p>

**3. Documentation** - none! They say that the code has comments, but I can tell you that that's not enough, and that the comments are sparse and sometimes are copied from other parts, with little connection to what lies below the comment.

**4. Communication**

<p style="padding-left: 30px;">
  4.1 Support - they give you 30 days support when you purchase a license, yet they always put "we are overloaded, it can take a while for us to give feedback to your ticket". Furthermore, it's only support for errors. 2nd furthermore - there is no way to see other tickets and to leave comments.
</p>

<p style="padding-left: 30px;">
  4.2. Censorship - you will now say that I don't know what I'm talking about, BUT please try to find one negative comment on their blog. I left a couple of comments, perfectly well-written and respectful, related to the blog posts, and the comments did not get approved. If you search online, there are quite many communities. It gives you a clear sense that this product is well known. Despite that, on each community you will see that people seek help for errors, plugins, etc. and almost no answer. My humble conclusion is that there are not many developers using SE, but just simple users that want to deploy their own social network.
</p>

<p style="padding-left: 30px;">
  4.3. Blog posts importance - they will post and wish you a Happy New Year, but they will not post about a security issue. Instead they just mention (inside the <a href="http://www.socialengine.net/blog/article?id=119&article=Happy-New-Year">Happy New Year post</a>) that the issue has been fixed (God knows how long ago that issue had been noticed).
</p>

<p style="padding-left: 30px;">
  4.4. Twitter - their twitter account is mostly dead, rarely answering mentions and rarely posting helpful things. You'd think that developers of a social network take communication seriously..
</p>

<p style="padding-left: 30px;">
  4.5. Email - my team and I wrote them at some point and asked them if they are willing to collaborate on strengthening the platform's code. There was no money or attribution involved, but we just wanted to make sure that future upgrades will not break our fixes. We knew early in our development cycle that we will notice&kill security & other issues, which did happen. No answer.
</p>

**5. Source code**

<p style="padding-left: 30px;">
  5.0 Legacy. This first bullet-point is not related to SocialEngine v4, but v3. Back in those times, all the code was in one big folder, and with little if any OOP in mind. Judge for yourselves.
</p>

<p style="padding-left: 30px;">
  5.1. Think twice, speak once. One can see that there is a lot of human and intellectual resources being deployed into SocialEngine. No doubt about it. Work is work and should be appreciated for what it is. Yet it's another thing when you see code being copy-pasted instead of going with modular programming. That reflects both in PHP, HTML, CSS code and database structure. When does a good developer stop doing that in their evolution cycle?
</p>

<p style="padding-left: 30px;">
  5.2. CSS - each module has its own CSS, as if saying "don't touch, private property". Good, although it is fairly easy to override due to CSScafold's features. The template's CSS covers should cover non-modular styles. If you want to modify the CSS adequately and get out of their design box, you will spend a lot just to properly put the CSS code (one file per template, one file per module) in smaller files. Then even longer to eliminate redundant CSS code, which then leads to the need of eliminating redundant PHP code (e.g. widgets: Event's Profile Photos is the same with Group's Profile Photos).
</p>

<p style="padding-left: 30px;">
  5.3. One can clearly notice that SE developers do not have a sense of uniform coding practices. Compare the Controller.php from the Event's Profile Photos (or Discussion) with the one from the Group module. Even if they are doing the same thing, the newer one has more checks and filters (striptags, canPost, etc). One can also find comments like "does this work like this?", or "this could break if.."
</p>

<p style="padding-left: 30px;">
  5.4. I will stop here for now, and maybe update the post at a later time with source-code crap. Bottom line is that modules do not communicate properly with each other, and that after these 2-3 months, I am still "refurbishing".
</p>

<p style="padding-left: 30px;">
  5.5. Don't fix it if it ain't broken. I fully agree, but what do you do when you go ahead with a product, especially when building a community, and then you get in deep shit because of poorly written code, getting errors or bumping into security issues? Am I then supposed to say that it's not my fault, that I'm looking into it and not knowing how long it will take, etc? Communities are not that stable as one might think. They need to be nurtured, and a good way to start doing just that is provide a good home for them. Fixing a home before people come live in it is much easier than fixing it when people live there.
</p>

**Disclaimer**

<p style="padding-left: 30px;">
  My intent is not to trash the developers, nor the product, but to provide a singular opinion (or not, if other people concur with what I wrote) on this product and its team's practices from a developer point of view. It could be that if you are a simple customer, and you do not want to customize its core, then it is a very good product. In SocialEngine's defense, a simple and powerful argument for the product's strong position on the market is that I'm still going forward with it. The question is: for how long?
</p>

 [1]: http://www.socialengine.net
 [2]: http://buddypress.org
 [3]: http://elgg.org
 [4]: http://www.joindiaspora.com
 [5]: http://www.anahitapolis.com/about/anahita-social-engine