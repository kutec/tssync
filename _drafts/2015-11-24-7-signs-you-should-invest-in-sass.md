---
ID: 4419
post_title: 7 Signs You Should Invest In Sass
author: Kushal Jayswal
post_date: 2015-11-24 10:54:32
post_excerpt: ""
layout: post
permalink: http://teckstack.com/?p=4419
published: false
---
<blockquote>Writing CSS is an easy task. But doing the same in proper manner, which can be understood by any developer in a team that is more important.</blockquote>
Before you start a project with [Sass], you should understand that how it can help for CSS authoring. Sass stands for “Syntactically Awesome Style sheets” and people using Sass won’t disagree on the statement. Today major projects demand for media query and branding options and from the experience I found Sass as one of the best solution.

For a big projects, writing pure CSS to manage everything becomes hectik sometime and here in pre-processor comes in a picture. [Configuring Sass] is not too tough. If you don’t want to configure manually then you can use tools listed on the site. I personally love [Skout] for HTML projects and [WP-SCSS] for WordPress. Liferay has <code>@compass</code> built-in, so you can directly start writing Sass with importing of compass at the top of the <code>.scss</code> file.

Related article: Understand Liferay Theme Structure

This article will focus on some of the most used features of the Sass with some easy-to-understand examples.
<h3>First Thing First - Why Sass</h3>
Well, the CSS is one an important asset for any front end developer, agree?. But today’s developer believe in smart work, not hard work. Hence the adoption ratio of pre-processor is too high. People used to it now. Sass is popular in this category. It can reduce the burden of writing and managing stuffs with some cool techniques. It comes with set of meaningful features.
<h3>What I Can Do with Sass</h3>
I remember that when I first heard about pre-processor, I couldn’t convince that why should we use Sass and how it can save lot of time and efforts. Let’s elaborate one by one with the list below.

If you have any question, kindly add your comment below. I would try to get over it soon.
<ul>
	<li>Improved Branding</li>
	<li>Clubbing &amp; Nesting</li>
	<li>Partials &amp; Importing</li>
	<li>Extending</li>
	<li>Including</li>
	<li>Functioning</li>
	<li>Community Aspect</li>
</ul>
<h2>Improved Branding</h2>
Giving default branding options, which can be configurable from control panel or backed of the site, is one of the important thing for any large project.

In simple term “Branding” means color options. Admin/user can change site’s background, font color dynamically. This seems pretty much simple if we go with CSS class approach. But if I have 4-5 different color options then you can imagine that how many number of lines it will take.

Just like JavaScript <code>variable</code>, in Sass you can also define variables and use across the web.
<pre><code>$variableName: value;
</code></pre>
Variable increases the efficiency. Like for above example where you have 4-5 color options to be configured as a branding options, you can define 5 different variables and assign color properties to each. So in future if you have to change any color for branding, you can simply change through changing variable’s value and it will change the color for all CSS where it the same variable has been used.
<h2>Clubbing &amp; Nesting</h2>
Initially I started using Sass because of Nesting only. Infect from the start of my career I wanted to group CSS in block manner. But with pure CSS we can only add comments.