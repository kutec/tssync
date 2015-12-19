---
ID: 4506
post_title: Be Smart with Pseudo Elements
author: Kushal Jayswal
post_date: 2015-12-19 10:35:31
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
<h2>:before</h2>
<iframe src="//jsfiddle.net/ft6syjvL/embedded/result,css" width="100%" height="300" frameborder="0"></iframe>
Above example is showing use of <strong>:before</strong>. But, I am sure that you must come across a requirement, where you have to use <strong>:before</strong> and <strong>:after</strong> together.
<h2>:before and :after Together</h2>
[caption id="attachment_4657" align="alignright" width="300"]<img class="alignnone size-medium wp-image-4657" src="http://teckstack.com/tsdir/wp-content/uploads/2015/12/2-smartquotes.jpg" alt="Quoted Statement" width="300" height="218" /> Quoted Statement[/caption]

The common example is the <strong>quoted statements</strong> or testimonials on a web page. Such a thing use to emphasize text block, which needs extra 1 or 2 elements for appropriate styling - to add double quote (<em>"</em>).

If we are not using pseudo element then we might need below structure.
<pre>&lt;blockquote&gt;
    &lt;span class="first-quote"&gt;&lt;/span&gt;
    &lt;span class="last-quote"&gt;&lt;/span&gt;
&lt;/blockquote&gt;</pre>
<strong>&lt;blockquote&gt; </strong>tag used for a quoted statement. But this is just another tag as <strong>&lt;div&gt;</strong>. And hence we required extra tags as mentioned in above code to add "double quotes" as in the image above. Of course, we can use <strong>&lt;span&gt;</strong> tags without classes and go with <strong>:first-child</strong> and <strong>:last-child</strong> instead. But that is again the same thing, adding up two extra tags. So, what is the solution?

We can use <strong>:active</strong> and <strong>:before</strong> elements together for an element. Below is a demo that how can we do so.
<div class="col-md-6"><iframe src="https://jsfiddle.net/k1270bkr/1/embedded/result/" width="100%" height="200" frameborder="0" allowfullscreen="allowfullscreen"></iframe></div>
<div class="col-md-6"><iframe src="//jsfiddle.net/p8gkthoe/embedded/result,css,html" width="100%" height="300" frameborder="0" allowfullscreen="allowfullscreen"></iframe></div>
sdfsdf