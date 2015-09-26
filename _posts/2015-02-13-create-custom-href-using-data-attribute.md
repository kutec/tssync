---
ID: 3317
post_title: Create Custom HREF Using DATA Attribute
author: Kushal Jayswal
post_date: 2015-02-13 13:03:28
post_excerpt: ""
layout: post
permalink: >
  http://teckstack.com/create-custom-href-using-data-attribute
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
  - "5078"
dsq_thread_id:
  - "3512410743"
mentions:
  - 'a:0:{}'
post_views_count:
  - "10"
ac_is_copyprotect:
  - "1"
ac_is_advanced_tracking:
  - "1"
ac_postid:
  - 3QuOzDayM1K.text
ac_is_process:
  - "1"
ac_embedid:
  - 7TjPB8XEvUp
vortex_system_likes:
  - "0"
vortex_system_dislikes:
  - "0"
---
<blockquote>HTML5 allows us to create custom attribute with use of <strong>DATA attribute</strong>. It<strong> </strong>is one of the coolest addition in HTML5 which will behave privately for a page or an application.</blockquote>

<a title="Create Custom HREF Using DATA Attribute" href="http://teckstack.com/create-custom-href-using-data-attribute">This article</a> will focus on how to "Create Custom HREF Using DATA Attribute" and that is without violating W3C rules. Let's understand little more in-depth.

<h2>Linkable DIV <small>has been a thought from decade</small></h2>

I am pretty much sure that you have faced situation where you need to make entire DIV tag linkable. And you may have done that using below kind of code structure.

<pre class="lang:default mark:2,6 decode:true" title="W3C Invalid Code">&lt;div class="boxes"&gt;
    &lt;a href="http://link1.com" target="_blank"&gt;
        &lt;div class="box"&gt;
            &lt;h3&gt;Link with _blank attr&lt;/h3&gt;
        &lt;/div&gt;
    &lt;/a&gt;
&lt;/div&gt;</pre>

Well, as per <a title="The World Wide Web Consortium (W3C)" href="http://www.w3.org/" target="_blank">W3C</a> rules, we cannot put <a title="Block-level elements" href="https://developer.mozilla.org/en-US/docs/Web/HTML/Block-level_elements" target="_blank">block level elements</a> inside <a title="Inline elements" href="https://developer.mozilla.org/en-US/docs/Web/HTML/Inline_elemente" target="_blank">inline elements</a> hence above code is invalid. And as a front end developer, we should take ownership to provide proper solution.

From the code I must say - project needs a block that would be <span style="text-decoration: underline">linkable all the way</span>. <em>And it is not possible without </em>"<em>a</em>"<em> tag as a parent</em>. If it is!, please show your reaction in <a title="Add a Comment" href="#disqus_thread">comment section</a> and help the community.

As an alternative solution, we can replace <span class="lang:default decode:true  crayon-inline">&lt;h3&gt;</span> &amp; <span class="lang:default decode:true  crayon-inline">&lt;div&gt;</span> with <span class="lang:default decode:true  crayon-inline">&lt;span&gt;</span> tags and get same look &amp; feel, using CSS. But replacing everything inside "a" tag with "span" is not a good suggestion and further <span class="lang:default decode:true  crayon-inline">&lt;h3&gt;</span> does magic in terms of SEO too, so we will not remove it anyway and keeping it so, again code will be invalid.

As I opine, <em>there is no other option than to think beyond the boundaries to achieve a valid structure</em>. So let the real work starts now...

<h2>Correct Code Structure <small>to match up W3C validation</small></h2>

<pre class="lang:default mark:4 decode:true" title="W3C Valid Structure">&lt;div class="boxes"&gt;
    &lt;div class="box"&gt;
        &lt;h3&gt;
            &lt;a href="http://link1.com" target="_blank"&gt;Link with _blank attr&lt;/a&gt;
        &lt;/h3&gt;
    &lt;/div&gt;
&lt;/div&gt;</pre>

Let me remind you the requirement - <em>we have to create a DIV - linkable all the way</em>.

<h2>Mindset</h2>

By observing above <a title="Section - Correct Code Structure" href="#Correct_Code_Structure_to_match_up_W3C_validation">correct code structure</a>, we have two attributes in "a" tag - <strong>href</strong> and <strong>target</strong>. So while thinking on <span class="lang:default decode:true  crayon-inline ">data-</span>  attributes, we need two custom attributes too. But still, it is completely up to you that whether you want to provide <em>custom target attribute</em> or not!

Below are two custom data-attributes that we will add to <span class="lang:default decode:true  crayon-inline">&lt;div class="box"&gt;</span> and those will behave exactly same way as "a" tag (including "target").

<ol>
    <li><strong>data-href </strong>= href</li>
    <li><strong>data-target</strong> = target</li>
