---
ID: 4755
post_title: >
  Conditional Alert Message with CSS
  Adjacent Selector
author: Kushal Jayswal
post_date: 2016-01-06 15:24:20
post_excerpt: ""
layout: post
permalink: >
  http://teckstack.com/conditional-alert-message-css-adjacent-selector
published: true
---
<span style="font-weight: 400;">There are many <a href="http://www.w3.org/TR/css3-selectors/" target="_blank">CSS selectors</a> we can apply style through but selectors like <a href="http://teckstack.com/css-pseudo-elements">Pseudo Elements</a>, Adjacent, etc. do the trick to reduce efforts on JavaScript. </span>This article would focus on how we can use <a href="http://www.w3.org/wiki/CSS/Selectors/combinators/adjacent" target="_blank">CSS adjacent selector</a> to show an alert message box, conditionally. <span style="font-weight: 400;">Using adjacent selector, we can target very next element at the same level of elements sequence.</span>
<h2>Syntax of CSS Adjacent</h2>
<pre>#table-header + .alert-message{
    display: block;
}</pre>
<h2>The Discussion</h2>
<span style="font-weight: 400;">I recently worked on an AngularJS project with a <em>Manish Sharma</em>, where on-page </span><b>content search</b><span style="font-weight: 400;"> was the main feature. Also user can filter data-rows based on various criteria. Below I am attaching a draft version of the design to make my words more clear.</span>

[caption id="attachment_4789" align="alignnone" width="768"]<img class="size-medium wp-image-4789" src="http://teckstack.com/tsdir/wp-content/uploads/2016/01/Rough-UI-768x421.png" alt="Rough UI - Concept IFIU" width="768" height="421" /> Rough Project Design (image-1)[/caption]

As you can see, above screenshot has a header with <em>number of checkbox filters</em> and <em>a dropdown</em> <em>(for even more available filters)</em>. The next is a search textbox and below that we have a table with heading and data in rows.

Now, if we follow the above image and search for the text term "Content 4", then we will be getting not data in a table. And as per the requirement, this is when we have to show an alert box/message. Below screenshot will help you to understand the scenario:

[caption id="attachment_4791" align="alignnone" width="768"]<img class="size-medium wp-image-4791" src="http://teckstack.com/tsdir/wp-content/uploads/2016/01/Rough-UI-no-data-found-768x236.png" alt="Rough UI no data found - Concept IIU" width="768" height="236" /> No Data Found (image-2)[/caption]
<h2>The Solution</h2>
Let's think on HTML structure first. As we have to target using CSS adjacent selector, we must have all elements (that we want to play with) at the same level. We can count on 3 elements for our needs.
<ol>
	<li>Table Header (<code>#table-header</code>) - <em>image-1</em></li>
	<li>Table Data (<code>#data</code>) - <em>image-1</em></li>
	<li>Alert Message Box (<code>.alert-message</code>) - <em>image-2</em></li>
</ol>
Recall the <a href="#Syntax_of_CSS_Adjacent">syntax</a> once and get clear idea that why we have to use all elements sequentially. If you have any doubts, please post a <a href="#comments">comment</a> below.
<h3>Demo</h3>
As of now, I am embedding same kind of DEMO where search functionality created using another jQuery plugin but the purpose is as same to understand the approach.
<p class="codepen" data-height="247" data-theme-id="0" data-slug-hash="GoWxGX" data-default-tab="result" data-user="kutec">See the Pen <a href="http://codepen.io/kutec/pen/GoWxGX/">GoWxGX</a> by Kushal Jayswal (<a href="http://codepen.io/kutec">@kutec</a>) on <a href="http://codepen.io">CodePen</a>.</p>
<script src="//assets.codepen.io/assets/embed/ei.js" async=""></script>

AngularJS completely hide the element if the search criteria doesn't match but here I have other demo which hides child elements. So I had to use <code>:empty</code> selector to achieve the goal. But we are not going to focus on that now and I will try to put another demo with AngularJS soon.

If you have any query or doubts, please <a href="#comments">comment</a> below OR you can share better examples as well.

&nbsp;