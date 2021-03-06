---
ID: 4419
post_title: 6 Signs You Should Invest In Sass
author: Kushal Jayswal
post_date: 2015-02-18 07:59:56
post_excerpt: "Sass is a complement to the CSS. It improves the flow of writing CSS. In other words, it can consider as a plugin or add-on to generate well formatted CSS file with less time and efforts. This article will cover Sass's most used features with examples."
layout: post
permalink: http://teckstack.com/6-sass-features
published: true
---
[Tweet "Writing #CSS is not a big deal. But doing the same, in better way is more important!"]

<a href="http://sass-lang.com/" target="_blank">Sass</a> is a complement to the CSS. It improves the flow of writing CSS. In other words, it can consider as a plugin or add-on to generate well formatted CSS file with less time and efforts.

But before starting with Sass, one should understand that how it can help in a project. Because at the end, CSS is the only output. So if you think, the project is small with a short timeline then definitely avoid it. But once you become familiar with Sass, you would not ignore it for the future project.

Also, <a href="http://teckstack.com/how-to-configure-sass-for-html-projects">configuring Sass</a> isn't a tough job. Even you can go with a one of the tools listed on the site. I use <a href="http://mhs.github.io/scout-app/" target="_blank">Scout</a> for HTML projects and <a href="https://wordpress.org/plugins/wp-scss/" target="_blank">WP-SCSS</a> for WordPress.

This article will focus on some of the most used features of the Sass with easy-to-understand examples.
<h2>First Thing First - Why Sass</h2>
The CSS is an important asset for any front end developer. And hence, it has to be the way he/she wants.  Sass is one of the solution as a pre-processor. It reduces the burden of writing and managing code with some cool features. So, let's jump into it and make our CSS more easier!
<h3>What We Can Do with Sass</h3>
I remember that when I first heard about Sass, I couldn't convince that why to use it when at the end, everything is converted to CSS. But after using it for couple of projects, I really saved big amount of time.

Below are 7 Sass features to understand Sass in better way.
Please feel free to add your <a href="#comments">comment</a>.
<h2>Improved Branding</h2>
Let's assume a project, where we have 5 color schemes that user can configure from the control panel. <strong>Can you imagine the number of lines you need to write to make 5 different color schemes, using CSS?</strong> It will definitely take longer if there is a big hierarchy of selectors. We can count on about 150-200 lines. May be we would consider some properties for all parent and child elements...
<ul>
	<li>Color Schemes</li>
	<li>Background color</li>
	<li>Font color</li>
	<li>Font Family, etc...</li>
</ul>
<strong>And what if client changes his mind to replace the old color with new one</strong>? We have to search the color code and replace all over in files. OMG! How frustrating!
<h3>The Sass Variable</h3>
You have facility to define variables in Sass. It is the same concept as in JavaScript.

<strong>Syntax</strong>
<pre>$variableName: value;</pre>
Variable increases the efficiency. Like in above discussion where we have 5 color options to be configured as a branding options, you can define 5 different variables and assign color properties to each. So in future, if you have to change any color for branding, you can simply change variable's value and it will affect the color for all CSS where the same variables have used.

