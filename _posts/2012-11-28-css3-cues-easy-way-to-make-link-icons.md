---
ID: 846
post_title: 'CSS3 Cues &#8211; Easy way to make link Icons'
author: Kushal Jayswal
post_date: 2012-11-28 18:44:56
post_excerpt: "CSS3 Cues is the way you can simply apply different icons for different extensions' files and that makes various category in your web easy-to-find, believe me."
layout: post
permalink: >
  http://teckstack.com/css3-cues-easy-way-to-make-link-icons
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
better-related-:
  - 'a:6:{s:6:"offset";i:10000;s:5:"stime";d:1365418497.428081989288330078125;s:7:"queries";i:14;i:846;a:40:{i:1519;d:280.01274226262017918998026289045810699462890625;i:1352;d:83.04590606689453125;i:1323;d:217.89318965031549168998026289045810699462890625;i:206;d:251.606448729526135821288335137069225311279296875;i:1197;d:264.664703369140625;i:1104;d:87.4478607177734375;i:970;d:255.2628021240234375;i:937;d:278.59649658203125;i:912;d:228.7012786865234375;i:893;d:253.227691650390625;i:874;d:47.441052259236158761268598027527332305908203125;i:792;d:271.7868545663650365895591676235198974609375;i:774;d:271.410736083984375;i:731;d:269.38979377440676898913807235658168792724609375;i:638;d:264.94435237004205418998026289045810699462890625;i:641;d:183.46295166015625;i:439;d:263.70001220703125;i:401;d:213.86644099308892918998026289045810699462890625;i:340;d:322.5543067870947879782761447131633758544921875;i:200;d:239.23980712890625;i:263;d:82.1300506591796875;i:256;d:144.6644062011646383325569331645965576171875;i:240;d:127.1043391826778048425694578327238559722900390625;i:220;d:133.6045104463836423747125081717967987060546875;i:193;d:56.749034881591796875;i:181;d:50.851688385009765625;i:165;d:84.2630092914287871508349780924618244171142578125;i:154;d:6.904185771942138671875;i:146;d:47.154003143310546875;i:141;d:39.910976409912109375;i:134;d:43.457584381103515625;i:126;d:53.44266510009765625;i:111;d:13.009372711181640625;i:99;d:8.588169097900390625;i:88;d:39.78261566162109375;i:82;d:27.9044170379638671875;i:78;d:7.22426700592041015625;i:48;d:18.529911041259765625;i:42;d:0.63706719875335693359375;i:24;d:169.1576690673828125;}s:5:"etime";d:1365418497.4834721088409423828125;s:5:"ctime";i:1365418497;}'
dsq_thread_id:
  - "948512553"
disclosure_dropdown:
  - None
authorsure_include_css:
  - ""
views:
  - "1396"
ac_is_copyprotect:
  - "1"
ac_is_advanced_tracking:
  - "1"
ac_postid:
  - 10-3mxg9g8G.text
ac_is_process:
  - "1"
ac_embedid:
  - 4opfoqASVPw
vortex_system_likes:
  - "0"
vortex_system_dislikes:
  - "0"
---
If you are working on a big application or a web portal where you need to show different <a class="zem_slink" title="Icon" href="http://en.wikipedia.org/wiki/Icon" target="_blank" rel="wikipedia">icons</a> (to get it separate manually with <a class="zem_slink" title="Cascading Style Sheets" href="http://en.wikipedia.org/wiki/Cascading_Style_Sheets" target="_blank" rel="wikipedia">CSS</a> CLASS or CSS ID) then "<a class="zem_slink" title="Cascading Style Sheets" href="http://en.wikipedia.org/wiki/Cascading_Style_Sheets" target="_blank" rel="wikipedia">CSS3</a> Cues" is the best solution.

<blockquote><strong>CSS3 Cues is the way came out as a part of CSS3. You can simply apply different icons for different extensions' files and that would make various category in your application / website very easy-to-find, believe me.</strong></blockquote>

<h3>PDF Extension (.PDF)</h3>

<pre>a[<a class="zem_slink" title="HTML element" href="http://en.wikipedia.org/wiki/HTML_element" target="_blank" rel="wikipedia">href</a> $='.pdf'] {
     background: transparent url('img/icon/pdf.png') 0 0 no-repeat;
     padding-right: 20px;
}</pre>

<h3>EXCEL Extension (<a class="zem_slink" title="Microsoft Excel" href="http://office.microsoft.com/en-us/excel" target="_blank" rel="homepage">.XLS</a>)</h3>

