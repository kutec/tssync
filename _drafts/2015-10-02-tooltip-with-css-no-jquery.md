---
ID: 4344
post_title: 'Let&#8217;s Create a Tooltip with CSS Only'
author: Manish Sharma
post_date: 2015-10-02 12:14:31
post_excerpt: ""
layout: post
permalink: http://teckstack.com/?p=4344
published: false
---
<blockquote>The Tooltip is a popular web component used to show informative content on user interaction. There are many ready-to-use jQuery plugins having tooltip functionality but plugins may load set of scripts and style sheets, which would result into downgrade the performance.</blockquote>
This article will focus on how to create a CSS tooltip. Means we are not going to use any JavaScript or jQuery code to achieve the tooltip functionality. It will be the CSS and HTML only doing the magic. So let's start!

<em>I am assuming that you are familiar with basic CSS and HTML. If not, Google it and feel comfortable.</em>
<h2>Brief about the Tooltip</h2>
As mentioned in the start, Tooltip is a functionality. If you google the keyword "tooltip" then you will find below definition.

[caption id="attachment_4349" align="aligncenter" width="549"]<img class="size-full wp-image-4349" src="http://teckstack.com/tsdir/wp-content/uploads/2015/10/tooltip-definition.png" alt="Tooltip Definition" width="549" height="187" /> Tooltip Definition[/caption]

Also, tooltip saves the space on a web page. In other words, we can call it an "infotip", which popping up with the content, while user hover on it.

The most common way to use a tooltip for any project is through jQuery plugin. But many front end developers prefer to write a custom code for small functionality like a tooltip.
<h2>The HTML Markup</h2>
<pre>&lt;div class="element-wrapper"&gt;
    &lt;label&gt;
        Label
        &lt;span class="tooltip-indicator"&gt;i&lt;/span&gt;
　　    &lt;div class="tooltip-box"&gt;Tooltip Opens up for TEXTBOX2&lt;/div&gt;
    &lt;/label&gt;
　　&lt;input type="text" placeholder="information..."/&gt;
&lt;/div&gt;</pre>
As per above code,
<ol>
	<li>We need a wrapper class <strong>element-wrapper </strong></li>
	<li><strong>tooltip-indicator</strong> is a graphical indicator for a tooltip</li>
	<li></li>
</ol>
&nbsp;

Here are the steps..

First we have to create wrapper of the element with this wrapper we can wrap up all need full content
Second We need Graphic pointer to indicate Tooltip
Third Tooltip element we need to be create where we can contain Tooltip information
Last but not the least CSS
for the styling and position of the Tooltip.

HTML code..
<pre>&lt;div class="element-wrapper"&gt;
    &lt;label&gt;
        Label
        &lt;span class="tooltip-indicator"&gt;i&lt;/span&gt;
　　      &lt;div class="tooltip-box"&gt;Tooltip Opens up for TEXTBOX2&lt;/div&gt;
    &lt;/label&gt;
　　    &lt;input type="text" placeholder="information..."/&gt;
&lt;/div&gt;
</pre>
asda