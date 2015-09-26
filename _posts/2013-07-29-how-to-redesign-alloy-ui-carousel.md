---
ID: 1952
post_title: How to Redesign Alloy UI Carousel
author: Kushal Jayswal
post_date: 2013-07-29 19:13:39
post_excerpt: >
  Focusing on "How to Redesign Alloy UI
  Carousel". I am experimenting with ICONS
  and RESPONSIVE design. You can even
  download the demo.
layout: post
permalink: >
  http://teckstack.com/how-to-redesign-alloy-ui-carousel
published: true
networkpub_postmessage:
  - ""
networkpub_postsummary:
  - ""
networkpub_twitterhandle:
  - ""
networkpub_twitterhash:
  - ""
networkpub_ogtype_facebook:
  - ""
networkpub_post_image_video:
  - ""
disclosure_dropdown:
  - None
disclosure_position:
  - Above the Content
dsq_thread_id:
  - "1545266239"
dcssb_short_url:
  - http://j.mp/17e0nuN
authorsure_hide_author_box:
  - ""
authorsure_include_css:
  - ""
views:
  - "2330"
post_views_count:
  - "0"
ac_is_copyprotect:
  - "1"
ac_is_advanced_tracking:
  - "1"
ac_postid:
  - 4HvJVGR7Thx.text
ac_is_process:
  - "1"
ac_embedid:
  - 1c5Enzej12C
vortex_system_likes:
  - "0"
vortex_system_dislikes:
  - "0"
---
<blockquote>Carousel (image rotation or slider) is such a thing you can find on 90% websites. The main reason to use carousel is to describe lot of stuffs with compact use of space. Today's topic is on redesigning the pre-developed module of Alloy UI, the Carousel.</blockquote>
<a class="btn btn-success" title="Download - AUI Carousel Redesign" href="http://demo.teckstack.com/aui-carousel-redesign/TeckStack.com(AUI_Carousel_Redesign_V1).zip" target="_blank">Download</a> <a class="btn btn-primary" title="DEMO - AUI Carousel Redesign" href="http://demo.teckstack.com/aui-carousel-redesign/" target="_blank">Demo</a>
<h3>What you will learn</h3>
<ol>
	<li>Initiate with Alloy UI</li>
	<li>Overwriting CSS for Module</li>
	<li>Targeting Node</li>
	<li>Override CSS</li>
</ol>
<h3>Prerequisites</h3>
<ul>
	<li>HTML</li>
	<li>CSS</li>
	<li>JavaScript or jQuery</li>
</ul>
<h2>What is Alloy UI</h2>
As the name says "Alloy UI" or in short "AUI" is a UI framework, built on YUI framwork. AUI provides ready-to-use component or module to develop rich and scalable application.
<h2>Alloy UI Carousel</h2>
AUI Carousel is ready-to-use module from AUI itself.

This is my first post in this category and I am going to focus on "How to Redesign Alloy UI Carousel". You can see the default look and feel here: <a href="http://alloyui.com/examples/carousel/" target="_blank">http://alloyui.com/examples/carousel/</a>.

AUI Carousel is very useful while we want to showcase something important elegantly with little use of space. We can rotate the images and content at the same place one-by-one circularly. Even we can control the rotation by clicking on Carousel's navigation controls.

Alloy UI provides fix width but I have tried with responsive one. Please comment me your suggestions.
<h3>AUI Carousel Navigation Controls</h3>
<ol>
	<li>Play and Pause Toggle control</li>
	<li>DOT Controls, means by default AUI generates the DOT as a number of sections or slides you add. And change the current section's DOT active by changing it's background-color to dark or light than others</li>
	<li>Next / Previous controls</li>
</ol>
<h2>Alloy UI Carousel Redesign</h2>
Now let me come to the main thing about changing the carousel icons with some content related icons OR images. By default AUI Carousel component has unique CSS class for <strong>Next</strong>, <strong>Previous</strong>, <strong>Play</strong> and <strong>Pause</strong>. But not for <span style="color: #ff6600;"><strong><em>DOT controls</em></strong></span>.
<h3>Changing DOT Controls with Image Icons</h3>
For this, you need to <em>add different class to each LI inside <strong>MENU</strong></em>. Here is the solution you may follow to do so.
<h3>The Carousel Structure</h3>
In this script I have targeted <strong>LI</strong> nodes and applied "<strong>css class</strong>" accordingly. CSS class names are simple and in numeric order for better understanding. You may use your own as well.

<strong>HTML</strong>

[gist]https://gist.github.com/kutec/cd9d43a57193421b57ce[/gist]

<strong>CSS</strong>

<span style="line-height: 1.5em;">For the elements which have been provided unique class by default, we can use them. So for those we do not need to add extra classes. But yes if we need some CSS change of course we should add, as I did for Next and Previous icon's LI.</span>

[gist]https://gist.github.com/kutec/475e817d6a5043d513e2[/gist]

<strong>SCRIPT</strong>

[gist]https://gist.github.com/kutec/bc6001e6b16b7e999d4b[/gist]

<strong></strong><strong style="line-height: 1.5em;">Icons Sprite</strong>

[caption id="attachment_1999" align="alignleft" width="70"]<img class="size-full wp-image-1999 " alt="icons" src="http://www.teckstack.com/wp-content/uploads/2013/07/icons.png" width="70" height="290" /> icons[/caption]

This is a group of icons as a single image called image sprite. Sprites can be used to improve the load performance and save bandwidth. It loads only single image once. Big brands like Google, Facebook, Yahoo, etc. all are using sprite images for their all project.

<a class="btn btn-success" title="Download - AUI Carousel Redesign" href="http://demo.teckstack.com/aui-carousel-redesign/TeckStack.com(AUI_Carousel_Redesign_V1).zip" target="_blank">Download</a> <a class="btn btn-primary" title="DEMO - AUI Carousel Redesign" href="http://demo.teckstack.com/aui-carousel-redesign/" target="_blank">Demo</a>

&nbsp;