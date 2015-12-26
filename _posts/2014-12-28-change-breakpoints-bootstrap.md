---
ID: 3143
post_title: How to Change Breakpoints with Bootstrap
author: Kushal Jayswal
post_date: 2014-12-28 12:40:38
post_excerpt: "Using Bootstrap in a web project is normal. And now if you know Bootstrap, that isn't enough. You need to keep upgrading yourself with new tricks to master it. Sometime client needs customization and he doesn't understand the framework anyway. In such a situation we have to think out of the box to sort it out. To handle such a situation Bootstrap breakpoints needs extra efforts to make it works as per requirement. This article will focus on the same."
layout: post
permalink: >
  http://teckstack.com/change-breakpoints-bootstrap
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
  - "5306"
dsq_thread_id:
  - "3366975385"
mentions:
  - 'a:0:{}'
post_views_count:
  - "3"
ac_is_copyprotect:
  - "1"
ac_is_advanced_tracking:
  - "1"
ac_postid:
  - 2gEP3w37-LL.text
ac_is_process:
  - "1"
ac_embedid:
  - 3yPppXZw0ET
vortex_system_likes:
  - "0"
vortex_system_dislikes:
  - "0"
---
<blockquote>Using Bootstrap in a web project is normal. And now if you know Bootstrap, that isn't enough. You need to keep upgrading yourself with new tricks to master it. Sometime client needs customization and he doesn't understand the framework anyway. In such a situation we have to think out of the box to sort it out.</blockquote>
Before I have written on <a href="http://teckstack.com/twitter-bootstrap-reposition-modal-popup" data-cke-saved-href="http://teckstack.com/twitter-bootstrap-reposition-modal-popup">re-positioning of modal popup</a>. And today we will discuss on possible ways to <a href="http://teckstack.com/change-breakpoints-bootstrap" data-cke-saved-href="http://teckstack.com/change-breakpoints-bootstrap">change breakpoints with Bootstrap</a>.
<h2>What is Breakpoint</h2>
Though the Bootstrap is complete framework and packaged with JavaScript components too but <strong>achieving effortless responsive behavior is the major key point we can granted Bootstrap for</strong>. Responsive behavior depends on resolutions (viewport or screen sizes).

By default Bootstrap supports four resolutions - called Breakpoints in technical term.
<table class="table table-bordered table-striped">
<thead>
<tr>
<th style="text-align: left;">&lt; 768px</th>
<td style="text-align: left;">Extra small devices <em>Phones</em></td>
</tr>
<tr>
<th style="text-align: left;">≥ 768px</th>
<td style="text-align: left;">Small devices <em>Tablets</em></td>
</tr>
<tr>
<th style="text-align: left;">≥ 992px</th>
<td style="text-align: left;">Medium devices <em>Desktops</em></td>
</tr>
<tr>
<th style="text-align: left;">≥ 1200px</th>
<td style="text-align: left;">Large devices <em>Desktops</em></td>
</tr>
</thead>
</table>
I would like to share my experience here. I had integrated Navbar component for primary navigation in a project. Might you aware that Navbar starts collapsing with &lt; 768px but unfortunately that project had 6-7 navigation items to show, so while re-sizing those items started moving to the next line until getting 768px width (image 1). Now this looks little weird and I had to change the Navbar's breakpoint to 992px instead of 768px (image 2).
<h5>There are 3 ways we can change media queries breakpoints with Bootstrap.</h5>
<ol>
	<li><a href="#Customize_Bootstrap_before_downloading">Customize Bootstrap before downloading</a></li>
	<li><a href="#Change_in_CSS">Change in CSS</a></li>
	<li><a href="#Create a_new_Breakpoint">Create a new Breakpoint</a></li>
</ol>
<h2><a title="Customize Bootstrap" href="http://getbootstrap.com/customize/" target="_blank">Customize Bootstrap</a> before downloading</h2>
Bootstrap let us change some of the preferences before downloading a ZIP. If you got the project requirement then you should select this option. Because here, you would have freedom to change breakpoints before start working on a project. So you can plan well in advance.

[caption id="attachment_3157" align="alignnone" width="768"]<img class="wp-image-3157 size-medium" src="http://teckstack.com/tsdir/wp-content/uploads/2014/12/Bootstrap-Media-Queries-Breakpoints-768x472.png" alt="Bootstrap-(Media-Queries-Breakpoints)" width="768" height="472" /> Bootstrap-(Media-Queries-Breakpoints)[/caption]

