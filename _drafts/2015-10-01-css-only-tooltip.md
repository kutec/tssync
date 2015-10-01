---
ID: 4344
post_title: CSS only Tooltip
author: Manish Sharma
post_date: 2015-10-01 13:08:41
post_excerpt: ""
layout: post
permalink: http://teckstack.com/?p=4344
published: false
---
In todays modern web development world Tooltip is a very popular element to show useful information.Even you can use the same
for the content which you don’t want to display to users all the time, user can simply click / hover on some of graphic icon or hover on the same
for the information.It is useful to save lots of space on webpage.

Tooltip is a important element
for web developments, so on the air lots of Third party plugins are available with different different approach, using HTML and CSS.

I have created my own
for latest project requirement, using the same HTML and CSS in a simple way without single line of script.

Here are the steps..

First we have to create wrapper of the element with this wrapper we can wrap up all need full content
Second We need Graphic pointer to indicate Tooltip
Third Tooltip element we need to be create where we can contain Tooltip information
Last but not the least CSS
for the styling and position of the Tooltip.

HTML code..

< div class = ”element - wrapper” > 　　 < label > 　　Label　　 < span class = ”tooltip - indicator” > i < /span>
　　<div class=”tooltip-box”>Tooltip Opens up for TEXTBOX2</div> 　　 < /label>
　　<input type=”text” placeholder=”information...” / /> < /div>