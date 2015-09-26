---
ID: 3306
post_title: How to Configure SASS for HTML Projects
author: Kushal Jayswal
post_date: 2015-03-01 06:53:44
post_excerpt: ""
layout: post
permalink: >
  http://teckstack.com/how-to-configure-sass-for-html-projects
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
  - "4817"
mentions:
  - 'a:0:{}'
dsq_thread_id:
  - "3558111384"
mentioned_by:
  - "3522"
post_views_count:
  - "10"
ac_is_copyprotect:
  - "1"
ac_is_advanced_tracking:
  - "1"
ac_postid:
  - 7VXtcJygDBO.text
ac_is_process:
  - "1"
ac_embedid:
  - 6KtU9XeJ9uz
vortex_system_likes:
  - "0"
vortex_system_dislikes:
  - "0"
---
<blockquote><a title="SASS" href="http://sass-lang.com/" target="_blank">SASS</a> is booming the world with giving super powers to CSS and if you don't know about it, you must gain your knowledge as a front end developer. The configuration for SASS is so simple but I observed that people avoids it or leave it to core developers. As I opine, when we can do more in less time, we should definitely go for it!</blockquote>

Previously I have written on "<a href="http://teckstack.com/creating-color-palette-sass" rel="bookmark">Creating Color Palette with SASS</a>" and it may changes the way you think about branding. This article will cover - "<a class="mentionable" href="http://teckstack.com/?p=3306">How to Configure SASS for HTML Projects</a>".

Well! There are two scenarios while you pick SASS as a CSS pre-processor.

<ol>
    <li>PSD to HTML/CSS markup development</li>
    <li>HTML/CSS to CMS (i.e.: WordPress,...) Theme Integration</li>
</ol>

<h2>Matter of Opinions</h2>

This is general approach that UI developers used to write CSS while working on PSD to HTML/CSS and rework on SASS at the time of CMS theme integration. Because CMS has number of easy ways to deal with SASS without wasting much time on configuration.

Likewise if your project needs <a title="WordPress" href="http://wordpress.org" target="_blank">WordPress</a> then you might choose <a title="WP-SCSS - SASS Plugin For WordPress" href="https://wordpress.org/plugins/wp-scss/" target="_blank">WP-SCSS</a> plugin where you have to pass directory path for CSS and SASS/SCSS folders and you are good to go! Easy right?

On the other hand if we talk about <a title="Liferay" href="http://liferay.com" target="_blank">Liferay</a>, then it has built-in support for SASS. You just have to <span class="lang:default decode:true  crayon-inline">@import "compass"</span> in your CSS file and you are done. No extra configuration needed.

So comparatively,  configuring SASS with CMS is easy rather than efforts in HTML &amp; CSS projects. Although you should learn to configure SASS for HTML projects. Below I tried to cover up all steps required.

<h2>SASS Configuration</h2>

<ol>
    <li>
<h3>Overall Project Architecture</h3>
You can keep <strong>.css</strong> and <strong>.scss</strong> files in one folder but considering best practices approach, we should have separate folders for each.
<pre class="lang:default mark:2,3,6,7 decode:true">Project Directory
|_ css
   |_ main.css 
|_ img
|_ js
|_ sass
   |_ main.scss
|_ index.html</pre>
</li>
    <li>
<h3>RUBY Installer</h3>
Very first thing is, you need to download and install Ruby 1.9.3 from below URL. And please read "WHICH VERSION TO DOWNLOAD?", so you will be cleared on selecting 1.9.3 version and not the latest one.
<pre class="lang:default decode:true">http://rubyinstaller.org/downloads/</pre>
</li>
    <li>
<h3>Open Command Prompt</h3>
There are two ways you can follow this step.
<ol>
    <li>Open command prompt (Ctrl+r and type cmd) and and go to project directory by changing directory path with CD command OR</li>
    <li>You can directly go to Project Directory in explorer and type "cmd" and hit enter. This will open command prompt for current directory

[caption id="attachment_3409" align="alignnone" width="763"]<img class="wp-image-3409 size-full" src="http://teckstack.com/tsdir/wp-content/uploads/2015/01/SASS-cmd.png" alt="SASS Command Propmpt" width="763" height="251" /> SASS Command Prompt[/caption]</li>
</ol>
</li>
    <li>
<h3>Installing SASS</h3>
In command prompt run command: <span class="lang:default decode:true  crayon-inline">gem install sass</span> . This will enable SASS for current project directory.

