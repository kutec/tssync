---
ID: 3217
post_title: Creating Color Palette with SASS
author: Kushal Jayswal
post_date: 2015-01-12 13:17:02
post_excerpt: ""
layout: post
permalink: >
  http://teckstack.com/creating-color-palette-sass
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
views:
  - "5356"
dsq_thread_id:
  - "3456595077"
mentions:
  - 'a:0:{}'
mentioned_by:
  - "3522"
post_views_count:
  - "3"
ac_is_copyprotect:
  - "1"
ac_is_advanced_tracking:
  - "1"
ac_postid:
  - 5npIFvnQKNq.text
ac_is_process:
  - "1"
ac_embedid:
  - 4doKGrUNOcU
vortex_system_likes:
  - "0"
vortex_system_dislikes:
  - "0"
---
<blockquote>Maintaining multiple color themes with a project is tedious task for a developer. SASS is popular CSS pre-processor. It works with simple motto - "reducing efforts with improved CSS".</blockquote>

While writing <a title="Creating Color Palette with SASS" href="http://teckstack.com/creating-color-palette-sass">this post</a>, I am targeting people who are familiar with CSS and have little knowledge about any CSS pre-processors like <a title="SASS" href="http://sass-lang.com/" target="_blank">SASS</a>, <a title="LESS" href="http://lesscss.org/" target="_blank">LESS</a> or <a title="Stylus" href="http://learnboost.github.io/stylus/" target="_blank">Stylus</a>.

<h2>About SASS</h2>

<strong>Syntactically Awesome Style Sheets</strong> also called <span style="text-decoration: underline">SASS</span> in short. SASS is popular CSS pre-processor, helps to drive CSS magically with improved code. You can write in modular pattern. It allows to define variables (as in JS), reduce redundant classes with @extend, declaring a JS like functions with @mixin and many more.

<strong>SASS Example</strong>

<pre class="lang:default decode:true">#nav{
  background: #fff;
  padding: 10px;
  li{
    float: left; 
    margin-right: 10px;
    &amp;:last-child{
      margin-right: 0;
    }
    a{
      padding: 5px;
      &amp;:hover, 
      &amp;.active{
        background: #666;
    }
  }
}</pre>

<strong>CSS Output</strong>

<pre class="lang:default decode:true">#nav{ 
  background: #fff; 
}
#nav li{ 
  float: left;
  margin-right: 10px;
}
#nav li:last-child{
  margin-right: 0;
}
#nav li a{ 
  padding: 5px; 
}
#nav li a:hover, 
#nav li a.active{ 
  background: #666; 
}</pre>

Today we will focus on "Creating Color Palette with SASS".

<h2>Mindset</h2>

Let's assume a requirement where client wants <span style="text-decoration: underline">5 different color scheme options</span> to the end-user.

Let me clear on 5 different color schemes <em>as a theme</em> - that means <strong>theme-a</strong>, <strong>theme-b</strong>,<strong> theme-c</strong> and so on. Each theme would be having 4-5 different colors as a branding options. Let's say - <em>neutral, primary, secondary, territory and quaternary</em>.

<img class="alignnone wp-image-3284 size-full" src="http://teckstack.com/tsdir/wp-content/uploads/2015/01/color-palette.png" alt="Color Palette" width="1121" height="239" />

Below I tried to explain HTML, CSS and SASS code for a single color scheme and it is having about 30 lines of CSS. So if requirement demands for 5 different color schemes then it would take 150 lines of CSS code approximately.

Below code is having "theme-a" as a theme name. On basis of theme name, the CSS has been coded for the structure with sub-classes (i.e.:  neutral-b, primary-bg, etc.). <span class="lang:default decode:true  crayon-inline ">.box</span>  is a helper class only to give physical visibility to DIVs.

<strong>HTML</strong>

<pre class="height:300 lang:default mark:1 decode:true">&lt;div class="theme-a"&gt;
    &lt;div class="box neutral-bg"&gt;Neutral&lt;/div&gt;
    &lt;div class="box primary-bg"&gt;Primary&lt;/div&gt;
    &lt;div class="box secondary-bg"&gt;Secondary&lt;/div&gt;
    &lt;div class="box territory-bg"&gt;Territory&lt;/div&gt;
    &lt;div class="box quaternary-bg"&gt;Quaternary&lt;/div&gt;
&lt;/div&gt;</pre>

<strong>CSS</strong>

