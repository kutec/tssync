---
ID: 4268
post_title: 'WordPress &#8211; Singular Vs. Single'
author: TeckStack Admin
post_date: 2015-09-27 07:24:07
post_excerpt: ""
layout: post
permalink: http://teckstack.com/?p=4268
published: false
ac_is_process:
  - "1"
ac_is_copyprotect:
  - "1"
---
<blockquote>The <a href="https://codex.wordpress.org" target="_blank" rel="nofollow">WordPress Codex</a> has very well documented for developers. However, there are few things you'll only face, while come to certain situation. There are many <a href="https://codex.wordpress.org/Conditional_Tags" target="_blank" rel="nofollow">conditional tags</a> in WordPress but some tags remain confusing to understand by their names. This article will focus on the difference between `is_singular()` and `is_single()`.</blockquote>
First, let's understand the term and then we will see an example.
<h2>The Difference</h2>
To make it simple, I would say `is_singular()` targets all the templates with `content-{something}.php` files name in your theme.

On the other hand `is_single()` targets the only `single.php` template.
<h2>Example</h2>
For an example, you want to add *social share icons* without using a plugin.
<ul>
	<li>These icons should be visible for `index.php`, `archive.php` and `single.php` templates.</li>
	<li>It should not come for the `page.php` template.</li>
</ul>
Here we have two options:
<ol>
	<li>We can directly put conditional check with `!is_page()` or</li>
	<li>We have to use multiple conditional check as per below snippet</li>
</ol>
<pre>function someName($content) {
    if( is_single() || is_home() || is_archive() || is_search() ){
        // custom code...
    }
}
</pre>
sdfsdf