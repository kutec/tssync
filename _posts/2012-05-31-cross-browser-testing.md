---
ID: 126
post_title: Thoughts on Cross Browser Testing
author: Kushal Jayswal
post_date: 2012-05-31 18:57:52
post_excerpt: >
  Cross browser testing is an untold task
  for any web or front end developer. This
  post will focus in general that how
  front end testing should be done.
layout: post
permalink: >
  http://teckstack.com/cross-browser-testing
published: true
dsq_thread_id:
  - "709844466"
better-related-:
  - 'a:6:{s:6:"offset";i:0;s:5:"stime";d:1365859797.6264460086822509765625;s:7:"queries";i:9;i:126;a:43:{i:1618;d:11.376346588134765625;i:1590;d:14.75234127044677734375;i:1559;d:5.931935787200927734375;i:1519;d:17.91428375244140625;i:1352;d:70.805206298828125;i:1323;d:13.44364833831787109375;i:206;d:16.5970745086669921875;i:1197;d:13.8125667572021484375;i:1104;d:68.8279755691002179673887440003454685211181640625;i:970;d:10.00260162353515625;i:937;d:8.60352802276611328125;i:912;d:9.4670429229736328125;i:893;d:9.035022735595703125;i:874;d:6.448479175567626953125;i:846;d:20.44475555419921875;i:792;d:17.749176025390625;i:774;d:10.57027912139892578125;i:731;d:24.636386871337890625;i:638;d:16.8267841339111328125;i:641;d:7.658032894134521484375;i:439;d:18.27325439453125;i:401;d:15.50920867919921875;i:340;d:15.2807521820068359375;i:200;d:18.6156444549560546875;i:263;d:12.04132366180419921875;i:256;d:37.86041259765625;i:240;d:14.959384918212890625;i:220;d:18.554019927978515625;i:193;d:11.12424564361572265625;i:181;d:13.13736724853515625;i:165;d:19.56201171875;i:154;d:9.88373661041259765625;i:146;d:6.65592288970947265625;i:141;d:3.82917690277099609375;i:134;d:27.9030246734619140625;i:111;d:19.508907318115234375;i:99;d:37.517765045166015625;i:88;d:37.1641387939453125;i:82;d:61.383068084716796875;i:78;d:13.16411113739013671875;i:48;d:7.92173862457275390625;i:42;d:0;i:24;d:12.768154144287109375;}s:5:"etime";d:1365859797.6477859020233154296875;s:5:"ctime";i:1365859797;}'
disclosure_dropdown:
  - None
networkpub_postmessage:
  - ""
networkpub_postsummary:
  - ""
networkpub_twitterhandle:
  - ""
networkpub_twitterhash:
  - ""
networkpub_ogtype_facebook:
  - article
networkpub_post_image_video:
  - image
awd_fcbk:
  - 'a:4:{s:11:"like_button";a:3:{s:8:"redefine";s:1:"0";s:7:"enabled";s:1:"1";s:5:"place";s:3:"top";}s:9:"opengraph";a:1:{s:11:"object_link";s:0:"";}s:7:"awd_ogp";a:16:{s:2:"id";s:0:"";s:12:"object_title";s:0:"";s:6:"locale";s:5:"en_US";s:10:"determiner";s:4:"auto";s:5:"title";s:7:"%TITLE%";s:4:"type";s:7:"article";s:11:"custom_type";s:10:"teckstack:";s:11:"description";s:13:"%DESCRIPTION%";s:9:"site_name";s:12:"%BLOG_TITLE%";s:3:"url";s:5:"%URL%";s:27:"auto_load_images_attachment";s:1:"0";s:6:"images";a:1:{i:0;s:0:"";}s:27:"auto_load_videos_attachment";s:1:"0";s:6:"videos";a:1:{i:0;s:0:"";}s:27:"auto_load_audios_attachment";s:1:"0";s:6:"audios";a:1:{i:0;s:0:"";}}s:30:"_nonce_options_save_ogp_object";s:10:"89f594fc89";}'
authorsure_include_css:
  - ""
views:
  - "1070"
ac_is_copyprotect:
  - "1"
ac_is_advanced_tracking:
  - "1"
ac_postid:
  - 01v_WOXZQon.text
ac_is_process:
  - "1"
ac_embedid:
  - 7t9l2Abg1Oh
vortex_system_likes:
  - "0"
vortex_system_dislikes:
  - "0"
---
Cross browser testing is an untold task for any web or front end developer. As per the general observation, many developers pick one browser (i.e: Chrome, Firefox) to test their code and stick to it for a lifetime. They don't care for other browsers and leave testing to QA.

As per the best practice approach, one should test his/her code in all popular browsers (i.e.: Google Chrome, Mozilla Firefox, Safari, Opera, IE, etc.). If I talk about me, I keep open all the browsers and refresh each (one-by-one) after certain time to make sure that nothing is breaking. If the project has documented well, it must have a list of browsers and devices as per the requirement. Most commonly the keyword <strong>certified</strong> and <strong>supported</strong> are used for bifurcation.

In the start of my career, I was associated with a company, who asked for a screenshots be taken in all browsers as a proof that your code is working well in all browsers. This company was providing PSD to HTML services to their clients and hence they confirm the code of quality through screenshots. Of course this is a good thing for the company but hectic approach for developers. I had to spent at least 3-4 hours taking screenshots on the day of delivery. Definitely I would not suggest this approach but developer should take ownership of his code.
<h2>Adobe Browser Lab</h2>
Couple of years ago, <a href="http://blogs.adobe.com/browserlab/" target="_blank" rel="nofollow">Adobe Browser Lab</a> was a standard approach for testing your code in various browsers. But from <em>March 13, 2013</em>, the tool is no more available. (Section updated on Nov,2015)
<h2>Helpful Tools</h2>
<ol>
	<li><a href="http://www.browseemall.com/Home/" target="_blank" rel="nofollow">BrowseEmAll</a></li>
	<li><a href="http://www.my-debugbar.com/wiki/IETester/HomePage" target="_blank" rel="nofollow">IE Tester</a></li>
</ol>
Do you have more thoughts on this? Kindly <a href="#comments" target="_blank" rel="nofollow">comment</a> below.