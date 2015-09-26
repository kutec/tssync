---
ID: 1684
post_title: YouTube Video as a Website Background
author: Kushal Jayswal
post_date: 2013-04-16 15:18:31
post_excerpt: "Yes it's true now you can use YouTube Video as Background of Website.You can give transparent background to content area to see video across content."
layout: post
permalink: >
  http://teckstack.com/youtube-video-as-a-website-background
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
  - "1215356257"
authorsure_include_css:
  - ""
views:
  - "1775"
ac_is_copyprotect:
  - "1"
ac_is_advanced_tracking:
  - "1"
ac_postid:
  - 1-l-M1Cyhlt.text
ac_is_process:
  - "1"
ac_embedid:
  - 4EGAyi7t9hm
vortex_system_likes:
  - "0"
vortex_system_dislikes:
  - "0"
---
Creativity has no bar. Earlier we use normal background with solid colors and then we started using background images and letter CSS3 has changed the trend by providing variety of color combination with different kind of gradient properties that is supported with all browsers (obviously with some hacks for IE). And now CSS3 background seems outdated as some of the websites are using <strong><a class="zem_slink" title="YouTube" href="http://en.wikipedia.org/wiki/YouTube" target="_blank" rel="wikipedia">YouTube</a> Video as Background of <a class="zem_slink" title="Website" href="http://en.wikipedia.org/wiki/Website" target="_blank" rel="wikipedia">Website</a></strong>.
<blockquote><strong>Yes it's true now you can use video as a background of your website. Means it would be like you can place video as a background and all content be over that video. You can give&nbsp;transparent&nbsp;background to content area. So video can be seen across the content area as well.</strong></blockquote>
Here I present some of the tricks you can use. You should have basic knowledge of <a class="zem_slink" title="HTML" href="http://en.wikipedia.org/wiki/HTML" target="_blank" rel="wikipedia">HTML</a>, <a class="zem_slink" title="Cascading Style Sheets" href="http://en.wikipedia.org/wiki/Cascading_Style_Sheets" target="_blank" rel="wikipedia">CSS</a> and <a class="zem_slink" title="JavaScript" href="http://en.wikipedia.org/wiki/JavaScript" target="_blank" rel="wikipedia">JavaScript</a>.

There are a couple of ways you can use.
<ol>
	<li>Better to use simple code by adding IFRAME just to the next of <a class="zem_slink" title="HTML element" href="http://en.wikipedia.org/wiki/HTML_element" target="_blank" rel="wikipedia">BODY tag</a> of HTML page adding <a class="zem_slink" title="Z-index" href="http://en.wikipedia.org/wiki/Z-index" target="_blank" rel="wikipedia">Z-INDEX</a> value "-1".
<pre class="prettyprint prettyprinted">
<div style="position: fixed; z-index: -99; width: 100%; height: 100%">
	<iframe frameborder="0" height="100%" width="100%" src="https://youtube.com/embed/VIDEOID?autoplay=1&controls=0&showinfo=0&autohide=1">
    	// replace VIDEOID with the ID fo VIDEO you want
  	</iframe>
</div>
</pre></li>
	<li>One option is <a title="mb.YTPLAYER" href="http://pupunzi.com/#mb.components/mb.YTPlayer/YTPlayer.html" target="_blank"><strong>jquery.mb.YTPLAYER</strong></a> plugin. I&nbsp;recommend this if you are using <a title="WordPress Plugin" href="http://wordpress.org/extend/plugins/wpmbytplayer/" target="_blank">WordPress</a>.</li>
	<li>Another plugin is known as <strong><a title="TABULAR jQuery Plugin" href="https://code.google.com/p/jquery-tubular/" target="_blank">TABULAR</a></strong>.</li>
</ol>

<div class="zemanta-pixie" style="margin-top: 10px; height: 15px;"><img class="zemanta-pixie-img" style="border: none; float: right;" alt="" src="http://img.zemanta.com/pixy.gif?x-id=6f9de612-2785-4209-956d-1d906c5ea497" /></div>