<strong>Example</strong>
<pre>$primary-color: blue;
$secondary-color: green;
.class1{
    background: $primary-color
}</pre>
<h2>Clubbing and Nesting</h2>
From the start, I wanted to write CSS in modular pattern (yes of course, we can add comment blocks and give proper indentation but yet it's not actually the modular). In JavaScript, we can define functions or create modules. And all its properties and variables have limited scope. In Sass, we can go in a nested way. It's more like <em>clubbing the code into one wrapper</em>.

Many times, we required CSS grouping to give the same CSS properties to multiple elements. But Sass has <span style="text-decoration: underline;">different grouping mechanism</span> and this is the first thing, attracted me to use the Sass! We can build parent-child relationship with the elements, nestedly.

Let's have an example of the Navigation to understand more clearly.

[Tweet "Using #Sass means, thinking of #CSS as a #component."]

The <strong>navigation</strong> is an essential part for any project. Below is a sample CSS to manage the navigation horizontally on a web page.

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
It is always good to separate CSS code in different files or folder to increase the manageability. For big projects, such an approach is helpful to manage the code in better way.
<h3>Sass Partials</h3>
Sass allows to define code in various files. We can make meaningful separations of the code using variables, <code>@extend</code>, <code>@include</code>, etc. in and re-use them across the application.

This is similar to what we do in CSS to import other CSS file. In Sass, we can create <code>.scss</code> files and using <code>@import</code>, call them into the other <code>.scss</code> file. Consider below hierarchical structure of the Sass directory:
<pre>Sass (dir)
|- _variables.scss
|- _functions.scss
|- _header.scss
|- _footer.scss
|- _navigation.scss
|- _content.scss
|- _plugin.scss
|- _overwrite.scss
|- main.scss
CSS (dir)
|- main.css</pre>
Above structure has two directories - Sass and CSS. Sass is dedicated to <code>.scss</code> files, where <code>main.scss</code> file will be importing all the other <code>.scss</code> files with <code>@import</code> definition. And finally <code>main.scss</code> will be compiled to <code>main.css</code> into CSS folder as a final output.

<strong>Using <code>@import</code> for <code>main.scss</code></strong>
<pre>@import 'variables';
@import 'functions';
@import 'header';
@import 'footer';
// and so on...</pre>
You may have noticed <code>.scss</code> files with underscore ("_"). These files will be merged in a one file and won't show up in output directory - CSS. Also, the order of the partials matters. Likewise, variables and functions files, that must be at the top because these files consist of references to be used in other files.
<h2>Extension with Class and Placeholder</h2>
There is a concept in JavaScript, where we can extend the functionality of existing object. This is in object-oriented programming approach known as Inheritance. The same thing we can do in Sass using <code>@extend</code> feature.
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
}
.btn-error{
    @extend .btn;
    background-color: red;
}</pre>
<strong>CSS Output</strong>
<pre>.btn, .btn-success, .btn-error {
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
Everyone knows about functions in JavaScript. Sass also facilitated to write code in that direction. To do so, we have to follow <code>@mixin</code>.

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

// including mixin
body{
    font-size: 16px;
    @include breakpoint(md){
        font-size: 14px;
    }
}</pre>
<strong>CSS Output</strong>
<pre>body {
    font-size: 16px;
}

@media only screen and (max-width: 960) {
    body {
       font-size: 14px;
    }
}</pre>
<h2>Community Aspect</h2>
Sass's <a href="http://sass-lang.com/documentation/file.SASS_REFERENCE.html" target="_blank">official documentation</a> is well maintained. Also, it has large adoption ration, so if you stuck somewhere, don't bother, Google your query and you will be getting it fixed.
<h3>Conclusion</h3>
To sum up, the Sass is just a tool to help in regular projects and it helps to reduce some burden of front end developer. But counting on Sass features, big projects' CSS can be managed and written in very well manner. Also, the <a href="http://teckstack.com/how-to-configure-sass-for-html-projects">configuration for Sass</a> is not that tough. <a href="https://www.liferay.com/" target="_blank">Liferay</a> like CMS has Sass built-in. It has big adoption ratio and larger community as a helping hand. Moreover, if you have any question, feel free to <a href="#comments">comment below</a>.
<h4>External Resources</h4>
<ul>
	<li><a href="http://sassmeister" target="_blank">Sass Meister</a> - An editor that instantly compiles Sass to CSS, so you can see the output with no-time</li>
	<li><a href="http://thesassway.com/" target="_blank">The Sass Way</a> - Tips and Easy to use Sass snippets helpful in real projects</li>
	<li><a href="http://stackoverflow.com/questions/tagged/sass" target="_blank">Stack Overflow</a> - Q&amp;A Community</li>
</ul>