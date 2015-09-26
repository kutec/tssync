---
ID: 3612
post_title: 'Responsive Web Design: Menu Vs. Sidebar'
author: Kushal Jayswal
post_date: 2015-08-25 11:54:15
post_excerpt: >
  Managing many components correctly for a
  responsive web design may be a
  challenge. Here is the example from past
  project on Menu Vs. Sidebar.
layout: post
permalink: >
  http://teckstack.com/responsive-web-design-menu-vs-sidebar
published: true
wbounce_status:
  - default
dsq_thread_id:
  - "4065733464"
feedweb_post_sort_value:
  - "-1"
ac_is_copyprotect:
  - "1"
ac_is_advanced_tracking:
  - "1"
ac_postid:
  - 3fCH2mhFM0h.text
ac_is_process:
  - "1"
ac_embedid:
  - 2Vwo6zmhhkF
vortex_system_likes:
  - "0"
vortex_system_dislikes:
  - "0"
---
<blockquote>You may have noticed various websites changes its design according to different screen sizes. Such a magic is possible because of the <a href="/responsive-web-design">responsive web design</a> concept. Major websites on the internet today are responsive. One of the most common reasons for <abbr title="Responsive Web Design">RWD</abbr> is to make the same content available for their users without any complex change in a code and no matter from where they are accessing.</blockquote>

Many times the <strong>@media</strong> queries is enough to handle the RWD but in some cases, you may need a script. Today we are going to consider <a href="http://www.wiztools.org/" target="_blank">WizTools.org</a> as an example to understand the <strong>Menu Vs. Sidebar </strong>in responsive design.

[caption id="attachment_4038" align="aligncenter" width="587"]<img class="wp-image-4038 size-full" src="http://teckstack.com/tsdir/wp-content/uploads/2015/05/wiztools_two_columns_desktop.png" alt="wiztools_two_columns_desktop" width="587" height="302" /> Two Column Structure and Sections Identified for Responsive Design[/caption]

As you can see in the above screenshot, WizTools.org has two column layout structure with header and footer sections.

<h2>The Menu</h2>

The navigation or menu is an important section, which allows user to navigate through a site. Therefor it should have implemented the best possible way for tablet and mobiles.

<strong>Desktop View (header)</strong>

[caption id="attachment_3995" align="aligncenter" width="1162"]<img class="wp-image-3995 size-full" src="http://teckstack.com/tsdir/wp-content/uploads/2015/05/wiztools_navigation_after.png" alt="wiztools_navigation_after" width="1162" height="238" /> Desktop - Header and Menus[/caption]

<strong>Toggle</strong> is the most popular way to convert the menu responsively. You can write <a href="http://teckstack.com/js">JavaScript</a> for it. We need a trigger to make hide/show <code>DIV</code> logically. However, WizTools.org has been developed using <a href="http://teckstack.com/bootstrap">Bootstrap framework</a> and the navigation has coded with <a href="http://getbootstrap.com/components/#navbar" target="_blank">navbar</a> component. But it really depends on the project's requirement, whether you should go with a framework or not.

<strong>Related Reading</strong>:

[list icon="icon: external-link"]
<ul>
	<li><a href="http://teckstack.com/change-breakpoints-bootstrap">How to Change Breakpoints with Bootstrap</a></li>
	<li><a href="http://teckstack.com/jquery-collapsible-panel" rel="bookmark">Simple Collapsible Panel with jQuery</a></li>
</ul>
[/list]

<strong>Mobile View (header)</strong>

[caption id="attachment_3998" align="aligncenter" width="436"]<img class="size-full wp-image-3998" src="http://teckstack.com/tsdir/wp-content/uploads/2015/05/wiztools_navigation_responsive_expanded.png" alt="wiztools_navigation_responsive_expanded" width="436" height="450" /> Expanded Menu[/caption]

<h2>The Sidebar</h2>

Now let's focus on the sidebar. If you can notice on the site, the sidebar has collapsible panel (for desktop view) with a set of links. Of course, this is somewhat similar to <strong>the menu</strong> (for smaller screens) but the only thing here different is that it is not a part of the header. It is part of the <em>content area </em><em>(main area between header &amp; footer sections)</em>.

Bootstrap converts everything in stack format, if we have <a href="http://getbootstrap.com/examples/grid/" target="_blank">Bootstrap grid</a> being used. The same we have with Wiztools.org and below is a screenshot what we had before implemented a custom solution for <em>responsive sidebar</em>. The sidebar was landed after the <em>main content area section</em>.

[caption id="attachment_4000" align="aligncenter" width="661"]<img class="size-full wp-image-4000" src="http://teckstack.com/tsdir/wp-content/uploads/2015/05/wiztools_two_columns_responsive.png" alt="wiztools_two_columns_responsive" width="661" height="556" /> Two Column Layout - Responsive Behavior (Earlier)[/caption]

If we think from <a href="http://teckstack.com/ux">UX</a> perspective, <em>links</em> at the bottom of the page, doesn't make sense. As a better solution, it was decided to have a trigger (<span class="lang:default decode:true crayon-inline">span</span>) to show/hide a sidebar for smaller screens from the left of the screen smoothly. It had implemented with <a href="http://srobbin.github.io/jquery-pageslide/" target="_blank">PageSlide</a> jQuery plugin.

<strong>Final Result</strong>

[caption id="attachment_4002" align="aligncenter" width="500"]<img class="size-full wp-image-4002" src="http://teckstack.com/tsdir/wp-content/uploads/2015/05/wiztools_two_columns_responsive_sidebar.png" alt="wiztools_two_columns_responsive_sidebar" width="500" height="507" /> Two Column Layout – Responsive Behavior (Now)[/caption]

<h4>Conclusion</h4>

If you have a short timeline, plugin can help to finish the task quickly. But in future if you need to extend the functionality of the same plugin, you might stick. And using of plugin downgrade your skills too. I would suggest to go with custom JavaScript or jQuery script with your own logic.

If you are a front end developer, you might have different thoughts and idea. Don't hesitate, shoot a comment below.

<em>I am shortly planning for an article - <strong>how to optimize a code for a jQuery plugin</strong>. Kindly subscribe for regular updates or connect socially.</em>

<div class="panel panel-info">
<div class="panel-body">Special thanks to <a href="https://twitter.com/subwiz" target="_blank">Subhash Chandran</a> (founder of WizTools.org) for letting us use his website as an example in this article.</div>
</div>