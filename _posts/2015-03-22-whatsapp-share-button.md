---
ID: 3474
post_title: 'WhatsApp Share &#8211; New Way to Social Engagement'
author: Kushal Jayswal
post_date: 2015-03-22 08:59:52
post_excerpt: ""
layout: post
permalink: >
  http://teckstack.com/whatsapp-share-button
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
mentions:
  - 'a:0:{}'
views:
  - "4188"
dsq_thread_id:
  - "3616466209"
wbounce_status:
  - default
post_views_count:
  - "10"
ac_is_copyprotect:
  - "1"
ac_is_advanced_tracking:
  - "1"
ac_postid:
  - 1K-yDEqkY8A.text
ac_is_process:
  - "1"
ac_embedid:
  - 0vkRGzrdZj9
vortex_system_likes:
  - "0"
vortex_system_dislikes:
  - "0"
---
<blockquote>Frankly speaking, I am <span style="text-decoration: line-through;">not</span> a big fan of WhatsApp. But while I came to know that it <a title="WhatsApp Hits 700 Million Users" href="http://readwrite.com/2015/01/06/whatsapp-700-million" target="_blank">crosses 700 million users</a> and the <a title="List of virtual communities with more than 100 million active users" href="http://en.wikipedia.org/wiki/List_of_virtual_communities_with_more_than_100_million_active_users" target="_blank">most popular application</a>, I changed my mind and in curiosity, I started googling on it. It's all wonderful but as a developer, we should think on the other side too and today we will discuss on it.</blockquote>
See <a class="btn btn-success" title="Demo - WhatsApp Share Button" href="http://demo.teckstack.com/WhatsApp-Share-Button" target="_blank">Demo</a> or <a class="btn btn-info" title="Fork - WhatsApp Share Button" href="http://kutec.github.io/WhatsApp-Share-Button" target="_blank">Fork</a> on Github.
<h2>A Small Story</h2>
Social sharing is a key to success for any blog and I noticed, almost all blogs with social sharing buttons. Facebook &amp; Twitter are the most preferred options, comparing to others like Google+, Pinterest, LinkedIn, etc. But yet I couldn't see even a single blog having <span style="text-decoration: underline;">WhatsApp sharing</span> button.

Further mobile and tablet users are increasing day-by-day and lets keep in mind, the demand for responsive web design <em>(more than native apps)</em>, adding one more button - WhatsApp Share - to your collection of social sharing widget wouldn't be that difficult! Agree? Moreover <a title="On Buzzfeed, people are already clicking the share-to-WhatsApp button more than Twitter’s" href="http://qz.com/179261/people-are-already-sharing-more-buzzfeed-stories-to-whatsapp-than-to-twitter" target="_blank">this article</a> pushed me even more to this direction.
<h2>The Mindset</h2>
From above story, requirement seems pretty simple to add a social share button which <strong>shares your article's link directly to WhatsApp application</strong>. If you write, read or develop blogs then getting this need is not new. This will be similar to what you do while integrate Facebook or Twitter share button for a blog.

Another need is to show this button only for portable devices <em>(i.e.: iPhone, Android, Tablet, etc.)</em>. We need to manipulate through jQuery. And I have written plugin code with some configurable options.

