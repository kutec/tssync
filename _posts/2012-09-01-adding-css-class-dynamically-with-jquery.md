---
ID: 340
post_title: Adding CSS Class Dynamically with Jquery
author: Kushal Jayswal
post_date: 2012-09-01 09:25:35
post_excerpt: >
  Add class to any HTML DIV or LI tags
  dynamically or using FOR LOOP or IF ELSE
  kind of structure you must extend your
  code by using JavaScript libraries.
layout: post
permalink: >
  http://teckstack.com/adding-css-class-dynamically-with-jquery
published: true
networkpub_postmessage:
  - ""
networkpub_twitterhandle:
  - ""
networkpub_twitterhash:
  - ""
better-related-:
  - 'a:6:{s:6:"offset";i:10000;s:5:"stime";d:1365418516.703649044036865234375;s:7:"queries";i:13;i:340;a:41:{i:1590;d:235.8862856351412347066798247396945953369140625;i:1519;d:244.8390139066256097066798247396945953369140625;i:1352;d:70.367645263671875;i:1323;d:171.9657686673677972066798247396945953369140625;i:206;d:216.76776944673974867328070104122161865234375;i:1197;d:197.939300537109375;i:1104;d:50.80020904541015625;i:970;d:193.0959625244140625;i:937;d:208.8943328857421875;i:912;d:172.64739990234375;i:893;d:195.783660888671875;i:874;d:97.1158547034630572625246713869273662567138671875;i:846;d:234.874309833233155586640350520610809326171875;i:792;d:206.7823732816256097066798247396945953369140625;i:774;d:202.63409423828125;i:731;d:222.6144467867337652933201752603054046630859375;i:638;d:192.1396425687349847066798247396945953369140625;i:641;d:135.5497589111328125;i:439;d:182.67620849609375;i:401;d:163.783203125;i:200;d:190.4135190523587652933201752603054046630859375;i:263;d:81.5233330359825885125246713869273662567138671875;i:256;d:83.9664459228515625;i:240;d:113.47302304781402426669956184923648834228515625;i:220;d:116.52061521089996176669956184923648834228515625;i:193;d:43.173290252685546875;i:181;d:52.04638877281775677374753286130726337432861328125;i:165;d:24.67883190741905963250246713869273662567138671875;i:154;d:13.17561626434326171875;i:146;d:36.283542633056640625;i:141;d:33.06050872802734375;i:134;d:27.631011962890625;i:126;d:39.26903533935546875;i:111;d:39.65739264855017864874753286130726337432861328125;i:99;d:21.26708874335655963250246713869273662567138671875;i:88;d:32.12511444091796875;i:82;d:20.999317169189453125;i:78;d:11.28833103179931640625;i:48;d:12.68219470977783203125;i:42;d:5.2827014923095703125;i:24;d:122.7010480440579982541748904623091220855712890625;}s:5:"etime";d:1365418516.7377378940582275390625;s:5:"ctime";i:1365418516;}'
dsq_thread_id:
  - "826579455"
networkpub_ogtype_facebook:
  - ""
disclosure_dropdown:
  - None
networkpub_postsummary:
  - ""
networkpub_post_image_video:
  - ""
disclosure_position:
  - Above the Content
authorsure_include_css:
  - ""
views:
  - "1291"
ac_is_copyprotect:
  - "1"
ac_is_advanced_tracking:
  - "1"
ac_postid:
  - 1P4D8D8CZ0d.text
ac_is_process:
  - "1"
ac_embedid:
  - 1IA5o5URiDV
vortex_system_likes:
  - "0"
vortex_system_dislikes:
  - "0"
---
<a class="zem_slink" title="Cascading Style Sheets" href="http://en.wikipedia.org/wiki/Cascading_Style_Sheets" target="_blank" rel="wikipedia">CSS</a> is the handle over <a class="zem_slink" title="HTML element" href="http://en.wikipedia.org/wiki/HTML_element" target="_blank" rel="wikipedia">HTML elements</a>. But we can't add class <a class="zem_slink" title="Dynamical system" href="http://en.wikipedia.org/wiki/Dynamical_system" target="_blank" rel="wikipedia">dynamically</a> with use of CSS only. If this is requirement to add class to any <a class="zem_slink" title="HTML" href="http://en.wikipedia.org/wiki/HTML" target="_blank" rel="wikipedia">HTML</a> <a class="zem_slink" title="Span and div" href="http://en.wikipedia.org/wiki/Span_and_div" target="_blank" rel="wikipedia">DIV</a> or LI tags (most commonly used) dynamically or using FOR LOOP or <a class="zem_slink" title="Conditional (programming)" href="http://en.wikipedia.org/wiki/Conditional_%28programming%29" target="_blank" rel="wikipedia">IF ELSE</a> kind of structure you must extend your code by using <a class="zem_slink" title="JavaScript library" href="http://en.wikipedia.org/wiki/JavaScript_library" target="_blank" rel="wikipedia">JavaScript libraries</a>.
<h2>I found the easiest solution for Adding CSS Class Dynamically with <a class="zem_slink" title="JQuery" href="http://jquery.com/" target="_blank" rel="homepage">Jquery</a></h2>
<h3><strong>HTML</strong></h3>
<pre class="prettyprint">
<ul class="quick_links">
	<li><a title="View Range" href="#">Link 1</a></li>
	<li><a title="View Range" href="#">Link 2</a></li>
	<li><a title="View Range" href="#">Link 3</a></li>
