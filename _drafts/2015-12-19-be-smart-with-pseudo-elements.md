---
ID: 4506
post_title: Be Smart with Pseudo Elements
author: Kushal Jayswal
post_date: 2015-12-19 09:55:26
post_excerpt: ""
layout: post
permalink: http://teckstack.com/?p=4506
published: false
---
CSS holds the power to apply the styles on the HTML elements. These elements are part of the DOM tree structure. We can directly apply styles to the DOM elements but in CSS, we have various selectors to maintain consistent styling across the application.

Set of<strong> </strong>the<strong> pseudo element</strong> is one of the CSS selector, which is actually not a part of DOM tree. Such elements opens the doors for extra stylings for the DOM.

[caption id="attachment_4147" align="alignright" width="367"]<img class="alignnone size-full wp-image-4147" src="http://teckstack.com/tsdir/wp-content/uploads/2014/11/Display-Advertising.jpg" alt="Advertisement Placeholder" width="367" height="256" /> Advertisement Placeholder[/caption]

Let's assume a real time example, where we have <strong>multiple sections to show advertise for a Blog</strong>. Most of the time, such ads may be coming up dynamically, where we do not have flexibility to modify the code.

Beside image , "Advertisement Placeholder" is a real screenshot of <a href="http://teckstack.com">this blog</a>. The heading "Sponsors", we can add using pseudo element.
<h2>:Before</h2>
<iframe src="//jsfiddle.net/ft6syjvL/embedded/result,css" width="100%" height="300" frameborder="0"></iframe>
Above example is showing use of <strong>:before</strong>. But, I am sure that you must come across a requirement, where you have to use <strong>:before</strong> and <strong>:after</strong> together.

[caption id="attachment_4657" align="alignright" width="300"]<img class="alignnone size-medium wp-image-4657" src="http://teckstack.com/tsdir/wp-content/uploads/2015/12/2-smartquotes.jpg" alt="Quoted Statement" width="300" height="218" /> Advertisement Placeholder[/caption]

The common example is the <strong>quoted statements</strong> or testimonials on a web page. Such a thing use to emphasize text block, which needs extra 1 or 2 elements for appropriate styling - to add double quote (<em>"</em>).

If we are not using pseudo element then we might need below structure.
<pre>&lt;blockquote&gt;
    &lt;span class="first-quote"&gt;&lt;/span&gt;
    &lt;span class="last-quote"&gt;&lt;/span&gt;
&lt;/blockquote&gt;</pre>
<strong>&lt;blockquote&gt;</strong>tag used for a quoted statement.