</ol>

&nbsp;

After adding <span class="lang:default decode:true  crayon-inline ">data-</span>  attributes, our code will be like as below. And as you can see it is not violating W3C standard - <a title="W3C Validator - Direct Input" href="http://validator.w3.org/#validate_by_input" target="_blank">check here</a>.

<pre class="lang:default mark:1,4 decode:true">&lt;div class="boxes" data-href="http://link1.com" data-target="_blank"&gt;
    &lt;div class="box"&gt;
        &lt;h3&gt;
            &lt;a href="http://link1.com" target="_blank"&gt;Link with _blank attr&lt;/a&gt;
        &lt;/h3&gt;
    &lt;/div&gt;
&lt;/div&gt;</pre>

<h2>jQuery <small>Code</small></h2>

First I tried with below code to create <span class="lang:default decode:true  crayon-inline ">data-href</span> specific to <span class="lang:default decode:true  crayon-inline">.boxes</span> class.

<pre class="lang:default decode:true" title="Simple jQuery">$(function() {  
    $('.boxes a').each(function(){
        var aTag = $(this).attr('href');
        
        $(this).parent().attr('data-href',aTag);        
        
        $("[data-href]").click(function() {
            window.location.href = $(this).attr("data-href");
            return false;
        });
    })  
}(jQuery));</pre>

But later I decided to extend this to next level where <em>user can decide a <span style="text-decoration: underline">class</span>, <span style="text-decoration: underline">id </span></em>or <span style="text-decoration: underline"><em>element</em></span> for logical manipulation.

<h2>Extended jQuery <small>plugin code</small></h2>

<pre class="lang:default decode:true">(function ( $ ) { 
    $.fn.dataURL = function() {
        
        // variables
        var el = $(this);
        var aTag = el.find('a');
        var aHref;
        var aTarget;
        
        // get &amp; set attributes
        aTag.each(function() {
            var aHref = $(this).attr('href');
            $(this).parent().attr('data-href',this);
            
            aTarget = $(this).attr('target');
            $(this).parent().attr('data-target',aTarget);
        });
        
        // imitation - default attributes' behavior on "data-" attributes
        $(el).delegate('[data-href]','click', function() {
            var loc = window.location.href;
            loc = $(this).attr("data-href");
            aTarget = $(this).attr('data-target');

            if(aTarget == "_blank"){
                window.open(loc);
            } else {
                window.location = loc;
            }
            
            return false;
        });     
        
        //removing attributes from selector itself
        el.removeAttr('data-href');
        el.removeAttr('data-target');
        
        // css
        $('[data-href]').css('cursor','pointer');
    };
}( jQuery ));</pre>

<h2>Final Call</h2>

<pre class="lang:default decode:true">&lt;script&gt;
    $('.boxes').dataURL();
&lt;/script&gt;</pre>

You can simply replace <span class="lang:default decode:true  crayon-inline ">.boxes</span>  with other <em><span style="text-decoration: underline">class</span></em>, <em><span style="text-decoration: underline">id</span></em> or <em><span style="text-decoration: underline">element</span></em>. But for now, the logic has to follow <a title="Section - Correct Code Structure" href="#Correct_Code_Structure_to_match_up_W3C_validation">given structure</a>. I am also planning to extend this plugin for <span class="lang:default decode:true  crayon-inline ">body</span>  tag to give more flexibility to user.

<h2>Demo</h2>

You can see a working <a title="Clickable DIV with W3C Validation" href="http://jsfiddle.net/kutec/m9vxhcke/6/" target="_blank">demo here</a> which I will be moving to <a href="#" target="_blank">Github</a> soon (as I have deeper thought to extend it).

<h3>Inspiration</h3>

This article is inspired by <a title="David Walsh - JavaScript, HTML5 Consultant" href="http://davidwalsh.name/" target="_blank">davidwalsh.name</a> &amp; <a title="HTML5 Linking Demo" href="http://meyerweb.com/eric/html-xhtml/html5-linking-demo.html" target="_blank">Eric Meyer</a>. And special thanks to <a title="UNDERSTAND JQUERY EVENTS – BIND, LIVE &amp; DELEGATE" href="http://ashishuideveloper.in/2014/12/difference-between-bind-live-delegate-functions-in-jquery" target="_blank">Ashish Panchal</a> for guideline on <span class="lang:default decode:true  crayon-inline">deligate()</span>  event.

<h3>Resources</h3>

<ul>
    <li><a title="HTML5 - Custom Data Attributes" href="http://www.w3.org/html/wg/drafts/html/master/dom.html#custom-data-attribute" target="_blank">HTML5 - Custom Data Attributes</a></li>
</ul>

<a title="Macrofolio" href="http://www.marcofolio.net/" target="_blank"><small>Image Credit</small></a>