<pre class="lang:default decode:true">.theme-a .nuetral-bg {
  background: rgba(0, 255, 153, 0.5);
}
.theme-a .nuetral-bg:hover {
  background: rgba(0, 255, 153, 0.75);
}
.theme-a .primary-bg {
  background: rgba(255, 140, 0, 0.5);
}
.theme-a .primary-bg:hover {
  background: rgba(255, 140, 0, 0.75);
}
.theme-a .secondary-bg {
  background: rgba(255, 0, 38, 0.5);
}
.theme-a .secondary-bg:hover {
  background: rgba(255, 0, 38, 0.75);
}
.theme-a .teritory-bg {
  background: rgba(128, 255, 0, 0.5);
}
.theme-a .teritory-bg:hover {
  background: rgba(128, 255, 0, 0.75);
}
.theme-a .quaternary-bg {
  background: rgba(183, 0, 255, 0.75);
}
.theme-a .quaternary-bg:hover {
  background: #b700ff;
}</pre>

<strong>SASS</strong>

<pre class="lang:default decode:true">/* declaring variables */
$neutralColor: rgba(0, 255, 153, 0.5);
$neutralColorHover: rgba(0, 255, 153, 0.75);

$primaryColor: rgba(255, 140, 0, 0.5);
$primaryColorHover: rgba(255, 140, 0, 0.75);

$secondaryColor: rgba(255, 0, 38, 0.5);
$secondaryColorHover: rgba(255, 0, 38, 0.75);

$teritoryColor: rgba(128, 255, 0, 0.5);
$teritoryColorHover: rgba(128, 255, 0, 0.75);

$quaternaryColor: rgba(183, 0, 255, 0.75);
$quaternaryColorHover: rgba(183, 0, 255, 1);


.theme-a{
  .neutral-bg {
    background: $neutralColor;
    &amp;:hover{
      background: $neutralColorHover;
    }
  }
  .primary-bg {
    background: $primaryColor;
    &amp;:hover {
      background: $primaryColorHover;
    }
  }
  .secondary-bg {
    background: $secondaryColor;
    &amp;:hover {
      background: $secondaryColorHover;
    }
  }
  .teritory-bg {
    background: $teritoryColor;
    &amp;:hover {
      background: $teritoryColorHover;
    }
  }
  .quaternary-bg {
    background: $quaternaryColor;
    &amp;:hover {
      background: $quaternaryColorHover;
    }
  }
}</pre>

After all processes one question is obvious to ask our self - <em>Is there any way we can make it simpler for developer</em>?

<strong>Well! I am not sure about <span style="text-decoration: underline">specific color codes</span> but yes I tried with logical way and that works for me <span style="text-decoration: underline">at some level*</span>.</strong>

<h2>Declaring MIXIN</h2>

For non-technical people reading this article - <strong>@mixin</strong> is one of the feature of SASS allows to declare logical code which is almost similar to a function in JavaScript.

I am declaring @mixin with <span style="text-decoration: underline">two arguments</span>:

<ol>
    <li><span class="lang:default decode:true  crayon-inline">$name</span> : Taking theme name</li>
    <li><span class="lang:default decode:true  crayon-inline">$color</span> : Taking color code as an input</li>
</ol>

Currently I am declaring @mixin for a background color but if you need, you can do it for foreground color (font-color) as well.

<pre class="lang:default decode:true">@mixin theme($name, $color) {}
</pre>

We can call @mixin using @include method of SASS. <em>It may be coded more dynamically with help of core developer.</em>

<h2>Calling with INCLUDE</h2>

@include is another feature of SASS allows to call @mixin. Below I am calling <span class="lang:default decode:true  crayon-inline">@mixin theme</span> in SASS file where <strong>theme-a</strong> &amp; <strong>#FF8C00</strong> are <em>theme name</em> and <em>color code</em> accordingly.