Here is a <a title="WhatsApp Sharing Button Generator" href="http://whatsapp-sharing.com/" target="_blank">site</a> provides code snippet to integrate WhatsApp sharing button which will be visible in devices. They have been written pure JavaScript code and as jQuery has larger community, I will follow jQuery. Lets start coding...
<h3>Initial Code</h3>
<pre class="lang:default decode:true crayon-selected" title="Initial Code">(function ($) { 
	$('.wa_btn').on("click", function(e) {
		if(devices) ) {
			//do something
		}else{
			alert("This button will work only in mobile device.");
		}
	});
}( jQuery ));</pre>
As you can see in above code, we have two blocks - IF and ELSE. We are trying to integrate WhatsApp share button for portable devices only. And in the ELSE block we try to throw alert to user possibly. All will be happened on click of element having class - <span class="lang:default decode:true crayon-inline">.wa_btn</span>. But as discussed, I have taken approach for a plugin. So forget about static class and follow below code now.
<h2>Full Plugin Code <em><span style="color: #999999;"><small><span style="color: #0000ff;"><a style="color: #0000ff;" title="Fork on Github" href="https://github.com/kutec/WhatsApp-Share-Button" target="_blank">Fork</a></span> on Github</small></span></em></h2>
<pre class="lang:default decode:true">(function ( $ ) {
 	 $.fn.wsBtn = function(options) {

		// Configuration
		var settings = $.extend({
			// These are the defaults.
			message			: "This button fires only in devices.",
			bgColor			: "#090",
			container		: ".post",
			target			: "h2"
		}, options );
 		
		this.each(function(){
			// Variables
			var el 			= $(this);
			var box			= el.find(settings.container);
			var targetTo	= box.find(settings.target);
			var aTag		= targetTo.find('a');
			var devices		= /Android|webOS|iPhone|iPad|iPod|BlackBerry|IEMobile|Opera Mini/i.test(navigator.userAgent);
			
			if(aTag &amp;&amp; devices){
				// appending WhatsApp Sharing button to container
				box.append("<a class="wa_btn wa_btn_s" href="#"><i class="fa fa-whatsapp"></i> Share</a>");
			}
			/*else{
				boxes.on("click",".wa_btn", function() {
					alert(settings.message);	
				});
			}*/
			box.on('click','.wa_btn',function(){
				var url 	= $(this).parent(box).find(aTag).attr('href');
				var txt		= $(this).parent(box).find(targetTo).text();
				var wmsg	= encodeURIComponent(txt)+" - "+encodeURIComponent(url);
				var wurl	= 'whatsapp://send?text='+wmsg;
				
				$(this).attr('href',wurl);
				$(this).attr('data-href',url);
				$(this).attr('data-text',txt);
				
			});
			
		});
    };
 
}( jQuery ));</pre>
We are done with the script now. If you are familiar with <a title="Skype URIs" href="https://msdn.microsoft.com/en-us/library/office/dn745878" target="_blank">Skype URIs</a> then <span class="lang:default decode:true  crayon-inline">var wurl = "whatsapp://send?text="+wmsg;</span> won't hesitate you. But let me know in <a title="Add Comment" href="#disqus_thread">comment</a> if you are not getting anything or have better idea.
<h2>Sample HTML</h2>
<pre class="lang:default decode:true">&lt;div class="posts"&gt;
    &lt;div class="post"&gt;
        &lt;h2&gt;&lt;a href="http://teckstack.com/how-to-configure-sass-for-html-projects"&gt;How to Configure SASS for HTML Projects&lt;/a&gt;&lt;/h2&gt;

        &lt;p&gt;SASS is booming the world with giving super powers to CSS and if you don’t know about it, you must gain your knowledge as a front end developer. The configuration for SASS is so simple but I observed that people avoids it or leave it to core developers. As I opine, when we can do more in less time, we should definitely go for it!&lt;/p&gt;

    &lt;/div&gt;
&lt;/div&gt;</pre>
As you can notice in above code, there is nothing for WhatsApp button as that will be appended dynamically.

See <a class="btn btn-success" title="Demo - WhatsApp Share Button" href="http://demo.teckstack.com/WhatsApp-Share-Button" target="_blank">Demo</a> or <a class="btn btn-info" title="Fork - WhatsApp Share Button" href="http://kutec.github.io/WhatsApp-Share-Button" target="_blank">Fork</a> on Github.
<h3>Conclusion</h3>
If you are a blogger, you should integrate WhatsApp share button. This would give you extra traffic which will be converted revenue for you. Also this will be displayed for portable devices for now, so if you want to suggest your blog to any friend through WhatsApp, you don't need to go to browser address bar to do so. Just share on a single click.

&nbsp;

Please add <a title="Add Comments" href="#disqus_thread">comments</a> to show your reaction to <a title="WhatsApp Share – New Way to Social Engagement" href="http://teckstack.com/whatsapp-share-button">this post</a>.
<h5><small>Image Artist: <a title="Image Drawn by Kinjal Mehta (Jayswal)" href="http://fb.com/kkinjal" target="_blank">Kinjal Jayswal (Mehta)</a></small></h5>