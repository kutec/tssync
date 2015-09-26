---
ID: 2374
post_title: 'Twitter Bootstrap &#8211; How to reposition modal popup'
author: Kushal Jayswal
post_date: 2014-02-17 10:32:21
post_excerpt: ""
layout: post
permalink: >
  http://teckstack.com/twitter-bootstrap-reposition-modal-popup
published: true
authorsure_include_css:
  - ""
authorsure_hide_author_box:
  - ""
post_to_facebook_timeline:
  - "1"
dsq_thread_id:
  - "2229123127"
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
  - "3141"
post_views_count:
  - "0"
  - "0"
ac_is_copyprotect:
  - "1"
ac_is_advanced_tracking:
  - "1"
ac_postid:
  - 42a8h2DAfqr.text
ac_is_process:
  - "1"
ac_embedid:
  - 2VNYsSnmLHx
vortex_system_likes:
  - "0"
vortex_system_dislikes:
  - "0"
---
Everyone is using <a title="Twitter Boostrap" href="http://getbootstrap.com/" target="_blank">Twitter Bootstrap</a> now. Even enterprise solution providers have started adopting Twitter Bootstrap as their standard framework. Bootstrap provides fantastic way to make HTML elements behave responsively per your thoughts. You can arrange them easily with different class for different screen-size. I love it. It also provides some useful JavaScript components. We can simply copy and paste <a title="Bootstrap CDN Links" href="http://www.bootstrapcdn.com/" target="_blank">CDN links</a> into page and ready to go!
<blockquote><strong>Bootstrap is highly recommended UI framework by front-end-developer world-wide. But sometimes you need to overwrite its default code to complete client's need. Here I am explaining some code for "Twitter Bootstrap - How to reposition modal pop-up with absolute position".</strong></blockquote>
<div id="a"></div>
<h2>Twitter Bootstrap - Default Behavior</h2>
Once you done with the setup with configuration for Twitter Bootstrap Modal Popup, you can see it is coming with <code>position: fixed</code>. As a front-end-developer you should aware about different <a title="Understand CSS Positions - TeckStack.com" href="http://www.teckstack.com/understand-css-positions/" target="_blank">CSS-POSITIONS</a>. It behaves considering the browser window as a stage. We can say BODY / HTML as a parent element.
<h2>Change The Behaviour as Per Specific Requirement</h2>
Now let's say there is a project need to overwrite default behaviour of modal popup to bound with the parent element. Means popup should open inside (or aligned to) parent DIV / element <strong>TEXTBOX</strong>.

See in action: <a class="btn btn-primary" href="http://demo.teckstack.com/twitter-bootstrap/modal-popup/how-to-reposition-modal-popup.html" target="_blank">Demo</a>
<div id="b"></div>
<h2>Overwriting CSS</h2>
<pre class="lang:css decode:true">/* created a TESTBOX class as a PARENT ELEMENT (DIV) */
.testbox {
    background: #000000;
    color: #FFFFFF;
    padding: 10px;
	min-height: 200px;
}
.testbox .modal{ 
    color: #333;
}

/* overwriting default behaviour of Modal Popup in Bootstrap  */
body{ 
    overflow: auto !important;
}
.modal{ 
    overflow: hidden; 
}

/* created new class for targetting purpose - named ".modal2", ".modal1" */
.modal2.in{ 
    position: absolute; 
    bottom: 0; 
    right:0; 
    left: auto; 
    top: auto; 
    bottom: 0; 
    overflow: auto;
}</pre>
<div id="c"></div>
<h2>HTML Changes</h2>
<pre class="lang:default decode:true ">&lt;div class="testbox col-lg-6"&gt; 
  &lt;h3&gt;&lt;strong&gt;Test Box&lt;/strong&gt;&lt;/h3&gt;
    
    &lt;blockquote&gt;
      Modal Popup should &lt;br /&gt;open inside (or aligned to) &lt;br /&gt;this balck DIV area.
    &lt;/blockquote&gt;
    
    &lt;!-- .modal1 --&gt;
    &lt;div class="modal fade bs-modal-sm modal1" tabindex="-1" role="dialog" aria-labelledby="mySmallModalLabel" aria-hidden="true"&gt;
        &lt;div class="modal-dialog modal-sm"&gt;
            &lt;div class="modal-content"&gt; 
                &lt;div class="modal-header"&gt;
                    &lt;button type="button" class="close" data-dismiss="modal" aria-hidden="true"&gt;×&lt;/button&gt;
                    &lt;h4 class="modal-title" id="myModalLabel"&gt;Default Modal Popup&lt;/h4&gt;
                  &lt;/div&gt;
                  
                  &lt;div class="modal-body"&gt;
                    Modal 1 Popup Content
                  &lt;/div&gt;
            &lt;/div&gt;
        &lt;/div&gt;
    &lt;/div&gt;
    
    &lt;!-- .modal2 --&gt;
    &lt;div class="modal bs-modal-sm col-sm-12 col-xs-12 modal2" tabindex="-1" role="dialog" aria-labelledby="mySmallModalLabel" aria-hidden="true"&gt;
        &lt;div class="modal-dialog modal-sm"&gt;
            &lt;div class="modal-content"&gt; 
                &lt;div class="modal-header"&gt;
                    &lt;button type="button" class="close" data-dismiss="modal" aria-hidden="true"&gt;×&lt;/button&gt;
                    &lt;h4 class="modal-title" id="myModalLabel"&gt;Bound to &lt;strong&gt;Test Box&lt;/strong&gt; DIV&lt;/h4&gt;
                  &lt;/div&gt;
                  
                  &lt;div class="modal-body"&gt;
                    Modal 2 Popup Content 
                  &lt;/div&gt;
            &lt;/div&gt;
        &lt;/div&gt;
    &lt;/div&gt;
&lt;/div&gt;</pre>
&nbsp;
<h3>Conclusion</h3>
<ul>
	<li>Such a logic may useful when project have requirement to align pop-up with some element</li>
	<li>HTML and CSS are prerequisites to understand the logic</li>
	<li>Other front-end-developer may have other solution with Script as well. I have tried to give solution through CSS only</li>
	<li>To understand different positions in CSS, you may <a title="Understand CSS Positions - TeckStack.com" href="http://www.teckstack.com/understand-css-positions/" target="_blank">read this article</a></li>
</ul>