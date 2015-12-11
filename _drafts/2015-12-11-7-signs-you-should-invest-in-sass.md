---
ID: 4419
post_title: 7 Signs You Should Invest In Sass
author: Kushal Jayswal
post_date: 2015-12-11 14:13:16
post_excerpt: ""
layout: post
permalink: http://teckstack.com/?p=4419
published: false
---
<blockquote>[Tweet "Writing #CSS is not a big deal. But doing the same, in well manner is more important!"]

<footer><a href="https://twitter.com/manishweb2009" target="_blank">Manish Sharma</a>
<cite title="If I Use (http://ifiuse.com)"><em>Front end developer</em></cite></footer></blockquote>
<img class="alignright wp-image-4482 size-full" src="http://teckstack.com/tsdir/wp-content/uploads/2015/12/sass-logo.png" alt="Sass Logo" width="250" height="250" /><a href="http://sass-lang.com/" target="_blank">Sass</a> is a complement to the CSS. It improves the flow of writing CSS. In other words, it can be considered as a plugin or add-on to generate well formatted CSS file with less time and efforts.

But before starting with Sass, one should understand that how it can help in a project. Because at the end, CSS is the only output. So if you think, the project is small with a short timeline then definitely avoid it. But mark my words, once you adopted Sass, you won't be off from it.

Also, <a href="http://teckstack.com/how-to-configure-sass-for-html-projects">configuring Sass</a> isn't a tough job. Even you can go with a one of the tools listed on the site. I use <a href="http://mhs.github.io/scout-app/" target="_blank">Scout</a> for HTML projects and <a href="https://wordpress.org/plugins/wp-scss/" target="_blank">WP-SCSS</a> for WordPress.

This article will focus on some of the most used features of the Sass with easy-to-understand examples.
<h2>First Thing First - Why Sass</h2>
The CSS is an important asset for any front end developer. And hence, it has to be the way he/she wanted to be.  Sass is one of the solution as a pre-processor. Sass reduces the burden of writing and managing code with some cool techniques. It has set of meaningful features. So, let's jump into it and make our life more easier!
<h3>What We Can Do with Sass</h3>
I remember that when I first heard about Sass, I couldn't convince that why to use it when at the end, everything being converted to CSS. But after getting over its features, I would highly recommend it.

Let's start looking into Sass's most popular features.
If you have any confusion, please add your <a href="#comments">comment</a> below.
<ol>
	<li>Improved Branding</li>
	<li>Clubbing and Nesting</li>
	<li>Partials and Importing</li>
	<li>Extending</li>
	<li>Including</li>
	<li>Functioning</li>
	<li>Community Aspect</li>
</ol>
<h2>Improved Branding</h2>
Let's assume a project where we have 5 color scheme options and that user can configure from the backend. This is the traditional thing for any reputed project. But if we think writing CSS for all the 5 then you can imagine number of lines needs to be written. May be we would consider some properties for all parent and child elements...
<ul>
	<li>Color Schemes</li>
	<li>Background color</li>
	<li>Font color</li>
	<li>Font Family, etc...</li>
</ul>
&nbsp;

<strong>And what if client changes his mind to replace the old color with new one</strong>? We have to search the color code and replace all over in files. OMG! How frustrating!
<h3>The Sass Variable</h3>
You have facility to define variables in Sass. It is the same concept as in JavaScript.

<strong>Syntax</strong>
<pre>$variableName: value;</pre>
Variable increases the efficiency. Like in above discussion where we have 5 color options to be configured as a branding options, you can define 5 different variables and assign color properties to each. So in future, if you have to change any color for branding, you can simply change variable's value and it will affect the color for all CSS where the same variable has been used.

