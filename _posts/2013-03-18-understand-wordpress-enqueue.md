---
ID: 1519
post_title: Understand WordPress Enqueue
author: Kushal Jayswal
post_date: 2013-03-18 17:01:37
post_excerpt: >
  Fixing jQuery bug while installing
  plugin, new and old versions of scripts
  can conflict. And adding given code of
  snippet will help a lot.
layout: post
permalink: >
  http://teckstack.com/understand-wordpress-enqueue
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
better-related-:
  - 'a:6:{s:6:"offset";i:10000;s:5:"stime";d:1365599732.3035221099853515625;s:7:"queries";i:9;i:1519;a:42:{i:1590;d:289.77974622002960813915706239640712738037109375;i:1559;d:21.038768768310546875;i:1352;d:56.17688751220703125;i:1323;d:207.916195339626739269078825600445270538330078125;i:206;d:221.628538402104283022708841599524021148681640625;i:1197;d:257.79715988919195979178766719996929168701171875;i:1104;d:53.812692912602329897708841599524021148681640625;i:970;d:224.054931640625;i:937;d:247.3533935546875;i:912;d:225.06246445462164729178766719996929168701171875;i:893;d:230.51904296875;i:874;d:76.148955509580417810866492800414562225341796875;i:846;d:221.534862942165801769078825600445270538330078125;i:792;d:207.831371731228301769078825600445270538330078125;i:774;d:242.507444652104283022708841599524021148681640625;i:731;d:214.405224270290801769078825600445270538330078125;i:638;d:241.276587650693699060866492800414562225341796875;i:641;d:162.4212188720703125;i:439;d:207.07171630859375;i:401;d:185.677242702907989269078825600445270538330078125;i:340;d:275.17793957940460813915706239640712738037109375;i:200;d:203.160736083984375;i:263;d:52.835893901371861147708841599524021148681640625;i:256;d:57.854793548583984375;i:240;d:50.345554351806640625;i:220;d:49.104366302490234375;i:193;d:40.38897705078125;i:181;d:59.69443009182867854178766719996929168701171875;i:165;d:19.77509307861328125;i:154;d:9.70126438140869140625;i:146;d:48.63303375244140625;i:141;d:28.929645538330078125;i:134;d:36.63991546630859375;i:126;d:35.114086151123046875;i:111;d:44.78787300869879572928766719996929168701171875;i:99;d:42.816534466213653331578825600445270538330078125;i:88;d:28.6840572357177734375;i:82;d:42.127414703369140625;i:78;d:6.138879299163818359375;i:48;d:42.623331340336704897708841599524021148681640625;i:42;d:5.7433185577392578125;i:24;d:120.58001969143805354178766719996929168701171875;}s:5:"etime";d:1365599732.3583939075469970703125;s:5:"ctime";i:1365599732;}'
dsq_thread_id:
  - "1147129329"
authorsure_include_css:
  - ""
views:
  - "2209"
ac_is_copyprotect:
  - "1"
ac_is_advanced_tracking:
  - "1"
ac_postid:
  - 7pyKBgHdbiJ.text
ac_is_process:
  - "1"
ac_embedid:
  - 36Rm7sfGkVT
vortex_system_likes:
  - "0"
vortex_system_dislikes:
  - "0"
---
<blockquote>I was working on a project in <strong><a class="zem_slink" title="WordPress" href="http://wordpress.org" target="_blank" rel="homepage">WordPress</a></strong> and stuck in between while plugin for content-slider working fine in <span style="color: #339966;"><em><a class="zem_slink" title="Firefox" href="http://en.wikipedia.org/wiki/Firefox" target="_blank" rel="wikipedia">Mozilla Firefox</a></em></span> and <span style="color: #339966;"><em>IE</em></span> but not in <span style="color: #ff0000;"><strong><em>Chrome</em></strong></span>. It was big problem as I had to deliver the project. <em style="line-height: 1.714285714;"><strong>Finally I found the solution. You can say OLD and NEW version of  <a class="zem_slink" title="JQuery" href="http://en.wikipedia.org/wiki/JQuery" target="_blank" rel="wikipedia">jQuery</a> <a class="zem_slink" title="Error message" href="http://en.wikipedia.org/wiki/Error_message" target="_blank" rel="wikipedia">script error</a> which is browser specific. And below code will fix it.</strong></em></blockquote>
Goto THEME folder and open <code>Functions.php </code>file. Paste the following code at the end of the file.
<pre>function my_scripts_method() {
   wp_deregister_script( 'jquery' );
   wp_register_script( 'jquery', 'http://code.jquery.com/jquery-1.4.4.min.js');
   wp_enqueue_script( 'jquery' );
}
add_action('wp_enqueue_scripts', 'my_scripts_method');</pre>
That's it!