<pre>a[href $='.xls'] {
     background: transparent url('img/icon/xls.png') 0 0 no-repeat;
     padding-left: 20px;
}</pre>

<h3>PHOTOSHOP EXTENSION (<a class="zem_slink" title="Adobe Photoshop" href="http://adobe.com/photoshop" target="_blank" rel="homepage">.PSD</a>)</h3>

<pre>a[href $='.psd'] {
     background: transparent url('img/icon/psd.png') 0 0 no-repeat;
     padding-left: 20px;
}</pre>

<h3>Word EXTENSION (<a class="zem_slink" title="DOC (computing)" href="http://en.wikipedia.org/wiki/DOC_%28computing%29" target="_blank" rel="wikipedia">.doc</a>)</h3>

<pre>a[href $='.doc'] {
     background: transparent url('img/icon/doc.png') 0 0 no-repeat;
     padding-left: 20px;
}</pre>

[caption id="" align="alignright" width="214"]<a href="http://commons.wikipedia.org/wiki/File:Css3.jpg" target="_blank"><img class="zemanta-img-inserted zemanta-img-configured" title="English: CSS3 - Styling" alt="English: CSS3 - Styling" src="http://www.teckstack.com/wp-content/uploads/2013/03/Css31.jpg" width="214" height="186" /></a> English: CSS3 - Styling (Photo credit: Wikipedia)[/caption]

All above snippet would work to show various icons for proper extensions. And 20px padding to adjust icons before the text. Or you cant just put text-indent to its minus value if you want only icons.

Well I had another thought while I was working on a client project. I wanted to set right icon for EMAIL link, <a class="zem_slink" title="Hypertext Transfer Protocol" href="http://en.wikipedia.org/wiki/Hypertext_Transfer_Protocol" target="_blank" rel="wikipedia">HTTP</a> <a class="zem_slink" title="Uniform Resource Locator" href="http://en.wikipedia.org/wiki/Uniform_Resource_Locator" target="_blank" rel="wikipedia">URL</a> and URL that opens in new window. The links were come dynamically so I was not able to do manually by applying CSS CLASS. I really want to that CSS3 that saved one of my client. Hats off to CSS3, really. Below snippet will show code for said thoughts.

<h3>Links begin with "<a class="zem_slink" title="Mailto" href="http://en.wikipedia.org/wiki/Mailto" target="_blank" rel="wikipedia">Mailto</a>:"</h3>

<pre>a[href ^='mailto:'] {
     background: transparent url('img/icon/email.png') 0 0 no-repeat;
     padding-left: 20px;
}</pre>

<h3> LINKS BEGIN WITH "http://"</h3>

<pre>a[href ^='http://'] {
     background: transparent url('img/icon/url.png') 0 0 no-repeat;
     padding-left: 20px;
}</pre>

<h3>LINKS "TO TOP"</h3>

<pre>a[href ^='#'] {
     background: transparent url('img/icon/totop.png') 0 0 no-repeat;
     padding-left: 20px;
}</pre>

<h3> LINKS open in "new window"</h3>

<pre>a[target ='_blank'] {
     background: transparent url('img/icon/url_blank.png') 0 0 no-repeat;
     padding-left: 20px;
}</pre>

<h6 class="zemanta-related-title" style="font-size: 1em;"></h6>

<h6 class="zemanta-related-title" style="font-size: 1em;">Related articles</h6>

