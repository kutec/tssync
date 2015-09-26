---
ID: 2395
post_title: Manipulate HREF using jQuery
author: Kushal Jayswal
post_date: 2014-02-20 11:40:36
post_excerpt: ""
layout: post
permalink: >
  http://teckstack.com/manipulate-href-using-jquery
published: true
authorsure_include_css:
  - ""
authorsure_hide_author_box:
  - ""
post_to_facebook_timeline:
  - "1"
dsq_thread_id:
  - "2293268450"
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
  - "1777"
ac_is_copyprotect:
  - "1"
ac_is_advanced_tracking:
  - "1"
ac_postid:
  - 71DNa0jnzT7.text
ac_is_process:
  - "1"
ac_embedid:
  - 2bCa4fLiukC
vortex_system_likes:
  - "0"
vortex_system_dislikes:
  - "0"
---
<blockquote>People get connected with the world by social connections like <a title="Facebook" href="http://facebook.com" target="_blank">Facebook</a>, <a title="Twitter" href="http://twitter.com" target="_blank">Twitter</a>, <a title="LinkedIn" href="http://linkedin.com" target="_blank">LinkedIn</a>, etc. Many Content Management System has started adding <strong>social fields</strong> in their <em>personal details form</em>. Today I am presenting one of the way to manipulate HREF using jQuery.</blockquote>
Well let us take an example having an <strong>HTML form</strong> asking to enter a <strong><em><a title="Facebook" href="http://facebook.com" target="_blank">Facebook</a> Username</em></strong>. I have created a <code>function create_social_link()</code> to manipulate HREF.

<a class="btn btn-primary" title="Demo" href="http://kutec.github.io/manipulate-href-using-jquery" target="_blank">Demo</a> or <a class="btn btn-default" title="Fork on Github" href="https://github.com/kutec/Manipulate-HREF-using-jQuery" target="_blank">Fork on Github</a>
<h2>HTML</h2>
<pre class="lang:default decode:true ">&lt;form name="social_links"action=""class=""&gt;
    &lt;div class="form-group"&gt;
        &lt;label&gt;Enter Facebook Username: 
            &lt;input class="input-sm"type="text"name="url_param"id="append_to_url_id"/&gt;
        &lt;/label&gt;
        &lt;label&gt;
            &lt;input class="btn btn-primary"type="button"value="Submit"onclick="create_social_link();"/&gt;
        &lt;/label&gt;
        &lt;input class="btn"id="reset"type="reset"value="Reset URL"/&gt;
    &lt;/div&gt;

    Result: &lt;a href=""id="linkValue"target="_blank"&gt;&lt;/a&gt;

&lt;/form&gt;</pre>
&nbsp;
<h2>Script</h2>
<pre class="lang:default decode:true">//url Prefix
var url_prefix = 'http://fb.com';

//set HREF value to A tag
var defaultLink = $('#linkValue').attr('href', url_prefix);

// place URL to RESULT
var putLink = $('#linkValue').append(url_prefix);
 
function create_social_link() {

    // ID to get input from user
    var append_to_url = $('#append_to_url_id').val();
 
    // if no inputs by user then no action
    if ( ! append_to_url ) {
        return false;
    }
 
    // appending user inputs to url_prefix
    var linkValue = putLink.append('/' + append_to_url);
    defaultLink = $('#linkValue').attr('href', url_prefix+'/'+append_to_url);
 
    //reset URL to default
    $('#reset').click(function(e) {
        defaultLink = $('#linkValue').attr('href', url_prefix);
        putLink = putLink.html(url_prefix);
    });
}</pre>