&nbsp;
<h6 class="zemanta-related-title" style="font-size: 1em;">Related articles</h6>
<ul class="zemanta-article-ul zemanta-article-ul-image" style="margin: 0; padding: 0; overflow: hidden;">
	<li class="zemanta-article-ul-li-image zemanta-article-ul-li" style="padding: 0; background: none; list-style: none; display: block; float: left; vertical-align: top; text-align: left; width: 84px; font-size: 11px; margin: 2px 10px 10px 2px;"><a style="box-shadow: 0px 0px 4px #999; padding: 2px; display: block; border-radius: 2px; text-decoration: none;" href="http://stackoverflow.com/questions/15438521/jquery-custom-content-scroller-doesnt-work-in-chrome" target="_blank"><img style="padding: 0; margin: 0; border: 0; display: block; width: 80px; max-width: 100%;" alt="" src="http://www.teckstack.com/wp-content/uploads/2013/03/152747316_80_80.jpg" /></a><a style="display: block; overflow: hidden; text-decoration: none; line-height: 12pt; height: 80px; padding: 5px 2px 0 2px;" href="http://stackoverflow.com/questions/15438521/jquery-custom-content-scroller-doesnt-work-in-chrome" target="_blank">jQuery custom content scroller doesn't work in Chrome</a></li>
	<li class="zemanta-article-ul-li-image zemanta-article-ul-li" style="padding: 0; background: none; list-style: none; display: block; float: left; vertical-align: top; text-align: left; width: 84px; font-size: 11px; margin: 2px 10px 10px 2px;"><a style="box-shadow: 0px 0px 4px #999; padding: 2px; display: block; border-radius: 2px; text-decoration: none;" href="http://poststat.us/never-load-jquery-from-google-in-themes-and-plugins/" target="_blank"><img style="padding: 0; margin: 0; border: 0; display: block; width: 80px; max-width: 100%;" alt="" src="http://www.teckstack.com/wp-content/uploads/2013/03/150369844_80_80.jpg" /></a><a style="display: block; overflow: hidden; text-decoration: none; line-height: 12pt; height: 80px; padding: 5px 2px 0 2px;" href="http://poststat.us/never-load-jquery-from-google-in-themes-and-plugins/" target="_blank">Never load jQuery from Google in themes and plugins</a></li>
	<li class="zemanta-article-ul-li-image zemanta-article-ul-li" style="padding: 0; background: none; list-style: none; display: block; float: left; vertical-align: top; text-align: left; width: 84px; font-size: 11px; margin: 2px 10px 10px 2px;"><a style="box-shadow: 0px 0px 4px #999; padding: 2px; display: block; border-radius: 2px; text-decoration: none;" href="http://www.noupe.com/jquery/jquery-custom-content-scroller-does-away-with-ugly-scrollbars-75441.html" target="_blank"><img style="padding: 0; margin: 0; border: 0; display: block; width: 80px; max-width: 100%;" alt="" src="http://www.teckstack.com/wp-content/uploads/2013/03/152784339_80_80.jpg" /></a><a style="display: block; overflow: hidden; text-decoration: none; line-height: 12pt; height: 80px; padding: 5px 2px 0 2px;" href="http://www.noupe.com/jquery/jquery-custom-content-scroller-does-away-with-ugly-scrollbars-75441.html" target="_blank">jQuery Custom Content Scroller Does Away With Ugly Scrollbars</a></li>
	<li class="zemanta-article-ul-li-image zemanta-article-ul-li" style="padding: 0; background: none; list-style: none; display: block; float: left; vertical-align: top; text-align: left; width: 84px; font-size: 11px; margin: 2px 10px 10px 2px;"><a style="box-shadow: 0px 0px 4px #999; padding: 2px; display: block; border-radius: 2px; text-decoration: none;" href="http://alexking.org/blog/2013/03/17/announcing-threads" target="_blank"><img style="padding: 0; margin: 0; border: 0; display: block; width: 80px; max-width: 100%;" alt="" src="http://www.teckstack.com/wp-content/uploads/2013/03/153033636_80_80.jpg" /></a><a style="display: block; overflow: hidden; text-decoration: none; line-height: 12pt; height: 80px; padding: 5px 2px 0 2px;" href="http://alexking.org/blog/2013/03/17/announcing-threads" target="_blank">Announcing Threads</a></li>
	<li class="zemanta-article-ul-li-image zemanta-article-ul-li" style="padding: 0; background: none; list-style: none; display: block; float: left; vertical-align: top; text-align: left; width: 84px; font-size: 11px; margin: 2px 10px 10px 2px;"><a style="box-shadow: 0px 0px 4px #999; padding: 2px; display: block; border-radius: 2px; text-decoration: none;" href="http://eamann.com/tech/dont-dequeue-wordpress-jquery/" target="_blank"><img style="padding: 0; margin: 0; border: 0; display: block; width: 80px; max-width: 100%;" alt="" src="http://www.teckstack.com/wp-content/uploads/2013/03/142740154_80_80.jpg" /></a><a style="display: block; overflow: hidden; text-decoration: none; line-height: 12pt; height: 80px; padding: 5px 2px 0 2px;" href="http://eamann.com/tech/dont-dequeue-wordpress-jquery/" target="_blank">Don't Dequeue WordPress' jQuery</a></li>
</ul>
<div class="zemanta-pixie" style="margin-top: 10px; height: 15px;"><img class="zemanta-pixie-img" style="border: none; float: right;" alt="" src="http://img.zemanta.com/pixy.gif?x-id=90942190-9301-4d1d-bc05-78489afbcb82" /></div>