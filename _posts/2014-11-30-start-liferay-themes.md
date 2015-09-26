---
ID: 3024
post_title: Start with Liferay Themes
author: Kushal Jayswal
post_date: 2014-11-30 12:04:30
post_excerpt: ""
layout: post
permalink: >
  http://teckstack.com/start-liferay-themes
published: true
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
  - "4089"
dsq_thread_id:
  - "3276314498"
post_views_count:
  - "3"
ac_is_copyprotect:
  - "1"
ac_is_advanced_tracking:
  - "1"
ac_postid:
  - 58HZpAWTLqN.text
ac_is_process:
  - "1"
ac_embedid:
  - 2k4NaCKFH1l
vortex_system_likes:
  - "1"
vortex_system_dislikes:
  - "0"
vortex_system_user_21:
  - 'a:2:{s:5:"liked";s:7:"noliked";s:8:"disliked";s:8:"disliked";}'
---
<blockquote>Few months back Liferay has been released its new <a title="Liferay 6.2" href="http://www.liferay.com/documentation/liferay-portal/6.2/user-guide" target="_blank">version 6.2</a>. It has numbers of new features and being a UI developer, I must consider the <strong>responsive behavior</strong> as a plus factor. Yes! Liferay 6.2 comes with the <a title="Twitter Bootstrap" href="http://getbootstrap.com" target="_blank">Twitter Bootstrap</a> CSS to make it responsive. But on the other side for components still it's dependent on <a title="Alloy UI" href="http://alloyui.com" target="_blank">Alloy UI</a>.</blockquote>
This article will talk about Liferay Theme Architecture. So let's start with the introduction.
<h2>Introduction</h2>
I got 2+ years of experience working on Liferay theme development. For me - it's the same stuff to write code using HTML5 and CSS3. But while come to a front-end part (i.e.: JavaScript, jQuery, etc.), here in Liferay, we have the Alloy UI.

Alloy UI is also called AUI as a small. It is specially developed for Liferay on top of <a title="YUI" href="http://yuilibrary.com/" target="_blank">YUI</a>. AUI has modular pattern as we have in <a title="Require JS" href="http://requirejs.org/" target="_blank">RequireJS</a>.

<em>There was a question in my mind while I started first project on Liferay - "Why should I use AUI instead of jQuery?" and if you are a newbie, the same you must have. Isn't it?</em>

However we can use jQuery or other JavaScript libraries too but as Liferay has AUI built-in, we should use it instead of including external libraries. If you agree on last statement you should refer <a title="Alloy UI Rosette Stone" href="http://alloyui.com/rosetta-stone/" target="_blank">AUI Rosseta</a> site to start learning on it. And Believe me it's not a tough job for jQuery ninjas.
<h2>Prerequisites</h2>
Before starting with theme we should have proper setup ready in our system. I tried to put some pointers which may helpful to understand this article well.
<ol>
	<li>Download and setup local environment with <a title="Liferay Plugin SDK" href="http://sourceforge.net/projects/lportal/files/Liferay%20Portal/6.2.1%20GA2/liferay-plugins-sdk-6.2-ce-ga2-20140319114139101.zip/download?download=http%3A%2F%2Fsourceforge.net%2Fprojects%2Flportal%2Ffiles%2FLiferay%2520Portal%2F6.2.1%2520GA2%2Fliferay-plugins-sdk-6.2-ce-ga2-20140319114139101.zip%2Fdownload" target="_blank">Liferay Plugin SDK</a></li>
	<li>Download and install <a title="Download Liferay Developer Studio" href="https://www.liferay.com/downloads/liferay-projects/liferay-ide" target="_blank">Liferay Developer Studio</a></li>
	<li>Basic knowledge of <a title="HTML Tutorial" href="http://www.w3schools.com/html/" target="_blank">HTML</a> and <a title="CSS Tutorial" href="http://www.w3schools.com/css/" target="_blank">CSS</a></li>
	<li>Understanding of any CMS (i.e.: WordPress, Joomla, Drupal, Magento, etc.)</li>
