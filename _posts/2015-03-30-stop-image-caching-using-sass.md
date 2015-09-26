---
ID: 3522
post_title: Stop Image Caching using SASS
author: Ashish Panchal
post_date: 2015-03-30 13:51:30
post_excerpt: ""
layout: post
permalink: >
  http://teckstack.com/stop-image-caching-using-sass
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
  - 'a:2:{i:3306;b:1;i:3217;b:1;}'
post_to_facebook_timeline:
  - "1"
views:
  - "2977"
facebook_status_messages:
  - 'a:1:{i:0;a:2:{s:7:"message";s:235:"Failed posting to your Facebook Timeline. Error: {&quot;message&quot;:&quot;Application with ID 183204455028760 has not been granted the capability to use the property fb:explicitly_shared.&quot;,&quot;type&quot;:&quot;Exception&quot;}";s:5:"error";b:1;}}'
dsq_thread_id:
  - "3639534314"
wbounce_status:
  - default
post_views_count:
  - "10"
ac_is_copyprotect:
  - "1"
ac_is_advanced_tracking:
  - "1"
ac_postid:
  - 7_sHNW9lKPV.text
ac_is_process:
  - "1"
ac_embedid:
  - 7DZfi6EEfnA
vortex_system_likes:
  - "0"
vortex_system_dislikes:
  - "0"
---
<blockquote>Developer prefers to cache assets of the project to enhance overall performance. In most cases, these assets are <a title="jQuery and JavaScript" href="http://teckstack.com/js">scripts</a>, <a title="CSS" href="http://teckstack.com/css">css</a> and images. Caching helps user to save bandwidth and load pages faster. But every coin has two sides. If you use <a title="Spin and pulsate loader image" href="http://preloaders.net/en/circular/spin-and-pulsate/" target="_blank">animated GIF with multiple loops</a> as a single image then it might not work properly, if cached is on.</blockquote>
This is my first article on <a title="TeckStack" href="http://teckstack.com">TeckStack.com</a> and today we have the same thing to discuss - "<a title="Stop Image Caching using SASS" href="http://teckstack.com/stop-image-caching-using-sass">Stop Image Caching using SASS</a>". If you don't know about <a title="Articles on SASS" href="http://teckstack.com/sass">SASS</a> then you should know <a class="mentionable" href="http://teckstack.com/how-to-configure-sass-for-html-projects" data-mentionable="3306">How to Configure SASS for HTML Projects</a> and learn new tricks like <a class="mentionable" href="http://teckstack.com/creating-color-palette-sass" data-mentionable="3217">Creating Color Palette with SASS</a>. Let's focus on the topic...
<h2>What is GIF Image</h2>
Generally <abbr title="Graphics Interchange Format">GIF</abbr> refers to image format - <span class="lang:default decode:true  crayon-inline ">.gif</span>  - that can be created using Adobe Photoshop (or CorelDraw, Illustrator like tools) in form of animation or static. While talking about animation it is tightly coupled with set of <span style="text-decoration: underline;">key frames</span>. Key frames are nothing but kinda measurement to decide timeline for you animation speed or length. TL;TR, <a title="GIF Wikipedia" href="http://en.wikipedia.org/wiki/GIF" target="_blank">GIF</a>.
<h2>Problem</h2>
<em>If you had worked on <a title="Adobe Flash - Wikipedia" href="http://en.wikipedia.org/wiki/Adobe_Flash" target="_blank">Adobe Flash</a>, <a title="ToonBoom - Wikipedia" href="http://en.wikipedia.org/wiki/Toon_Boom_Animation" target="_blank">ToonBoom</a> or <a title="Swish Max - Wikiepedia" href="http://en.wikipedia.org/wiki/SWiSH_Max" target="_blank">Swish</a> previously and you are familiar with GIF images then to understand this situation is not big deal.</em>

Recently I stuck where I need to load animated image from first key-frame at each time user refreshes a page (or comes back to a page). As a solution I decided to pass a random parameter in the URL of image - <span class="lang:default decode:true  crayon-inline">some-image.gif?random=22</span>. This image would be defined in <span class="lang:default decode:true  crayon-inline ">.scss</span>  file as below.
<pre class="lang:default decode:true">.animated-image {
    background: url("some-image.gif") 0 0 no-repeat;
}</pre>
<h2>Solution</h2>
As discussed in above section, we will code for <span style="text-decoration: underline;">adding a parameter at the end of URL</span>. It is very easy to get a random value in JavaScript using <span class="lang:default decode:true  crayon-inline">Math.random();</span>  function for <span class="lang:default decode:true  crayon-inline ">&lt;img&gt;</span> tag on a page. But here as image coming through CSS,  we will try to achieve same thing using SASS.
<h3>SASS <small>Input</small></h3>
<pre class="lang:default decode:true">@function stopImageCache($image) {
    $ran = random(100);

    @return $image +"?ran="+ $ran;
}

.animated-image {
    background: url(stopImageCache("some-image.gif")) 0 0 no-repeat;
}</pre>
As you can see in above code, we have defined a SASS function <span class="lang:default decode:true  crayon-inline">stopImageCache()</span> in which we have <span class="lang:default decode:true  crayon-inline">$ran</span> variable to returns a random number between 1 to 100.<i>  </i>When we use <span class="lang:default decode:true  crayon-inline ">random()</span>  function we have to pass largest number <em>(i.e.: 100)</em> as a limit to which value will be generated randomly.

With <span class="lang:default decode:true  crayon-inline">@return $image +"?ran="+ $ran;</span> , we are trying to concatenate <span class="lang:default decode:true  crayon-inline ">$image</span>  and <span class="lang:default decode:true  crayon-inline ">$ran</span> .

<span class="lang:default decode:true crayon-inline">stopImageCache();</span>  function will append at the end of the image. So when we compile the project, the URL in the background property will get the new image URL every time.
<h3>CSS <small>Output</small></h3>
<pre class="lang:default decode:true">.animated-image {
    background: url("some-image.gif?ran=56") 0 0 no-repeat;
}</pre>