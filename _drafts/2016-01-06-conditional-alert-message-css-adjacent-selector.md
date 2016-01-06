---
ID: 4755
post_title: >
  Conditional Alert Message with CSS
  Adjacent Selector
author: Kushal Jayswal
post_date: 2016-01-06 13:38:09
post_excerpt: ""
layout: post
permalink: http://teckstack.com/?p=4755
published: false
---
<span style="font-weight: 400;">There are many <a href="http://www.w3.org/TR/css3-selectors/" target="_blank">CSS selectors</a> we can apply style with but selectors like <a href="http://teckstack.com/css-pseudo-elements">Pseudo Elements</a>, Adjacent, ect. do the trick to minimize efforts that we had to spend on JavaScript.</span>

This article would focus on how we can use <a href="http://www.w3.org/wiki/CSS/Selectors/combinators/adjacent" target="_blank">CSS adjacent</a> to show an alert message conditionally. <span style="font-weight: 400;">Using adjacent selector, we can target very next element at the same level of elements sequence.</span>
<h2>Syntax of CSS Adjacent</h2>
&nbsp;

<span style="font-weight: 400;">I recently worked on an AngularJS project with a friend, where on-page </span><b>content search</b><span style="font-weight: 400;"> was the main feature. Also user can filter data rows based on various criteria. Below I am attaching a small version of the UI to make the project more clear.</span>

[caption id="attachment_4789" align="alignnone" width="768"]<img class="size-medium wp-image-4789" src="http://teckstack.com/tsdir/wp-content/uploads/2016/01/Rough-UI-768x421.png" alt="Rough UI - Concept IFIU" width="768" height="421" /> Rough Project Design (image-1)[/caption]

This article will focus on a small tip to show <span style="text-decoration: underline;">conditional alert message with CSS Adjacent selector</span>, which I came across during on <a href="http://ifiuse.com" target="_blank">ifiuse</a> project. Ifiuse built on AngularJS but you do not need to be expert to understand the example in terms of CSS adjacent.

&nbsp;