[caption id="attachment_3415" align="alignnone" width="439"]<img class="size-full wp-image-3415" src="http://teckstack.com/tsdir/wp-content/uploads/2015/01/SASS-install.png" alt="SASS Install" width="439" height="136" /> SASS Install[/caption]</li>
    <li>
<h3>Watching Input and Output Directories</h3>
There is simple command, watches input and output files or directories for changes: <span class="lang:default decode:true  crayon-inline">sass --watch sass:css</span> . For our project we have followed separate folders for SCSS and CSS files. That's it! Now whenever you changes anything in <strong>.scss</strong> file under <span style="text-decoration: underline">sass</span> folder, <em>watch</em> command will compile and update <strong>.css</strong> files accordingly under <span style="text-decoration: underline">css</span> folder.

[caption id="attachment_3419" align="alignnone" width="453"]<img class="size-full wp-image-3419" src="http://teckstack.com/tsdir/wp-content/uploads/2015/01/SASS-watch.png" alt="SASS Watch" width="453" height="100" /> SASS Watch[/caption]</li>
</ol>

<strong>Now we are completely done with SASS configuration for HTML project. But wait there are little more...</strong>

<hr />

I am assuming that you have included <span class="lang:default decode:true  crayon-inline">main.css</span> file to <span class="lang:default decode:true  crayon-inline ">index.html</span>  page. So skipping that basic stuffs and directly come to important point.

[caption id="attachment_3421" align="alignleft" width="225"]<img class="wp-image-3421 size-full" src="http://teckstack.com/tsdir/wp-content/uploads/2015/01/SASS-Inspector.png" alt="SASS Inspector" width="225" height="143" /> SASS Inspector[/caption]

I am opening <span class="lang:default decode:true  crayon-inline">index.html</span> page in Chrome browser and opened developer tool. In developer tool following "Sources" tab to view current project's architecture. Now as you can notice in screenshot that we have two folders <strong>css</strong> and <strong>scss</strong>, visible publicly. And actually we don't need that scss folder be visible to users for security concerns.

<blockquote>So to hide SASS folder from the architecture, now we need <a title="Compass - CSS Authoring Framework" href="http://compass-style.org/" target="_blank">compass</a> be configured for our HTML project. And though we are done with SASS configuration, next we'll move to configure compass in our project.</blockquote>

I am personally big fan of the Compass as it also helps with compression which enhance overall performance of the site. Below are few points on the same...

<h2>Compass Configuration</h2>

<ol>
    <li>
<h3>Update Ruby</h3>
Run command in command prompt: <span class="lang:default decode:true  crayon-inline">gem update --system</span></li>
    <li>
<h3>Install Compass</h3>
Run command for current project directory: <span class="lang:default decode:true  crayon-inline ">gem install compass</span></li>
    <li>
<h3>Enable Compression</h3>
Run command for current project: <span class="lang:default decode:true  crayon-inline ">compass compile -e production --force</span></li>
    <li>
<h3>Watching Files for a Change</h3>
[caption id="attachment_3441" align="alignleft" width="225"]<img class="size-full wp-image-3441" src="http://teckstack.com/tsdir/wp-content/uploads/2015/01/SASS-Inspector-Compass.png" alt="SASS Inspector Compass" width="225" height="147" /> SASS Inspector Compass[/caption]

Now we have to tell Compass to start watching our projects' <strong>css</strong> and <strong>sass</strong> directories for a change: <span class="lang:default decode:true  crayon-inline">compass watch</span>

<strong>Just to update that, by default <span style="text-decoration: underline">Compass will generate new folders named stlesheets and sass</span> while you create a new project using <span class="lang:default decode:true  crayon-inline">compass create &lt;myproject&gt;</span>  or start watching current directory using <span class="lang:default decode:true  crayon-inline">compass watch</span> command. So, here for our project the css folder will be replaced with stylesheets folder.</strong></li>
</ol>

<h3>Conclusion</h3>

So, I would recommend to front end developers to start using Compass and SASS for HTML projects instead of doing it so at the time of theme integration with any CMS. This way you do not need to write same code again for SASS and save time and efforts for the next project.

<h4>Resources</h4>

<ol>
    <li><a title="SASS" href="http://sass-lang.com/" target="_blank">SASS</a></li>
    <li><a title="WordPress CMS" href="http://wordpress.org/" target="_blank">WordPress</a></li>
    <li><a title="Liferay" href="http://liferay.com/" target="_blank">Liferay</a></li>
    <li><a title="Compass" href="http://compass-style.org/" target="_blank">Compass</a></li>
</ol>