<ul class="zemanta-article-ul zemanta-article-ul-image" style="margin: 0; padding: 0; overflow: hidden;">
    <li class="zemanta-article-ul-li-image zemanta-article-ul-li" style="padding: 0; background: none; list-style: none; display: block; float: left; vertical-align: top; text-align: left; width: 84px; font-size: 11px; margin: 2px 10px 10px 2px;"><a style="box-shadow: 0px 0px 4px #999; padding: 2px; display: block; border-radius: 2px; text-decoration: none;" href="http://www.ahrefmagazine.com/web-design/30-useful-css-snippets-for-developers" target="_blank"><img style="padding: 0; margin: 0; border: 0; display: block; width: 80px; max-width: 100%;" alt="" src="http://www.teckstack.com/wp-content/uploads/2013/03/127212568_80_801.jpg" /></a><a style="display: block; overflow: hidden; text-decoration: none; line-height: 12pt; height: 80px; padding: 5px 2px 0 2px;" href="http://www.ahrefmagazine.com/web-design/30-useful-css-snippets-for-developers" target="_blank">30 Useful CSS Snippets for Developers</a></li>
    <li class="zemanta-article-ul-li-image zemanta-article-ul-li" style="padding: 0; background: none; list-style: none; display: block; float: left; vertical-align: top; text-align: left; width: 84px; font-size: 11px; margin: 2px 10px 10px 2px;"><a style="box-shadow: 0px 0px 4px #999; padding: 2px; display: block; border-radius: 2px; text-decoration: none;" href="http://alexmaccaw.com/posts/growl" target="_blank"><img style="padding: 0; margin: 0; border: 0; display: block; width: 80px; max-width: 100%;" alt="" src="http://www.teckstack.com/wp-content/uploads/2013/03/noimg_53_80_801.jpg" /></a><a style="display: block; overflow: hidden; text-decoration: none; line-height: 12pt; height: 80px; padding: 5px 2px 0 2px;" href="http://alexmaccaw.com/posts/growl" target="_blank">jQuery Growl with CSS3</a></li>
    <li class="zemanta-article-ul-li-image zemanta-article-ul-li" style="padding: 0; background: none; list-style: none; display: block; float: left; vertical-align: top; text-align: left; width: 84px; font-size: 11px; margin: 2px 10px 10px 2px;"><a style="box-shadow: 0px 0px 4px #999; padding: 2px; display: block; border-radius: 2px; text-decoration: none;" href="http://lifeascode.com/2012/09/29/replacing-images-and-icons-with-web-fonts-in-web-intefaces/" target="_blank"><img style="padding: 0; margin: 0; border: 0; display: block; width: 80px; max-width: 100%;" alt="" src="http://www.teckstack.com/wp-content/uploads/2013/03/115362992_80_801.jpg" /></a><a style="display: block; overflow: hidden; text-decoration: none; line-height: 12pt; height: 80px; padding: 5px 2px 0 2px;" href="http://lifeascode.com/2012/09/29/replacing-images-and-icons-with-web-fonts-in-web-intefaces/" target="_blank">Replacing images and icons with CSS3 web fonts</a></li>
    <li class="zemanta-article-ul-li-image zemanta-article-ul-li" style="padding: 0; background: none; list-style: none; display: block; float: left; vertical-align: top; text-align: left; width: 84px; font-size: 11px; margin: 2px 10px 10px 2px;"><a style="box-shadow: 0px 0px 4px #999; padding: 2px; display: block; border-radius: 2px; text-decoration: none;" href="http://www.onextrapixel.com/2012/11/28/create-a-glossy-photo-effect-with-css3/" target="_blank"><img style="padding: 0; margin: 0; border: 0; display: block; width: 80px; max-width: 100%;" alt="" src="http://www.teckstack.com/wp-content/uploads/2013/03/128633312_80_801.jpg" /></a><a style="display: block; overflow: hidden; text-decoration: none; line-height: 12pt; height: 80px; padding: 5px 2px 0 2px;" href="http://www.onextrapixel.com/2012/11/28/create-a-glossy-photo-effect-with-css3/" target="_blank">Create a Glossy Photo Effect with CSS3</a></li>
    <li class="zemanta-article-ul-li-image zemanta-article-ul-li" style="padding: 0; background: none; list-style: none; display: block; float: left; vertical-align: top; text-align: left; width: 84px; font-size: 11px; margin: 2px 10px 10px 2px;"><a style="box-shadow: 0px 0px 4px #999; padding: 2px; display: block; border-radius: 2px; text-decoration: none;" href="http://www.queness.com/post/13033/make-cool-effect-with-css3-animation-libraries" target="_blank"><img style="padding: 0; margin: 0; border: 0; display: block; width: 80px; max-width: 100%;" alt="" src="http://www.teckstack.com/wp-content/uploads/2013/03/124527214_80_801.jpg" /></a><a style="display: block; overflow: hidden; text-decoration: none; line-height: 12pt; height: 80px; padding: 5px 2px 0 2px;" href="http://www.queness.com/post/13033/make-cool-effect-with-css3-animation-libraries" target="_blank">Make Cool Effect with CSS3 Animation Libraries</a></li>
</ul>

<div class="zemanta-pixie" style="margin-top: 10px; height: 15px;"><img class="zemanta-pixie-img" style="border: none; float: right;" alt="" src="http://img.zemanta.com/pixy.gif?x-id=25f35a81-220c-43ae-957d-05f6eafbda49" /></div>