</ol>
<h2>Theme Architecture</h2>
[caption id="attachment_3085" align="alignleft" width="334"]<img class="wp-image-3085 size-full" src="http://teckstack.com/tsdir/wp-content/uploads/2014/11/test-theme-lr-1.jpg" alt="Liferay Theme Architecture" width="334" height="260" /> IMG:1 (Liferay Theme Architecture)[/caption]

If you want to learn something new, understanding overall structure may ease the flow and increase your confidence. I tried to cover up entire structure of Liferay themes here.

&nbsp;

Let's say, I am creating a new theme named - "test-theme", then inside your themes (Plugin SDK) directory you would have below structure.
<pre class="lang:default mark:5 decode:true" title="Liferay Theme Structure">|-- test-theme
|-- test-theme \ docroot
|-- test-theme \ docroot \ WEB-INF

|-- test-theme \ docroot \ _diffs

|-- test-theme \ docroot \ css
|-- test-theme \ docroot \ images
|-- test-theme \ docroot \ js
|-- test-theme \ docroot \ templates</pre>
Most probably theme developer has to deal with <strong>_diffs</strong> folder. <a href="#">Creating a new theme with Liferay IDE</a> is pretty much easy task. You will be getting <em>blank _diffs folder</em> while creating theme for the first time.
<h2><small>The Purpose of</small> _diffs Folder</h2>
Creating a theme in Liferay needs a deeper knowledge of understanding _diffs folder. Because this is where you will create assets for your theme. For any theme assets are css, javascript, images and templates.

You may have noticed css, images, js and templates directories at the same level of _diffs folder (and not inside of _diffs). Now let's understand what are these folders! These are the assets directories those we have been inherited with parent theme. By default new theme in Liferay inherited with <em>_styled</em> parent theme.

Here I would like to talk about important information on inheriting a parent theme. Actually Liferay provides 3 parent themes as a base you can inherit with (or we can say take a reference to start with).
<ol>
	<li><strong>_styled</strong>: It contains only basic styles for portlets</li>
	<li><strong>_unstyled</strong>: It contains no styles <em>- completely naked theme</em></li>
	<li><strong>Classic</strong>: It contains default look and feel of Liferay <em>- less effort</em></li>
</ol>
Let's say we have started using <strong>_styled </strong>parent theme. So at least we will have basic styling for the portlets. But still my _diffs folder is empty.
<h3>How can I write CSS or change images for my theme in Liferay?</h3>
[caption id="attachment_3112" align="alignright" width="334"]<a href="http://teckstack.com/tsdir/wp-content/uploads/2014/11/test-theme-lr-2.jpg"><img class="wp-image-3112 size-full" src="http://teckstack.com/tsdir/wp-content/uploads/2014/11/test-theme-lr-2.jpg" alt="Liferay _diffs" width="334" height="260" /></a> IMG: 2 (Liferay _diffs)[/caption]

You can create new folders those you want to overwrite inside _diffs folder. Like if you want to change styling for your theme then you will change in css files in CSS folder. So you can create CSS folder inside _diffs folder and start changing in <strong>custom.css</strong> file. Same way you can do with js, images and templates.
<h3>Conclusion</h3>
Here I tried to put my observation on Liferay Themes. It may be different as in approach. I hope you like it and waiting for your reaction in form of comments below. My next article would be on "<a href="#">Creating a New Theme with Liferay IDE</a>".
<h4>Resources</h4>
<ul>
	<li><a title="Liferay.com" href="http://liferay.com" target="_blank">Liferay</a></li>
	<li><a title="Alloy UI" href="http://alloyui.com" target="_blank">Alloy UI</a></li>
	<li><a title="Twitter Bootstrap" href="http://getbootstrap.com" target="_blank">Twitter Bootstrap</a></li>
</ul>
&nbsp;