&nbsp;
<h2>Change in CSS</h2>
If you need to change behavior of specific component (i.e.: navbar), you can overwrite or change with CSS. You can click on bellow "see in action" links for a demo.
<h4>Image 1 <small><a title="Demo with Default CSS for Navbar" href="http://jsfiddle.net/1skvyz1o/1/" target="_blank">see in action</a></small></h4>
[caption id="attachment_3158" align="alignnone" width="767"]<img class="wp-image-3158 size-full" src="http://teckstack.com/tsdir/wp-content/uploads/2014/12/Bootstrap-Media-Queries-Breakpoints-broken-menu.png" alt="Bootstrap-(Media-Queries-Breakpoints)-menu-768" width="767" height="166" /> Bootstrap-(Media-Queries-Breakpoints)-menu-768[/caption]
<h5></h5>
<h4>Image 2 <small><a title="Demo after changing CSS for Navbar" href="http://jsfiddle.net/1skvyz1o/2/" target="_blank">see in action</a></small></h4>
[caption id="attachment_3159" align="alignnone" width="768"]<img class="wp-image-3159 size-medium" src="http://teckstack.com/tsdir/wp-content/uploads/2014/12/Bootstrap-Media-Queries-Breakpoints-menu-992-768x81.png" alt="Bootstrap-(Media-Queries-Breakpoints)-menu-992" width="768" height="81" /> Bootstrap-(Media-Queries-Breakpoints)-menu-992[/caption]
<h4></h4>
<h4>Sample Code <small><a title="https://coderwall.com" href="https://coderwall.com/p/wpjw4w/change-the-bootstrap-navbar-breakpoint" target="_blank">Coderwall</a></small></h4>
<pre class="lang:default decode:true">@media (max-width: 992px) {
    .navbar-header {
        float: none;
    }
    .navbar-toggle {
        display: block;
    }
    .navbar-collapse {
        border-top: 1px solid transparent;
        box-shadow: inset 0 1px 0 rgba(255, 255, 255, 0.1);
    }
    .navbar-collapse.collapse {
        display: none!important;
    }
    .navbar-nav {
        float: none!important;
        margin: 7.5px -15px;
    }
    .navbar-nav&gt;li {
        float: none;
    }
    .navbar-nav&gt;li&gt;a {
        padding-top: 10px;
        padding-bottom: 10px;
    }
}</pre>
<h2>Create a new Breakpoint</h2>
If above two are not the solution in your case, you need to create a new breakpoint. Below are some steps.
<ol>
	<li><a href="https://github.com/Gizra/custom-breakpoint-example/blob/master/app/_scss/main.scss#L1-L14" target="_blank">Set the custom breakpoints</a> as per your need</li>
	<li><a href="https://github.com/Gizra/custom-breakpoint-example/blob/master/app/_scss/main.scss#L16-L19" target="_blank">Create new <span class="lang:default decode:true  crayon-inline ">_grids.scss</span>  file</a> and include it to your <span class="lang:default decode:true  crayon-inline">styles.scss</span>  file</li>
	<li><a href="https://github.com/Gizra/custom-breakpoint-example/blob/master/app/_scss/_grids.scss#L1-L3" target="_blank">Declaring</a> new breakpoints</li>
	<li>Deciding on container width and <a href="https://github.com/Gizra/custom-breakpoint-example/blob/master/app/_scss/_grids.scss#L4-L11" target="_blank">setting up</a></li>
	<li>Calling up the <span class="lang:default decode:true  crayon-inline ">make-grid()</span>  <a href="https://github.com/Gizra/custom-grid/blob/master/app/_scss/_grids.scss#L13-L17" target="_blank">SASS function</a></li>
	<li>Last step is optional but recommended to <a href="https://github.com/Gizra/custom-breakpoint-example/blob/master/app/_scss/_grids.scss#L19-L36" target="_blank">add visible and hidden classes</a></li>
</ol>
<h3>Conclusion</h3>
It completely depends on your need. If you can fix with CSS you should avoid jumping into complex side. The best option is to use <a title="Customize Bootstrap" href="http://getbootstrap.com/customize/" target="_blank">Bootstrap's custom tool</a>.
<h3>Resources</h3>
<ul>
	<li><a title="Twitter Bootstrap Official Site" href="http://getbootstrap.com" target="_blank">Twitter Bootstrap</a></li>
	<li><a title="https://coderwall.com" href="https://coderwall.com/p/wpjw4w/change-the-bootstrap-navbar-breakpoint" target="_blank">Coderwall</a></li>
	<li><a href="http://www.gizra.com/content/custom-breakpoint-bootstrap-sass/" target="_blank">Gizra</a></li>
</ul>