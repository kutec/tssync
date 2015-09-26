---
ID: 1845
post_title: Simple Login Popup with jQuery and CSS
author: Kushal Jayswal
post_date: 2013-05-19 07:52:32
post_excerpt: >
  There are many plugins available for
  Modal Popup. But writing own code for
  Login Popup with jQuery was excited. It
  is very simple and ready-to-use code
  with jQuery and CSS.
layout: post
permalink: >
  http://teckstack.com/simple-login-popup-with-jquery-and-css
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
  - "1298501893"
authorsure_include_css:
  - ""
authorsure_hide_author_box:
  - ""
quality_blog_tip_done1:
  - 'no'
quality_blog_tip_done2:
  - 'no'
quality_blog_tip_done3:
  - 'no'
quality_blog_tip_done4:
  - 'no'
quality_blog_tip_done5:
  - 'no'
quality_blog_tip_done6:
  - 'no'
quality_blog_tip_done7:
  - 'no'
quality_blog_tip_done8:
  - 'no'
quality_blog_tip_done9:
  - 'no'
quality_blog_tip_done10:
  - 'no'
quality_blog_tip_done11:
  - 'no'
quality_blog_tip_done12:
  - 'no'
quality_blog_tip_done13:
  - 'no'
quality_blog_tip_done14:
  - 'no'
quality_blog_tip_done15:
  - 'no'
quality_blog_tip_done16:
  - 'no'
quality_blog_tip_done17:
  - 'no'
quality_blog_tip_done18:
  - 'no'
quality_blog_tip_done19:
  - 'no'
quality_blog_tip_done20:
  - 'no'
quality_blog_tip_done21:
  - 'no'
quality_blog_tip_done22:
  - 'no'
quality_blog_tip_done23:
  - 'no'
quality_blog_tip_done24:
  - 'no'
quality_blog_tip_done25:
  - 'no'
views:
  - "7836"
post_views_count:
  - "0"
  - "0"
ac_is_copyprotect:
  - "1"
ac_is_advanced_tracking:
  - "1"
ac_postid:
  - 6HtgPUGVcrD.text
ac_is_process:
  - "1"
ac_embedid:
  - 5jXFntP6Tm4
vortex_system_likes:
  - "0"
vortex_system_dislikes:
  - "0"
---
There are many plugins available for Modal Popup. But writing own code for Login Popup with jQuery was excited. It is very simple and ready-to-use code with jQuery and CSS. You can also <a title="Fork on Github" href="http://kutec.github.io/ku-login-popup/" target="_blank">fork on Github</a>.

<strong>See in Action: </strong><a class="btn btn-success" title="Download Source" href="https://github.com/kutec/ku-login-popup/zipball/master" target="_blank">Download</a> <a class="btn btn-primary" title="View Demo" href="http://demo.teckstack.com/login-popup/" target="_blank">Demo</a>
<h3>Prerequisite</h3>
<ul>
	<li>HTML</li>
	<li>CSS</li>
	<li>JavaScript / jQuery</li>
</ul>
<h2>Simple Requirement</h2>
Create a Modal Popup for login in such a way that disabled everything while open. Means user will not able to click anywhere except Login Form or content except inside the popup.
<h3>HTML</h3>
<pre class="lang:default decode:true " title="HTML">&lt;div class="ar login_popup"&gt;
    &lt;a class="button" href="#" &gt;Login&lt;/a&gt;        
 
    &lt;div class="popup"&gt;
        &lt;a href="#" class="close"&gt;CLOSE&lt;/a&gt;
        &lt;form&gt;
            &lt;P&gt;&lt;span class="title"&gt;Username&lt;/span&gt; &lt;input name="" type="text" /&gt;&lt;/P&gt;
            &lt;P&gt;&lt;span class="title"&gt;Password&lt;/span&gt; &lt;input name="" type="password" /&gt;&lt;/P&gt;
            &lt;P&gt;&lt;input name="" type="button" value="Login" /&gt;&lt;/P&gt;
        &lt;/form&gt;
    &lt;/div&gt;
&lt;/div&gt;</pre>
&nbsp;
<h3>CSS</h3>
<pre class="lang:default decode:true " title="CSS">.button {
	display: inline-block;
	background: #000;
	padding: 5px 10px;
	z-index: 0;
	color: #fff;
}
 
.overlay {
	z-index: 5;
	background: rgba(0, 0, 0, .50);
	display: block;
	position: fixed;
	width: 100%;
	height: 100%;
}
 
.popup {
	padding: 10px 10px 35px;
	background: #fff;
	z-index: 999;
	display: none;
	position: absolute;
	right: 0;
}</pre>
&nbsp;
<h3>jQuery</h3>
<pre class="lang:default decode:true" title="jQuery">$(document).ready(function() {
    $(".button").click(function(e) {
        $("body").append(''); $(".popup").show(); 
        $(".close").click(function(e) { 
            $(".popup, .overlay").hide(); 
        }); 
    }); 
});</pre>