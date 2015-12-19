---
ID: 4506
post_title: Be Smart with Pseudo Elements
author: Kushal Jayswal
post_date: 2015-12-19 08:50:06
post_excerpt: ""
layout: post
permalink: http://teckstack.com/?p=4506
published: false
---
CSS holds the power to apply the styles on the HTML elements. These elements are part of the DOM tree structure. We can directly apply styles to the DOM elements but in CSS, we have various selectors to maintain consistent styling across the application.

Set of<strong> </strong>the<strong> pseudo element</strong> is one of the CSS selector, which is actually not a part of DOM tree. Such elements opens the doors for extra stylings for the DOM.

[caption id="attachment_4147" align="alignright" width="367"]<img class="alignnone size-full wp-image-4147" src="http://teckstack.com/tsdir/wp-content/uploads/2014/11/Display-Advertising.jpg" alt="Advertisement Placeholder" width="367" height="256" /> Advertisement Placeholder[/caption]

Let's assume a real time example, where we have <strong>multiple sections to show advertise for a Blog</strong>. Most of the time, such ads may be coming up dynamically, where do not have flexibility to modify the code.

"Advertisement Placeholder" is a real screenshot of <a href="http://teckstack.com">this blog</a>. The heading "Sponsors", we can add using pseudo element.
<div class="styles-section-title styles-selector">
<div><span class="selector"><span class="simple-selector selector-matches">#wp125adwrap_2c:before</span></span> {</div>
<div><span class="webkit-css-property">content</span>: <span class="value">"Sponsors"</span>;</div>
</div>
<ol class="style-properties monospace" tabindex="0">
	<li><input class="enabled-button" type="checkbox" /> <span class="webkit-css-property">font-size</span>: <span class="value">24px</span>;</li>
	<li class="parent"><input class="enabled-button" type="checkbox" /> <span class="webkit-css-property">padding</span>: <span class="value styles-panel-hovered">0 5px</span>;</li>
	<li class=""><input class="enabled-button" type="checkbox" /> <span class="webkit-css-property">margin-top</span>: <span class="value">20px</span>;</li>
	<li><input class="enabled-button" type="checkbox" /> <span class="webkit-css-property">margin-bottom</span>: <span class="value">10px</span>;</li>
</ol>
<div>}</div>
&nbsp;