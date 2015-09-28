---
ID: 874
post_title: 'jQuery &#8211; Disable Click after N Number of Clicks'
author: Kushal Jayswal
post_date: 2012-12-09 18:18:21
post_excerpt: >
  I am here to focus on very easy trick to
  disabled the button after "n" numbers of
  click with BUTTON and HYPERLINK as well.
layout: post
permalink: >
  http://teckstack.com/jquery-disable-click
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
  - 'a:6:{s:6:"offset";i:3000;s:5:"stime";d:1365633905.51241588592529296875;s:7:"queries";i:11;i:874;a:42:{i:1590;d:33.67084819116507077296773786656558513641357421875;i:1559;d:0.792333066463470458984375;i:1519;d:32.78219825067434811671773786656558513641357421875;i:1352;d:2.283462047576904296875;i:1323;d:20.021385793332701297231324133463203907012939453125;i:206;d:19.780435715598624568656305200420320034027099609375;i:1197;d:4.06882190704345703125;i:1104;d:9.33711910247802734375;i:970;d:3.85530757904052734375;i:937;d:2.92929172515869140625;i:912;d:8.26250743865966796875;i:893;d:5.46729755401611328125;i:846;d:18.89195602728793943470009253360331058502197265625;i:792;d:17.371966008786802859731324133463203907012939453125;i:774;d:5.967538356781005859375;i:731;d:12.188311700467711062856324133463203907012939453125;i:638;d:12.527657155637388797231324133463203907012939453125;i:641;d:2.6793911457061767578125;i:439;d:4.57077884674072265625;i:401;d:17.298353795652037234731324133463203907012939453125;i:340;d:55.1171489023766270065607386641204357147216796875;i:200;d:2.760349750518798828125;i:263;d:59.8911725625224420355152687989175319671630859375;i:256;d:9.9984874725341796875;i:240;d:21.91014967658967549368753680028021335601806640625;i:220;d:25.38600550392121846243753680028021335601806640625;i:193;d:1.6533262729644775390625;i:181;d:9.046021035804603371843768400140106678009033203125;i:165;d:4.122285366058349609375;i:154;d:4.959084033966064453125;i:146;d:3.41822910308837890625;i:141;d:3.266068935394287109375;i:134;d:5.00598049163818359375;i:126;d:4.34696292877197265625;i:111;d:25.421944367322279134668860933743417263031005859375;i:99;d:15.961959485654478640981324133463203907012939453125;i:88;d:17.1627063751220703125;i:82;d:3.5613176822662353515625;i:78;d:10.4124889373779296875;i:48;d:1.32343065738677978515625;i:42;d:0.664298534393310546875;i:24;d:60.6499574059575223827778245322406291961669921875;}s:5:"etime";d:1365633905.536941051483154296875;s:5:"ctime";i:1365633905;}'
dsq_thread_id:
  - "966037397"
disclosure_dropdown:
  - None
authorsure_include_css:
  - ""
views:
  - "827"
ac_is_copyprotect:
  - "1"
ac_is_advanced_tracking:
  - "1"
ac_postid:
  - 6IwhA4oQiPg.text
ac_is_process:
  - "1"
ac_embedid:
  - 1DTDg_u7-ax
vortex_system_likes:
  - "0"
vortex_system_dislikes:
  - "0"
---
There may be a situation for a form validation when you need to disable a click of an anchor element or button after N number of clicks. This article will focus on the code for the same purpose.
<h3>The&nbsp;Requirement</h3>
It was something like I have to ADD one group of elements on a CLICK event. But the greatest numbers of adding it would be 9.

Frankly speaking I have tried with FOR LOOP with jQuery. But then I stroke that I can even do something different from this and though came in my mind was DISABLED attribute with HTML INPUT TAG. Let's have a look with code now that can work for example of "jQuery - Disabled Button/Link After N Clicks."
<h2>jQuery</h2>
<pre>$(function(){
  var count = 3,
      $btn = $("#addon"); 
	  //Or which ever you want
      //Change the label of $btn
      //$btn.val($btn.val()+' ('+count+')')
      
  $btn.click(function(){
      $btn.val($btn.val().replace(count,count-1));
      count--;
      if(count==0) {
            return !$btn.attr('disabled','disabled');
		/* FOR HYPERLINK
		return !$btn.unbind('click');
		*/
      }
  })
  
  //Adding GROUP of elements ONCLICK
  $("#addon").click(function() {
		for (var i = 0; i &lt; 1; i++) {
			$('#content form').append('&lt;input size="5" type="text" value="Text" /&gt;');
		}
	});
});</pre>
<h2>HTML</h2>
<pre>&lt;div id="content"&gt;
    &lt;form action="" name="form1"&gt;&lt;input size="5" type="text" value="Text" /&gt;

    &lt;/form&gt;
 
    &lt;input id="addon" size="5" type="submit" value="Add" /&gt;

    &lt;!--FOR HYPERLINK &lt;a id="addon" href="#" title="" id="addon"&gt;addon&lt;/a&gt; --&gt;

&lt;/div&gt;
</pre>
<h2>Demo</h2>
<iframe src="//jsfiddle.net/kutec/h4ua7hpj/embedded/result/" width="100%" height="200" frameborder="0" allowfullscreen="allowfullscreen"></iframe>