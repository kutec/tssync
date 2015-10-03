---
ID: 4344
post_title: 'Let&#8217;s Create CSS Only Tooltip'
author: Manish Sharma
post_date: 2015-10-03 10:00:29
post_excerpt: >
  This article will focus on how to create
  a CSS only tooltip. We will not use any
  JavaScript or jQuery code to achieve the
  tooltip functionality.
layout: post
permalink: http://teckstack.com/?p=4344
published: false
---
<blockquote>The Tooltip is a popular web component used to show informative content on user interaction. There are many ready-to-use jQuery plugins having tooltip functionality but plugins may load set of scripts, which would result into downgrade the performance.</blockquote>
This article will focus on how to create a CSS only tooltip. Means we are not going to use any JavaScript or jQuery code to achieve the tooltip functionality.

<em>I am assuming that you are familiar with basic CSS and HTML. If not, Google it and feel comfortable.</em>
Github: <a class="btn btn-success" href="http://kutec.github.io/CSS-Tooltip" target="_blank">Demo</a> or <a href="https://github.com/kutec/CSS-Tooltip" target="_blank">Fork</a>.
<h2>Brief about the Tooltip</h2>
As mentioned in the start, Tooltip is a functionality. If you google the keyword "tooltip" then you will find below definition.

[caption id="attachment_4349" align="aligncenter" width="549"]<img class="size-full wp-image-4349" src="http://teckstack.com/tsdir/wp-content/uploads/2015/10/tooltip-definition.png" alt="Tooltip Definition" width="549" height="187" /> Tooltip Definition[/caption]

Also, tooltip saves the space on a web page. In other words, we can call it an "infotip", which popping up with the content, while user hover on it.

Let's see the code now, to achieve CSS only tooltip...
<h2>The HTML Markup</h2>
<pre>&lt;div class="tooltip"&gt;
    &lt;p&gt;
        &lt;a href="#" class="tooltip-indicator"&gt;Tooltip top&lt;/a&gt;
        &lt;span class="tooltip-box" tip-dir="top"&gt;Tooltip from &lt;strong&gt;TOP&lt;/strong&gt; direction&lt;/span&gt;
    &lt;/p&gt;
&lt;/div&gt;</pre>
As per above code,
<ol>
	<li>We need a wrapper class <code>tooltip </code></li>
	<li><code>tooltip-indicator</code> is coded for a tooltip</li>
	<li><code>tooltip-box </code>is a container for tooltip content. This will be hidden by default and while use hover on <code>tooltip-indicator it simply popped up</code></li>
	<li>You might have noticed <code>tip-dir="top"</code>. It decides from which direction tooltip will be shown up. In code above, we have <strong>top</strong>, so it will be coming up from top position. If we change it to <code>tip-dir="bottom"</code>, it behaves accordingly.</li>
</ol>
Related Article:
<ul>
	<li><a href="http://teckstack.com/understand-css-positions" target="_blank">Understand CSS Positions</a></li>
	<li><a href="http://teckstack.com/jquery-tooltip" target="_blank">jQuery Tooltip - The Accordion Concept</a></li>
</ul>
<h2>CSS</h2>
We have used CSS3 properties for bouncy animation effect and also have some selectors like <code>.tooltip-box[tip-dir="top"] </code>to change the position of tooltip container as per user preference.
<pre>.tooltip {
	display: inline-block;
	position: relative;
	margin: 38px;
	width: 83px;
	opacity: 1;
	z-index: 1;
}
.tooltip-indicator:hover + .tooltip-box{
	opacity: 1;
	visibility: visible;
	transform: translate3d(0px, 0px, 0px);
	-webkit-transform: translate3d(0px, 0px, 0px);
	-moz-transform: translate3d(0px, 0px, 0px);
} 
.tooltip-box{
	background: #f5f5f5;
	border: solid 1px #ccc;
	border-radius: 5px;
	padding: 10px;
	width: 230px;
	position: absolute;
	visibility: hidden;
	-ms-filter: "progid:DXImageTransform.Microsoft.Alpha(Opacity=0)";
	filter: progid:DXImageTransform.Microsoft.Alpha(Opacity=0);
	opacity: 0;
	-webkit-transition: 
	  opacity 0.2s ease-in-out,
		visibility 0.2s ease-in-out,
		-webkit-transform 0.2s cubic-bezier(0.71, 1.7, 0.77, 1.24);
	-moz-transition:    
		opacity 0.2s ease-in-out,
		visibility 0.2s ease-in-out,
		-moz-transform 0.2s cubic-bezier(0.71, 1.7, 0.77, 1.24);
	transition:         
		opacity 0.2s ease-in-out,
		visibility 0.2s ease-in-out,
		transform 0.2s cubic-bezier(0.71, 1.7, 0.77, 1.24);
	-webkit-transform: translate3d(0, 0, 0);
	-moz-transform:    translate3d(0, 0, 0);
	transform:         translate3d(0, 0, 0);
	pointer-events: none;
}

/****** top and bottom ******/
.tooltip-box[tip-dir="top"], .tooltip-box[tip-dir="bottom"] {
	left: 50%;
	margin:-15px 0 10px -115px;
}
.tooltip-box[tip-dir="top"]:before, .tooltip-box[tip-dir="bottom"]:before {
	content: '';
	position: absolute;
	bottom: -10px;
	left: 50%;
	width: 0;
	height: 0px;
	border-left: solid 8px transparent;
	border-right: solid 8px transparent;
	margin-left: -9px;
}
/****** top ******/
.tooltip-box[tip-dir="top"]{
	bottom: 100%;
	transform: translateY(-12px);
	-webkit-transform: translateY(-12px);
	-moz-transform: translateY(-12px);
}
.tooltip-box[tip-dir="top"]:before{
	bottom: -10px;
	border-top: solid 9px #ccc;
}
/****** bottom ******/
.tooltip-box[tip-dir="bottom"] {
	top: 100%;
	transform: translateY(12px);
	-webkit-transform: translateY(12px);
	-moz-transform: translateY(12px);
}
.tooltip-box[tip-dir="bottom"]:before {
	top: -10px;
	border-bottom: solid 9px #ccc;
}

/****** left and right ******/
.tooltip-box[tip-dir="left"], .tooltip-box[tip-dir="right"]{
	top: 50%;
	margin-top: -33px;
}
.tooltip-box[tip-dir="left"]:before,.tooltip-box[tip-dir="right"]:before {
	content: '';
	position: absolute;
	top: 50%;
	width: 8px;
	height: 0px;
	border-top: solid 8px transparent;
	border-bottom: solid 8px transparent;
	margin-top: -8px;
}
/****** left ******/
.tooltip-box[tip-dir="left"]{
	right: 100%;
	transform: translateX(-12px);
	-webkit-transform: translateX(-12px);
	-moz-transform: translateX(-12px);
	text-align:right
}
.tooltip-box[tip-dir="left"]:before {
	right: -10px;
	border-left: solid 9px #ccc;
}
/****** right ******/
.tooltip-box[tip-dir="right"]{
	left: 100%;
	margin-left:9px;
	transform: translateX(12px);
	-webkit-transform: translateX(12px);
	-moz-transform: translateX(12px);
	text-align:left
}
.tooltip-box[tip-dir="right"]:before{
	left: -10px;
	border-right: solid 9px #ccc;
}
</pre>
Github: <a class="btn btn-success" href="http://kutec.github.io/CSS-Tooltip" target="_blank">Demo</a> or <a href="https://github.com/kutec/CSS-Tooltip" target="_blank">Fork</a>.