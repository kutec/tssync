---
ID: 2607
post_title: 'jQuery Events &#8211; Click, MouseDown, MouseUp'
author: Kushal Jayswal
post_date: 2014-05-31 21:12:23
post_excerpt: >
  jQuery is most common JavaScript library
  used by web developers today. Many
  popular frameworks are developed using
  jQuery and there is a big library exist
  for ready-to-use plugins build on it.
  You just need to google it up and you
  are there. Well! This article will
  clarify confusion between three jQuery
  events…
layout: post
permalink: >
  http://teckstack.com/jquery-events-click-mousedown-mouseup
published: true
authorsure_include_css:
  - ""
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
authorsure_hide_author_box:
  - ""
post_to_facebook_timeline:
  - "1"
switch_like_status:
  - "1"
dsq_thread_id:
  - "2775281719"
factory_shortcodes_assets:
  - 'a:1:{s:12:"sociallocker";b:1;}'
views:
  - "2880"
ac_is_copyprotect:
  - "1"
ac_is_advanced_tracking:
  - "1"
ac_postid:
  - 3Y5q3_AdtT8.text
ac_is_process:
  - "1"
ac_embedid:
  - 2-KRXG7o9xX
vortex_system_likes:
  - "1"
vortex_system_dislikes:
  - "0"
vortex_system_user_11:
  - 'a:2:{s:5:"liked";s:7:"noliked";s:8:"disliked";s:8:"disliked";}'
---
jQuery is most common JavaScript library used by web developers today. Many popular frameworks built upon jQuery and there is a big library exist for ready-to-use plugins. You just need to Google it up and you are there.

Well! This article will clarify confusion between three jQuery events...
<ol>
	<li><span class="lang:default decode:true  crayon-inline">mousedown()</span></li>
	<li><span class="lang:default decode:true  crayon-inline ">mouseup()</span></li>
	<li><span class="lang:default decode:true  crayon-inline">click()</span></li>
</ol>
<h2>jQuery - Mouse Down</h2>
[list icon="icon: check"]
<ul>
	<li>Very first thing I would like to describe here is the button identification. You can know which button of a mouse got pressed. Below code snippet showing the same example.</li>
	<li>Mouse Down event can use only for mouse keys and NOT for keyboard's keys. For keys we have different function keypress() . But we will discuss it in the next article.</li>
	<li>It can fire an event on X and Y co-ordinates</li>
</ul>
[/list]

<strong>Example </strong><em>(which mouse button got clicked)</em>
<pre class="lang:js mark:1 decode:true" title="Showing which mouse button is clicked">$('#btnClick').mousedown(function(event){
    switch (event.which) {
        case 1:
            alert('Left mouse button pressed');
            break;
        case 2:
            alert('Middle mouse button pressed');
            break;
        case 3:
            alert('Right mouse button pressed');
            break;
        default:
           break;
    }
});</pre>
<a class="btn btn-primary" title="Demo" href="http://jsfiddle.net/jquerybyexample/5fmch/" target="_blank">Demo</a>
<h2>jQuery - Click</h2>
Click is very useful and most used jQuery function as it can fire an event though mouse and keyboard too. Below are some comparison with <span class="lang:default decode:true  crayon-inline">mousedown()</span> .

[list icon="icon: check"]
<ul>
	<li>We can fire click event through keyboard's key like <em>space</em>, <em>enter</em>, etc. It is more convenient approach while we can control elements as per user's preference. Useful for user interaction</li>
</ul>
[/list]

[list icon="icon: times"]
<ul>
	<li>It cannot find which mouse button got pressed</li>
	<li>It cannot fire event for X and Y co-ordinates</li>
</ul>
[/list]
<h2>jQuery - Mouse Up</h2>
We cannot fire a click event once we have fired <span class="lang:default decode:true  crayon-inline ">mousedown()</span>  event. It fires after mouse released means <span class="lang:default decode:true  crayon-inline ">mouseup()</span>  event happened.

<strong>Example</strong> <em>(for comparison between mouseup and mousedown events)</em>
<pre class="lang:js mark:1,5 decode:true" title="Comparison - MouseUp and MouseDown Events">$('#mouseup').mouseup(function(){
	$('#mouseup').slideUp();
});
 
$('#mousedown').mousedown(function(){
	$('#mousedown').fadeOut();
});</pre>
<a class="btn btn-primary" title="Demo" href="http://www.mkyong.com/wp-content/uploads/jQuery/jQuery-mouseup-mousedown-example.html" target="_blank">Demo</a>
<h2><strong>Example</strong> <em>(Comparing all 3 events)</em></h2>
<pre class="lang:js mark:14,20 decode:true" title="Example - Comparing all 3 events">//this flag is checked against to see if the "click" function can happen
var clickIsValid = true;

//this is how many milliseconds you want to allow before click doesn't count
var delay = 500;

//this function sets the flag to false
var dontClick = function(){
 clickIsValid = false;
 $('.can-click').text(' not ');
}

//mousedown, a global variable is set to the timeout function
$('.target').mousedown( function(){
    $('.status').text('Mouse down');
    cancelClick = setTimeout( dontClick, delay );
})

//mouseup, the timeout for dontClick is cancelled
$('.target').mouseup( function(){
    $('.status').text('Mouse up');
    clearTimeout( cancelClick );
   
    //if the time limit wasn't passed, this will be true
    if(clickIsValid){
        // this is where you call the function you want to happen on  a quick click
        $('.click-or-no').text('Let\'s call that a click!');
    }else{
        $('.click-or-no').text('Let\'s not call that a click...');
    }
    //reset the values to their defaults
     clickIsValid = true;
    $('.can-click').text(' ');
})</pre>
<a class="btn btn-primary" title="Demo" href="http://jsfiddle.net/zRr4s/3/" target="_blank">Demo</a>
<h3>Resources</h3>
[list icon="icon: rss-square"]
<ul>
	<li><a title="DEMO - JSFiddle" href="http://jsfiddle.net/zRr4s/3/" target="_blank">JSFiddle</a></li>
	<li><a title="DEMO - jQuery By Example" href="http://jsfiddle.net/jquerybyexample/5fmch/" target="_blank">Jquery by Example</a></li>
	<li><a title="DEMO - MKYoung.com" href="http://www.mkyong.com/wp-content/uploads/jQuery/jQuery-mouseup-mousedown-example.html" target="_blank">MKYoung</a></li>
</ul>
[/list]