<strong>Example</strong>
<pre>$primary-color: blue;
$secondary-color: green;
.class1{
    background: $primary-color
}</pre>
<h2>Clubbing and Nesting</h2>
From the start, I wanted to write CSS in modular pattern (yes of course, we can add comment blocks and give proper indentation but yet it's not actually the modular). In JavaScript, we can define functions or create modules. And all its properties and variables have limited scope. In Sass, we can go in a nested way. It's more like clubbing the code into one wrapper.

Many times we required CSS grouping to give the same CSS properties to multiple elements. But Sass has different grouping mechanism and this is the first thing, attracted me to use Sass! Yes, I started using Sass because it allows nesting flow to define CSS. We can build parent-child relationship with the elements.

Let's have an example of the Navigation component / element to understand the nesting.

[Tweet "Using #Sass means, thinking of #CSS as a #component."]

Navigation is an essential component for any project. Below is a sample CSS to manage the navigation horizontally on a web page.

<strong>Sample CSS for Navigation</strong>
<pre>nav{ background: #eee; }
nav li{ float: left; }
nav li a{ display: block; padding: 5px 10px; }</pre>
<strong>Sass</strong>
<pre>nav{
   background: #eee;
   li{
       float: left;;
       a{
           display: block;
           padding: 5px 10px;
       }
   }
}</pre>
As you can see in above Sass snippet, the code is more readable and we have actually defined <code>&lt;nav&gt;</code> as a component while <code>&lt;li&gt;</code> and <code>&lt;a&gt;</code> tags are children elements to <code>&lt;nav&gt;</code>.
<h2>Partials and Importing</h2>
It is always good to separate CSS code in different files or folder to increase the manageability. Large projects may need this approach based on features of a project. This kind of separation makes sense for developers working on the same theme at a time.
<h3>Sass Partials</h3>
Sass allows to define code in various files. We can define codes using variables, @extend, @include, etc. in any file to re-use across the application.

This is similar to what we do in CSS to import a file. We can create <code>.scss</code> files and using <code>@import</code> call them into another <code>.scss</code> file. Consider below hierarchical structure of the Sass directory:
<pre>Sass (dir)
|_ _variables.scss
|_ _functions.scss
|_ _header.scss
|_ _footer.scss
|_ _navigation.scss
|_ _content.scss
|_ _plugin.scss
|_ _overwrite.scss
|_ main.scss
CSS (dir)
|_ main.css</pre>
Above structure has two directories - Sass and CSS. Sass is dedicated to <code>.scss</code> files, where <code>main.scss</code> file will be importing all the other <code>.scss</code> files with <code>@import</code> definition. And finally <code>main.scss</code> will be compiled to <code>main.css</code> into CSS folder as a final output.

<strong>Using <code>@import</code> for <code>main.scss</code></strong>
<pre>@import 'variables';
@import 'functions';
@import 'header';
@import 'footer';
// etc</pre>
You may have noticed <code>.scss</code> files with underscore ("_"). These files will be merged in a one file and won't show up in output directory. Also, the order of the partials matters. Likewise, variables and functions files, that must be at the top because these files consist of definitions of re-usable code.
<h2>Inheritance or @extend</h2>
There is a concept in JavaScript, where we can extend the functionality of existing object. This is in object-oriented programming approach know as Inheritance. The same thing we can do in Sass, using <code>@extend</code> feature.
<pre>@extend .some-class<span class="token punctuation">;</span></pre>
<blockquote>[Tweet "Extends do not allow customization, but they produce very efficient CSS"]

<footer><a href="http://stackoverflow.com/questions/18008700/using-include-vs-extend-in-sass?answertab=active#tab-top" target="_blank">Andrey Mikhaylov</a>
Front end developer at Firecracker.me</footer></blockquote>
Let's have an example of buttons by assuming 3 variants with colors. So, here we have to define a generic class for <code>.btn</code> and then you can change properties as per the preference or requirement.

<strong>Sass</strong>
<pre>.btn{
    padding: 15px;
    color: #fff;
}
.btn-success{
    @extend .btn;
    background-color: green;
}</pre>
<strong>CSS Output</strong>
<pre>.btn, .btn-success {
    padding: 15px;
    color: #fff;
}
.btn-success {
    background-color: green;
}
.btn-error {
    background-color: red;
}</pre>
Also, instead of <code>.btn</code> class, we can define through Sass placeholder selector:
<pre>%btn{
    padding: 15px;
    color: #fff;
}
.btn-success{
    @extend %btn;
    background-color: green;
}</pre>
<h2>Function and Include</h2>
Everyone knows about functions in JavaScript. Sass also facilitated to write code in that direction. To do so we have to follow syntax using <code>@mixin</code> keyword.

<strong>Syntax</strong>
<pre>@mixin mixin_name(parameter){
    // code
}
.class-name{
    @include mixin_name(parameter){ // code }
}</pre>
Below is an example for <strong>media query <code>@mixin</code></strong>
<pre>@mixin breakpoint($media){
    @if $media == xs {
        @media only screen and (max-width: 480) { @content; }
    }
    @else if $media == sm {
        @media only screen and (max-width: 768) { @content; }
    }
    @else if $media == md {
        @media only screen and (max-width: 960) { @content; }
    }
    @else if $media == lg {
        @media only screen and (max-width: 1170) { @content; }
    }
}

// including
body{
    font-size: 16px;
    @include breakpoint(md){
        font-size: 14px;
    }
}</pre>
<strong>CSS Output</strong>
<pre>body {
    font-size: 16px;
}</pre>
<pre>@media only screen and (max-width: 960) {
    body {
       font-size: 14px;
    }
}</pre>
asdasd