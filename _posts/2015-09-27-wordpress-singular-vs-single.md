---
ID: 4268
post_title: 'WordPress &#8211; Singular Vs. Single'
author: Kushal Jayswal
post_date: 2015-09-27 09:25:01
post_excerpt: >
  There are many conditional tags in
  WordPress. This article is all about
  difference between is_singular() and
  is_single().
layout: post
permalink: >
  http://teckstack.com/wordpress-singular-vs-single
published: true
ac_is_process:
  - "1"
ac_is_copyprotect:
  - "1"
---
The <a href="https://codex.wordpress.org" target="_blank" rel="nofollow">WordPress Codex</a> has very well documented for developers. However, there are few things you'll only face, while come to certain situation. There are many <a href="https://codex.wordpress.org/Conditional_Tags" target="_blank" rel="nofollow">conditional tags</a> in WordPress but some tags remain confusing to understand by their names. This article will focus on the difference between `is_singular()` and `is_single()`.

First, let's understand the terms and then we will see an example.
<h2>The Difference</h2>
[list icon="icon: check"]
<ul>
	<li><code>is_singular()</code> targets all templates with <strong>content-{something}.php</strong> files name in a theme. So if you have some code to manipulate with all single pages, then you should use <code>is_singular()</code>.</li>
	<li>On the other hand <code>is_single()</code> targets only <strong>single.php</strong> template, which meant to target only a single post page.</li>
</ul>
[/list]
<h2>An Example</h2>
For an example, you want to add <strong>social share icons</strong> without using a plugin. Below are some requirement:

[list icon="icon: check"]
<ul>
	<li>Icons should be visible for <strong>index.php</strong>, <strong>archive.php</strong> and <strong>single.php</strong> templates.</li>
	<li>Icons should not come for the <strong>page.php</strong> template.</li>
</ul>
[/list]

Here we have two options:
<ol>
	<li>We can directly put conditional check with <code>if( !is_page() )</code> for a function inside <strong>functions.php</strong> file or</li>
	<li>We have to use multiple conditional check as per below snippet</li>
</ol>
<pre>function someName($content) {
    if( is_single() || is_home() || is_archive() || is_search() ){
        // custom code...
    }
}
</pre>
Learning is everything. If you think there are still something you can add - kindly <a href="#comments" target="_blank">comment</a> below.
<h4>Resources</h4>
<ul>
	<li><a href="https://codex.wordpress.org/Function_Reference/is_singular" target="_blank" rel="nofollow">WordPress is_singular()</a></li>
	<li><a href="https://codex.wordpress.org/Function_Reference/is_single" target="_blank" rel="nofollow">WordPress is_single()</a></li>
	<li><a href="https://codex.wordpress.org/Function_Reference/is_page" target="_blank" rel="nofollow">WordPress is_page()</a></li>
	<li><a href="https://codex.wordpress.org/Conditional_Tags" target="_blank" rel="nofollow">WordPress Conditional Tags</a></li>
</ul>