---
ID: 4039
post_title: Simple Collapsible Panel with jQuery
author: Kushal Jayswal
post_date: 2015-09-12 13:48:23
post_excerpt: >
  Collapsible panel is one of the most
  used components for a web project. Here
  you can find the easiest jQuery code to
  make it work for the project.
layout: post
permalink: >
  http://teckstack.com/jquery-collapsible-panel
published: true
feedweb_post_sort_value:
  - "0"
feedweb_pac:
  - 18a39021-fa3e-47bc-a121-d549fb85a4d2
ac_is_process:
  - "1"
ac_is_copyprotect:
  - "1"
ac_is_advanced_tracking:
  - "1"
ac_postid:
  - 2ZtQYc8bfMB.text
ac_embedid:
  - 0YZ2RTSdqwp
vortex_system_likes:
  - "1"
vortex_system_dislikes:
  - "0"
vortex_system_user_11:
  - 'a:2:{s:5:"liked";s:7:"noliked";s:8:"disliked";s:8:"disliked";}'
dsq_thread_id:
  - "4145648856"
---
Collapsible panel is one of the most used components for a web&nbsp;project. It easily allows the user showing and&nbsp;hiding the content. Also,&nbsp;it&nbsp;saves the space on a web page. Most of the time it can be found on&nbsp;<abbr title="Frequently Asked Questions">FAQ</abbr>&nbsp;pages, but it can be used anywhere as per&nbsp;the need.

This article will focus on the easiest way to create a collapsible panel using jQuery. And&nbsp;to understand the code, you must have basic knowledge of <a href="/html">HTML</a> and&nbsp;<a href="/js">jQuery</a>.

There are many ways we can integrate the collapsible panel. If you are using the&nbsp;<a href="http://teckstack.com/rwd">Bootstrap</a> then you might choosing its <a href="http://getbootstrap.com/components/#panels" target="_blank">JavaScript component</a>. Also, many jQuery plugins available to download for quick&nbsp;use. But here I have created very simple code that may help you to create a simple jQuery collapsible panel for any project.

<h2>HTML</h2>

I believe in&nbsp;good readable code structure. So I am following below way, where we have a parent <span class="lang:default decode:true crayon-inline ">#secondary</span>&nbsp;to control the hierarchy at its best. Further&nbsp;there is set of <span class="lang:default decode:true crayon-inline ">.widget</span>&nbsp;with panel title and its relevant content.

<pre class="lang:default mark:7,9 decode:true ">&lt;aside id="secondary" class="col-md-3 col-sm-3"&gt;
    &lt;div class="row"&gt;

        &lt;!-- .widget STARTS --&gt;
        &lt;div class="widget"&gt;
            &lt;div class="widget-inner"&gt;
                &lt;h3 class="widget-title"&gt;Panel 1&lt;/h3&gt;

                &lt;div id="code" class="widget-content"&gt;
                    &lt;p&gt;Some content 1&lt;/p&gt;
                &lt;/div&gt;
            &lt;/div&gt;
        &lt;/div&gt;
        &lt;!-- .widget ENDS --&gt;

        &lt;!-- .widget STARTS --&gt;
        &lt;div class="widget"&gt;
            &lt;div class="widget-inner"&gt;
                 &lt;h3 class="widget-title"&gt;Panel 2&lt;/h3&gt;

                &lt;div id="store" class="widget-content"&gt;
                    &lt;p&gt;Some content 2&lt;/p&gt;
                &lt;/div&gt;
            &lt;/div&gt;
        &lt;/div&gt;
        &lt;!-- .widget ENDS --&gt;

        &lt;!-- .widget STARTS --&gt;
        &lt;div class="widget"&gt;
            &lt;div class="widget-inner"&gt;
                 &lt;h3 class="widget-title"&gt;Panel 3&lt;/h3&gt;

                &lt;div id="books" class="widget-content"&gt;
                    &lt;p&gt;Some content 3&lt;/p&gt;
                &lt;/div&gt;
            &lt;/div&gt;
        &lt;/div&gt;
        &lt;!-- .widget ENDS --&gt;

    &lt;/div&gt;
&lt;/aside&gt;</pre>

<h2>jQuery</h2>

I have highlighted part in HTML code above, those we are going to manipulate with below jQuery code.&nbsp;Before jumping into below code, I would suggest to read&nbsp;<a href="http://ashishuideveloper.in/2015/04/understand-jquery-events-bind-live-delegate/" target="_blank">this article</a>&nbsp;to understand why we have used <span class="lang:default decode:true crayon-inline">.on()</span>&nbsp; function instead of <span class="lang:default decode:true crayon-inline ">.click()</span>&nbsp;.

<pre class="lang:default decode:true">(function ($) {
    $("#secondary").on('click', '.widget-title', function (e) {
        $(this).next('.widget-content').toggle(200);
        $(this).parents('.widget').toggleClass('active');
    });
})(jQuery);</pre>

<h2>CSS</h2>

Through CSS we are hiding&nbsp;the&nbsp;<span class="lang:default decode:true crayon-inline">.widget-content</span>&nbsp;class, which will be shown upon clicking on <span class="lang:default decode:true crayon-inline ">.widget-title</span>&nbsp;.

<pre class="lang:default decode:true">#secondary .widget-title {
    margin: 0;
    font-size: 22px;
    background: #eee;
    padding: 10px;
    cursor: pointer;
}
#secondary .widget .widget-content {
    display: none;
}
#secondary .widget.active .widget-title, #secondary .widget.active ul {
    background: #666;
    color: #fff;
}</pre>

<h2>Demo</h2>

<iframe width="100%" height="300" src="//jsfiddle.net/kutec/6x3qb1zc/embedded/result/" allowfullscreen="allowfullscreen" frameborder="0"></iframe>

This article is intent to be helpful to freshers in to front end development or UI development.&nbsp;Kindly share your thoughts area in comment below.