<pre class="lang:default decode:true">@include theme(theme-a, #FF8C00);</pre>

As you can see in above code there are only one color passed and there is no specification for sub classes too. So next thing we need a <em>logic to generate 5 different color variations with appropriate class names</em>.

<h2>Manipulating with MIXIN Arguements</h2>

We have been already declared color variables with <span class="lang:default decode:true  crayon-inline">$</span> symbol. Now we have to play with colors and that is possible using <a title="Color Manipulation Functions in SASS" href="http://sass-lang.com/documentation/Sass/Script/Functions.html" target="_blank">color manipulation option in SASS</a>.

<pre class="lang:default decode:true" title="SASS - Generating Color Variations with $color Arguement">@mixin theme($name, $color) {
  $neutralColor: rgba(adjust-hue($color, 123), .5);
  $neutralColorHover: rgba(adjust-hue($color, 123), .75);

  $primaryColor: rgba(adjust-hue($color, 0), .5);
  $primaryColorHover: rgba(adjust-hue($color, 0), .75);

  $secondaryColor: rgba(adjust-hue($color, 678), .5);
  $secondaryColorHover: rgba(adjust-hue($color, 678), .75);

  $teritoryColor: rgba(adjust-hue($color, 777), .5);
  $teritoryColorHover: rgba(adjust-hue($color, 777), .75);

  $quaternaryColor: rgba(adjust-hue($color, 250), .75);
  $quaternaryColorHover: rgba(adjust-hue($color, 250), 1);
}</pre>

Above code will take <span class="lang:default decode:true  crayon-inline">$color</span>  as a <span class="lang:default decode:true  crayon-inline ">$primaryColor</span>  and then with <a title="Color Manipulators" href="http://sass-lang.com/documentation/Sass/Script/Functions.html" target="_blank">color manipulators</a> like <strong>rgba</strong> and <strong>adjust-hue </strong>help to generate other variations. But this way we can generate only random colors and cannot get awesome color combination as on <a title="Adobe Kuler" href="https://color.adobe.com/" target="_blank">Adobe Kuler</a>. Experts can comment much better logic and help the community.

<h3>Creating Sub Classes</h3>

<pre class="lang:default decode:true">.#{$name} {

    /* nuetral BG */
    .neutral-bg {
      background: $neutralColor;
      &amp;:hover{
        background: $neutralColorHover;
      }
    }

    /* BASE COLOR - primary BG */
    .primary-bg {
      background: $primaryColor;
      &amp;:hover{
        background: $primaryColorHover;
      }
    }

    /* secondary BG */
    .secondary-bg {
      background: $secondaryColor;
      &amp;:hover{
        background: $secondaryColorHover;
      }
    }

    /* teritory BG */
    .teritory-bg {
      background: $teritoryColor;
      &amp;:hover{
        background: $teritoryColorHover;
      }
    }

    /* quaternary BG */
    .quaternary-bg {
      background: $quaternaryColor;
      &amp;:hover{
        background: $quaternaryColorHover;
      }
    }</pre>

<h2>SASS Complete Code</h2>

<pre class="lang:default mark:72 decode:true" title="Complete Code - Creating Color Palette">@mixin theme($name, $color) {
  
  /* declaring color variables */
  
  $neutralColor: rgba(adjust-hue($color, 123), .5);
  $neutralColorHover: rgba(adjust-hue($color, 123), .75);
  
  $primaryColor: rgba(adjust-hue($color, 0), .5);
  $primaryColorHover: rgba(adjust-hue($color, 0), .75);

  $secondaryColor: rgba(adjust-hue($color, 678), .5);
  $secondaryColorHover: rgba(adjust-hue($color, 678), .75);

  $teritoryColor: rgba(adjust-hue($color, 777), .5);
  $teritoryColorHover: rgba(adjust-hue($color, 777), .75);

  $quaternaryColor: rgba(adjust-hue($color, 250), .75);
  $quaternaryColorHover: rgba(adjust-hue($color, 250), 1);
  
  
  /*  sub-classes 
      $name = theme name with @include
  */
  .#{$name} {

    /* BASE COLOR - nuetral BG */
    .neutral-bg {
      background: $neutralColor;
      &amp;:hover{
        background: $neutralColorHover;
      }
    }

    /* primary BG */
    .primary-bg {
      background: $primaryColor;
      &amp;:hover{
        background: $primaryColorHover;
      }
    }

    /* secondary BG */
    .secondary-bg {
      background: $secondaryColor;
      &amp;:hover{
        background: $secondaryColorHover;
      }
    }

    /* teritory BG */
    .teritory-bg {
      background: $teritoryColor;
      &amp;:hover{
        background: $teritoryColorHover;
      }
    }

    /* quaternary BG */
    .quaternary-bg {
      background: $quaternaryColor;
      &amp;:hover{
        background: $quaternaryColorHover;
      }
    }
  }
}

/*  calling @mixin using @include 
    where "theme-a" = theme name
    and   "#FF8C00" = color code
*/
@include theme(theme-a, #FF8C00);

/* helper class */
.box{ 
  width: 200px; 
  height: 200px; 
  margin: 10px; 
  float: left; 
}</pre>

<h2><a title="See In Action" href="http://codepen.io/kutec/pen/OPWBrO" target="_blank">Demo</a></h2>

<h2>Conclusion</h2>

This article will give you hint to create something awesome. Though this doesn't help to generate specific colors but at some level it will boost up your view to write more code with less efforts.

I am eagerly looking for your reaction in below <a title="Show Your Reaction :)" href="#disqus_thread">comment section</a>.