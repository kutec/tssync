---
ID: 3759
post_title: Doctype
author: Manish Sharma
post_date: 2015-07-01 18:45:17
post_excerpt: ""
layout: webdocs
permalink: >
  http://teckstack.com/webdocs/html5/elements/d/doctype
published: true
wpcf-link-references:
  - http://google.com
---
<blockquote>HTML starts with tag. A longer name for DOCTYPE is Document Type. As the name suggests it helps browsers to validate and render HTML tags in proper way.</blockquote>
<h3>Syntax of the DOCTYPE and variation</h3>
<h2>HTML 5</h2>
<pre>&lt;!DOCTYPE html&gt;</pre>
As per W3C Publications for HTML, we can consider HTML 5 as the latest version for HTML.

HTML5 has a simple <span class="lang:default decode:true  crayon-inline">&lt;doctype&gt;</span>&nbsp;as mentioned in above code.
<h2>HTML 4</h2>
Previously we had HTML 4.01 version for HTML document.
Here <span class="lang:default decode:true  crayon-inline">&lt;doctype&gt;</span>&nbsp;is&nbsp;dependent on developers'&nbsp;mind or need of a project. We have&nbsp;multiple options available to&nbsp;declare a&nbsp; with different values.
<span style="color: #ff6600;"><em>User used to store doctype values somewhere in notepad or Googled it, but HTML5 has better doctype!</em></span>
<ol>
	<li>Strict</li>
	<li>Transitional</li>
	<li>Frameset</li>
</ol>
<h3>Strict</h3>
<pre>&lt;!DOCTYPE HTML PUBLIC "-//W3C//DTD HTML 4.01//EN" "http://www.w3.org/TR/html4/strict.dtd"&gt;</pre>
Strict doctype has some restrictions. We can use all HTML elements and attributes but not presentations or deprecated elements.
<h3>Transitional</h3>
<pre class="lang:xhtml decode:true">&lt;!DOCTYPE HTML PUBLIC "-//W3C//DTD HTML 4.01 Transitional//EN" "http://www.w3.org/TR/html4/loose.dtd"&gt;</pre>
Transitional doctype is little flexible and most used doctype with HTML4. We can use all HTML elements and attributes including those are restricted in Strict doctype.
<h3>Frameset</h3>
<pre>&lt;!DOCTYPE HTML PUBLIC "-//W3C//DTD HTML 4.01 Frameset//EN" "http://www.w3.org/TR/html4/frameset.dtd"&gt;</pre>
Frameset doctype is same as Transitional doctype, but here we can use frameset content, which is not allowed in Transitional type.