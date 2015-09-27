---
ID: 4268
post_title: 'WordPress &#8211; Singular Vs. Single'
author: TeckStack Admin
post_date: 2015-09-27 08:39:14
post_excerpt: ""
layout: post
permalink: http://teckstack.com/?p=4268
published: false
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
	<li><em>is_singular()</em> targets all templates with <em>content-{something}.php</em> files name in a theme. So if you have some code to manipulate with all single pages, then you should use <em>is_singular()</em>.</li>
	<li>On the other hand <em>is_single()</em> targets only <em>single.php</em> template, which meant to target only a single post page.</li>
</ul>
[/list]
<h2>An Example</h2>
For an example, you want to add <strong>social share icons</strong> without using a plugin. Below are some requirement:

[list icon="icon: check"]
<ul>
	<li>Icons should be visible for <em>index.php</em>, <em>archive.php</em> and <em>single.php</em> templates.</li>
	<li>Icons should not come for the <em>page.php</em> template.</li>
</ul>
[/list]

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