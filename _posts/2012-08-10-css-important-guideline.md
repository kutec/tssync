---
ID: 240
post_title: 'CSS Important &#8211; A Small Guideline'
author: Kushal Jayswal
post_date: 2012-08-10 20:09:47
post_excerpt: ""
layout: post
permalink: >
  http://teckstack.com/css-important-guideline
published: true
networkpub_postmessage:
  - ""
networkpub_twitterhandle:
  - ""
networkpub_twitterhash:
  - ""
dsq_thread_id:
  - "800525073"
better-related-:
  - 'a:6:{s:6:"offset";i:5000;s:5:"stime";d:1365773961.5842521190643310546875;s:7:"queries";i:14;i:240;a:41:{i:1590;d:25.9658069610595703125;i:1519;d:36.883419036865234375;i:1352;d:46.74109649658203125;i:1323;d:39.915332794189453125;i:206;d:49.15369708721453889666008763015270233154296875;i:1197;d:32.986385345458984375;i:1104;d:28.191997528076171875;i:970;d:21.6909809112548828125;i:937;d:18.219898223876953125;i:912;d:20.480106353759765625;i:893;d:20.831958770751953125;i:874;d:31.18837840740497568958744523115456104278564453125;i:846;d:66.3939845745380097241650219075381755828857421875;i:792;d:44.88757148155799114874753286130726337432861328125;i:774;d:19.3114414215087890625;i:731;d:50.98831675602838942040762049145996570587158203125;i:638;d:19.8136444091796875;i:641;d:22.161342620849609375;i:439;d:23.3682498931884765625;i:401;d:24.152782440185546875;i:340;d:80.4734652592585604224950657226145267486572265625;i:200;d:28.8702239990234375;i:263;d:56.630624330960785073330043815076351165771484375;i:256;d:68.9535390413724371683201752603054046630859375;i:220;d:119.803933950570893784970394335687160491943359375;i:193;d:34.500469207763671875;i:181;d:54.912133730374847573330043815076351165771484375;i:165;d:34.57672940767728420041748904623091220855712890625;i:154;d:9.097400665283203125;i:146;d:36.3366851806640625;i:141;d:10.33405017852783203125;i:134;d:15.91535854339599609375;i:126;d:23.2847766876220703125;i:111;d:12.7651920318603515625;i:99;d:4.310210704803466796875;i:88;d:17.4683895111083984375;i:82;d:8.9462146759033203125;i:78;d:1.18196856975555419921875;i:48;d:17.9295101165771484375;i:42;d:0.661465108394622802734375;i:24;d:42.944622039794921875;}s:5:"etime";d:1365773961.6165049076080322265625;s:5:"ctime";i:1365773961;}'
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
disclosure_position:
  - Above the Content
authorsure_include_css:
  - ""
views:
  - "1109"
ac_is_copyprotect:
  - "1"
ac_is_advanced_tracking:
  - "1"
ac_postid:
  - 4BVIWzfgFU0.text
ac_is_process:
  - "1"
ac_embedid:
  - 55Y3x0d5yt5
vortex_system_likes:
  - "0"
vortex_system_dislikes:
  - "0"
---
<p style="text-align: left;"><a href="/css" target="_blank">CSS</a> holds the power of styling <a href="http://www.w3.org/TR/html-markup/elements.html" target="_blank">HTML elements</a>. It has many <a href="http://www.w3.org/TR/selectors/" target="_blank">selectors</a> and all behaves as per their specificity or weightage. <a href="http://teckstack.com/how-to-deal-with-issues-in-css-specificity">CSS specificity</a> is a deep subject but this article will focus on the CSS !important property in terms of the best practice.</p>

<h2 style="text-align: left;">What is CSS Important</h2>
It was December 17, 1996, when <a href="http://www.w3.org/TR/REC-CSS1-961217#important">CSS !important</a> declaration has been introduced. And we still have it alive within our style sheets. !important helps developers to override CSS properties. But to be frank, using !important is not a good practice.
<h3>Syntax</h3>
<pre class="prettyprint">header {
   baackground-color: #000; /* Black color */
}

header {
   baackground-color: #fff !important; /* White color */
}
</pre>
<h2>Good</h2>
Although, using !important is not good practice, we have to use it to fix issues instantly. Sometime we have tight deadlines for a project and we may have a demo to present to client. At the last-minute you found some issue and do not have enough time to debug on it. Now? To avoid bad in such a situation, we of course use !important but it is really advisable to remove those !importants when you get enough time.
<h3>Plugin and 3rd Party Services</h3>
If you have to overwrite styling of a plugin then it is obvious to use !important. Extending plugin might be another solution but that would take expertise in JavaScript.

The same follows for 3rd party services, where we do not have control over the CSS and JS files.
<h3>User Theme</h3>
Sometime we have to offer color schemes for the same theme which user can change as per his choice. This kind of situation is handled by writing extra CSS. Most of the time we can avoid !important by adding ID or class on the parent element but if it's not possible then before using !important, we must check with backend developer.
<h2>Bad</h2>
There are many developers write CSS on ad hoc basis to fix the UI. Such a kind of CSS should be added to the theme in the end. But developer don't understand to update a theme developer  in most of the projects and it remains at the page level. Now if it is a big project then it might be grouped into phases. So, if !important has been used in Phase-1 then successful handover of Phase-1's deliverables might someone new in a team doesn't have idea for that !important.

<strong>Temp Issue Fixer</strong>: During unit testing and bug fixing might we have someone align on temp basis. Such a scenario can be dangerous because he might not have proper knowledge of the project and all pages. He may add !important for some CSS properties to fix the bugs quickly. I am sure you must go through such a situation :)
<h4>What Should I Do</h4>
You must not use !important in CSS files. Instead you should understand the CSS specificity and use ID or other high weightage CSS selector to overwrite the property.

If you have any question or want to share more use cases to help the community, please provide below in <a href="#comments" target="_blank">comment</a> section.