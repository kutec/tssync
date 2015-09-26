---
ID: 220
post_title: CSS Content
author: Kushal Jayswal
post_date: 2012-07-20 20:59:40
post_excerpt: ""
layout: post
permalink: http://teckstack.com/css-content
published: true
dsq_thread_id:
  - "773666772"
networkpub_postmessage:
  - ""
networkpub_twitterhandle:
  - ""
networkpub_twitterhash:
  - ""
better-related-:
  - 'a:6:{s:6:"offset";i:10000;s:5:"stime";d:1365755917.990107059478759765625;s:7:"queries";i:16;i:220;a:42:{i:1590;d:14.208988189697265625;i:1559;d:1.70067608356475830078125;i:1519;d:18.1172542572021484375;i:1352;d:21.8494968414306640625;i:1323;d:18.9624538421630859375;i:206;d:42.47625196025745708539034239947795867919921875;i:1197;d:20.4733692110726650525975855998694896697998046875;i:1104;d:24.3172931671142578125;i:970;d:14.68959808349609375;i:937;d:13.752063751220703125;i:912;d:13.5606212615966796875;i:893;d:12.67901515960693359375;i:874;d:29.198737323512517605195171199738979339599609375;i:846;d:53.41179159561487921337175066582858562469482421875;i:792;d:26.62519493931250025298140826635062694549560546875;i:774;d:16.4230518341064453125;i:731;d:38.49381599085236160817657946608960628509521484375;i:638;d:13.94100284576416015625;i:641;d:12.57515716552734375;i:439;d:13.898082733154296875;i:401;d:14.45181751251220703125;i:340;d:59.86300352493616827587175066582858562469482421875;i:200;d:22.7434253692626953125;i:263;d:31.0516181887337978650975855998694896697998046875;i:256;d:33.43396568541934499307899386622011661529541015625;i:240;d:78.9070438175518091838966938666999340057373046875;i:193;d:14.4555187225341796875;i:181;d:23.8739410341927822400975855998694896697998046875;i:165;d:10.6895130298755791642406620667316019535064697265625;i:154;d:2.9500091075897216796875;i:146;d:8.56728649139404296875;i:141;d:4.418494701385498046875;i:134;d:8.33851718902587890625;i:126;d:11.9039306640625;i:111;d:5.67108058929443359375;i:99;d:3.4481353759765625;i:88;d:5.654544353485107421875;i:82;d:7.224979400634765625;i:78;d:1.10993480682373046875;i:48;d:7.98906040191650390625;i:42;d:3.4654090404510498046875;i:24;d:25.2525134981820400525975855998694896697998046875;}s:5:"etime";d:1365755918.021276950836181640625;s:5:"ctime";i:1365755918;}'
networkpub_ogtype_facebook:
  - ""
disclosure_dropdown:
  - None
networkpub_postsummary:
  - ""
networkpub_post_image_video:
  - ""
awd_fcbk:
  - 'a:4:{s:11:"like_button";a:3:{s:8:"redefine";s:1:"0";s:7:"enabled";s:1:"0";s:5:"place";s:3:"top";}s:9:"opengraph";a:1:{s:11:"object_link";s:0:"";}s:7:"awd_ogp";a:16:{s:2:"id";s:0:"";s:12:"object_title";s:0:"";s:6:"locale";s:5:"en_US";s:10:"determiner";s:4:"auto";s:5:"title";s:7:"%TITLE%";s:4:"type";s:7:"article";s:11:"custom_type";s:10:"teckstack:";s:11:"description";s:13:"%DESCRIPTION%";s:9:"site_name";s:12:"%BLOG_TITLE%";s:3:"url";s:5:"%URL%";s:27:"auto_load_images_attachment";s:1:"0";s:6:"images";a:1:{i:0;s:0:"";}s:27:"auto_load_videos_attachment";s:1:"0";s:6:"videos";a:1:{i:0;s:0:"";}s:27:"auto_load_audios_attachment";s:1:"0";s:6:"audios";a:1:{i:0;s:0:"";}}s:30:"_nonce_options_save_ogp_object";s:10:"89f594fc89";}'
authorsure_include_css:
  - ""
views:
  - "965"
ac_is_copyprotect:
  - "1"
ac_is_advanced_tracking:
  - "1"
ac_postid:
  - 2fd3nqktUM5.text
ac_is_process:
  - "1"
ac_embedid:
  - 5914_5nntPH
vortex_system_likes:
  - "0"
vortex_system_dislikes:
  - "0"
---
<blockquote><strong><em>CSS Content is the easiest way to put some symbolic content like "&gt;" or something like this dynamically, before and after of the <a class="zem_slink" title="HTML element" href="http://en.wikipedia.org/wiki/HTML_element" target="_blank" rel="wikipedia">TAG</a> element. It can be apply with use of pseudo elements ":before" and ":after". </em></strong></blockquote>
<!--more-->
<h3>Please clear your mind...</h3>
<pre lang="css">p#test {
	content: "Your browser supports content";
}
p#test2 {
	content: url(../pix/logo_quirksmode.gif);
}</pre>
I faced some problem when working on large application development where I need to mention by arrow or image that the content is actually separated from specific area or something to make highlighted than usual text in <a class="zem_slink" title="Wine tasting descriptors" href="http://en.wikipedia.org/wiki/Wine_tasting_descriptors" target="_blank" rel="wikipedia">BODY</a> content. I found CSS Content trick very useful want to share with you.

It is great when you need to design breadcrumb in the website header. You can just pick <a class="zem_slink" title="Long Island" href="http://maps.google.com/maps?ll=40.8,-73.3&amp;spn=1.0,1.0&amp;q=40.8,-73.3%20%28Long%20Island%29&amp;t=h" target="_blank" rel="geolocation">LI</a> tag and apply the following CSS. And all without changing the structure of the code.
<pre lang="css">li:before { content: "&gt;&gt;"; }
#breadcrumbs:before { content: "You are here:"; margin-right: 0.5em; }</pre>
If you want to use some complex symbols like "$" or some other <a class="zem_slink" title="Currency sign" href="http://en.wikipedia.org/wiki/Currency_sign" target="_blank" rel="wikipedia">currency symbols</a>, you can <a title="Entity Conversion Calculator" href="http://www.evotech.net/articles/testjsentities.html" target="_blank">click here</a> to retrieve on a symbol conversion site.
<div class="zemanta-pixie" style="margin-top: 10px; height: 15px;"></div>