</ul>
</pre>
<h3><strong>JAVASCRIPT / <a class="zem_slink" title="JQuery" href="http://jquery.com/" target="_blank" rel="homepage">JQUERY</a></strong></h3>
<pre lang="prettyprint">
<script src="http://ajax.googleapis.com/ajax/libs/jquery/1.3.2/jquery.min.js"></script>
<script type="text/javascript">
    $(document).ready(function() {
        $ ('ul.image-list li:even').addClass('even');
        $ ('ul.image-list li:odd').addClass('odd');
    });
</script>
</pre>
&nbsp;

&nbsp;
<h6 class="zemanta-related-title" style="font-size: 1em;">Related articles</h6>
<ul class="zemanta-article-ul zemanta-article-ul-image" style="margin: 0; padding: 0; overflow: hidden;">
	<li class="zemanta-article-ul-li-image zemanta-article-ul-li" style="padding: 0; background: none; list-style: none; display: block; float: left; vertical-align: top; text-align: left; width: 84px; font-size: 11px; margin: 2px 10px 10px 2px;"><a style="box-shadow: 0px 0px 4px #999; padding: 2px; display: block; border-radius: 2px; text-decoration: none;" href="http://bryanforester.com/webdevtutcss/" target="_blank"><img style="padding: 0; margin: 0; border: 0; display: block; width: 80px; max-width: 100%;" alt="" src="http://www.teckstack.com/wp-content/uploads/2013/04/103791656_80_80.jpg" /></a><a style="display: block; overflow: hidden; text-decoration: none; line-height: 12pt; height: 80px; padding: 5px 2px 0 2px;" href="http://bryanforester.com/webdevtutcss/" target="_blank">CSS: Web Technologies From the Beginning</a></li>
	<li class="zemanta-article-ul-li-image zemanta-article-ul-li" style="padding: 0; background: none; list-style: none; display: block; float: left; vertical-align: top; text-align: left; width: 84px; font-size: 11px; margin: 2px 10px 10px 2px;"><a style="box-shadow: 0px 0px 4px #999; padding: 2px; display: block; border-radius: 2px; text-decoration: none;" href="http://www.daniweb.com/web-development/web-design-html-and-css/threads/432291/java-script-to-detect-screen-resolution-and-apply-the-css-file" target="_blank"><img style="padding: 0; margin: 0; border: 0; display: block; width: 80px; max-width: 100%;" alt="" src="http://www.teckstack.com/wp-content/uploads/2013/04/109466605_80_80.jpg" /></a><a style="display: block; overflow: hidden; text-decoration: none; line-height: 12pt; height: 80px; padding: 5px 2px 0 2px;" href="http://www.daniweb.com/web-development/web-design-html-and-css/threads/432291/java-script-to-detect-screen-resolution-and-apply-the-css-file" target="_blank">Java script to detect screen resolution and apply the css file</a></li>
	<li class="zemanta-article-ul-li-image zemanta-article-ul-li" style="padding: 0; background: none; list-style: none; display: block; float: left; vertical-align: top; text-align: left; width: 84px; font-size: 11px; margin: 2px 10px 10px 2px;"><a style="box-shadow: 0px 0px 4px #999; padding: 2px; display: block; border-radius: 2px; text-decoration: none;" href="http://www.hongkiat.com/blog/rwd-tools/" target="_blank"><img style="padding: 0; margin: 0; border: 0; display: block; width: 80px; max-width: 100%;" alt="" src="http://www.teckstack.com/wp-content/uploads/2013/04/101793077_80_80.jpg" /></a><a style="display: block; overflow: hidden; text-decoration: none; line-height: 12pt; height: 80px; padding: 5px 2px 0 2px;" href="http://www.hongkiat.com/blog/rwd-tools/" target="_blank">50 Useful Responsive Web Design Tools For Designers</a></li>
	<li class="zemanta-article-ul-li-image zemanta-article-ul-li" style="padding: 0; background: none; list-style: none; display: block; float: left; vertical-align: top; text-align: left; width: 84px; font-size: 11px; margin: 2px 10px 10px 2px;"><a style="box-shadow: 0px 0px 4px #999; padding: 2px; display: block; border-radius: 2px; text-decoration: none;" href="http://www.mt-soft.com.ar/2012/08/31/new-twitter-like-application-with-jquery-and-php/" target="_blank"><img style="padding: 0; margin: 0; border: 0; display: block; width: 80px; max-width: 100%;" alt="" src="http://www.teckstack.com/wp-content/uploads/2013/04/noimg_98_80_80.jpg" /></a><a style="display: block; overflow: hidden; text-decoration: none; line-height: 12pt; height: 80px; padding: 5px 2px 0 2px;" href="http://www.mt-soft.com.ar/2012/08/31/new-twitter-like-application-with-jquery-and-php/" target="_blank">New Twitter Like Application with JQuery and PHP</a></li>
</ul>
<div class="zemanta-pixie" style="margin-top: 10px; height: 15px;"><img class="zemanta-pixie-img" style="border: none; float: right;" alt="" src="http://img.zemanta.com/pixy.gif?x-id=c1239f7c-2fe0-4c36-a0b5-224120c8f9f9" /></div>