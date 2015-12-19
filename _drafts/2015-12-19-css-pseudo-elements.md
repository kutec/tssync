---
ID: 4506
post_title: Be Smart with CSS Pseudo Elements
author: Kushal Jayswal
post_date: 2015-12-19 13:34:15
post_excerpt: >
  Set of the CSS pseudo element is one of
  the CSS selector, which is actually not
  a part of DOM tree. Such elements opens
  the doors for extra stylings.
layout: post
permalink: http://teckstack.com/?p=4506
published: false
---
CSS holds the power to apply the styles on the HTML elements. These elements are part of the DOM tree structure. We can directly apply styles to the DOM elements but in CSS, we have various selectors to keep up consistent styling across the application. Set of the<strong> <a href="http://www.w3.org/TR/css3-selectors/#pseudo-elements" target="_blank">CSS pseudo element</a></strong> is one of the CSS selector, which is actually not a part of DOM tree. Such elements opens the doors for extra stylings.

[caption id="attachment_4147" align="alignright" width="367"]<img class="alignnone size-full wp-image-4147" src="http://teckstack.com/tsdir/wp-content/uploads/2014/11/Display-Advertising.jpg" alt="Advertisement Placeholder" width="367" height="256" /> Advertisement Placeholder[/caption]

Let's assume a real-time example, where we have <strong>multiple sections to show advertise for a Blog</strong>. Ads may have coming up dynamically, where we do not have flexibility to change the code.

In the image beside this paragraph is a real screenshot of <a href="http://teckstack.com">this blog</a>. The heading "Sponsors", we can add using pseudo elements.
<h2>:before</h2>
<iframe src="//jsfiddle.net/ft6syjvL/embedded/result,css" width="100%" height="300" frameborder="0"></iframe>
Above example is showing the use of <code>:before</code>. But, I am sure that you must come across a requirement, where you have to use <code>:before</code> and <code>:after</code> together.
<h2>:before and :after Together</h2>
[caption id="attachment_4657" align="alignright" width="300"]<img class="alignnone size-medium wp-image-4657" src="http://teckstack.com/tsdir/wp-content/uploads/2015/12/2-smartquotes.jpg" alt="Quoted Statement" width="300" height="218" /> Quoted Statement[/caption]

The common example is the <strong>quoted statements</strong> or testimonials on a web page. Quoted statement is the most emphasizing text on a page, which needs extra 1 or 2 elements for proper styling. As you can see in image, the size of the double quote symbols are bigger than the text size, which needs extra tags wrapping the <strong>" </strong>symbol.
<pre>&lt;blockquote&gt;
    &lt;span class="first-quote"&gt;&lt;/span&gt;
    &lt;span class="last-quote"&gt;&lt;/span&gt;
&lt;/blockquote&gt;</pre>
<code>&lt;blockquote&gt; </code>tag used for a quoted statement. But this is just another tag as <code>&lt;div&gt;</code>. And hence we required extra tags as mentioned in above code snippet to add <strong>"</strong> or image for double quote symbol. Of course, we can use <code>&lt;span&gt;</code> tags without classes and go with <code>:first-child</code> and <code>:last-child</code> instead. But that is again the same thing, adding up two extra tags. So, what is the solution?

We can use <code>:active</code> and <code>:before</code> elements together for an element. Below is a demo that how can we do so.
<div class="col-md-6"><strong>Without Pseudo Elements</strong>
<iframe src="//jsfiddle.net/k1270bkr/1/embedded/result,css,html/" width="100%" height="300" frameborder="0" allowfullscreen="allowfullscreen"></iframe></div>
<div class="col-md-6"><strong>With Pseudo Elements</strong>
<iframe src="https://jsfiddle.net/p8gkthoe/1/embedded/result,css,html/" width="100%" height="300" frameborder="0" allowfullscreen="allowfullscreen"></iframe></div>
<h2>:selection</h2>
<img class="size-full wp-image-4750 alignleft" src="http://teckstack.com/tsdir/wp-content/uploads/2015/12/How-to-Change-the-Default-Text-Selection-Color-with-CSS-in-Blogger1-e1450529744762.png" alt="CSS Selection" width="199" height="62" />Sometime, we need to copy and paste texts from a web page. While selecting text, we can see default blue background color with white font-color as stated in image beside. Well, there is a way, we can change this default styling using <code>:selection</code> pseudo element.

For our blog, we have used custom CSS effect using the same way.
<pre>:selection{
    background: #ffb;
    text-shadow: 1px 0 0 #000;
}</pre>
<h2>:first-letter</h2>
<img class="wp-image-4749 size-thumbnail alignright" src="http://teckstack.com/tsdir/wp-content/uploads/2015/12/2.1.7-decorative-initials1-e1450527715696-200x130.png" alt="Text Drop Cap" width="200" height="130" />If you like to read articles then you might have noticed the first letter of an article is bigger in size usually. Well, this is special styling we can do with <code>:first-letter</code> pseudo element. This doesn't require extra markup.
<iframe src="//jsfiddle.net/7t2fdLrL/embedded/result,css" width="100%" height="150" frameborder="0" allowfullscreen="allowfullscreen"></iframe>

<code>:first-line</code> is another pseudo element that used to apply CSS to the first line but this is less popular the list.
<pre><span class="highELE">p:first-line </span>{ 
<span class="highATT">    background-color:</span><span class="highVAL"> yellow;</span>
}
</pre>
<h3>Conclusion</h3>
There are lot many things, we can do with the use of pseudo elements. There is no boundary for the creativity. If you have better idea, please share the snippet below in <a href="#comments">comment area</a>.
<h4>Resources</h4>
<ul>
	<li><a href="http://www.w3.org/TR/css3-selectors/#pseudo-elements" target="_blank">W3C</a></li>
	<li><a href="http://nicolasgallagher.com/an-introduction-to-css-pseudo-element-hacks/" target="_blank">An introduction to CSS pseudo-element hacks</a></li>
</ul>