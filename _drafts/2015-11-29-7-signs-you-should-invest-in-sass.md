---
ID: 4419
post_title: 7 Signs You Should Invest In Sass
author: Kushal Jayswal
post_date: 2015-11-29 06:22:06
post_excerpt: ""
layout: post
permalink: http://teckstack.com/?p=4419
published: false
---
<blockquote>Writing CSS is an easy task. But doing the same in proper manner, which can be understood by all developers in a team that is more important.</blockquote>
Before you start a project with <a href="http://sass-lang.com/" target="_blank">Sass</a>, you should understand that how it can help for CSS authoring. Sass stands for "Syntactically Awesome Style Sheets" and people using Sass won't disagree on the statement. Today major projects demand for media query and branding options. From the years of experience, I found Sass as one of the best solution as CSS enhancer.

For big projects, writing pure CSS becomes hectik sometime (and especially when, you have numbers of developers working on the same project) and here in, pre-processors comes in a picture. <a href="http://teckstack.com/how-to-configure-sass-for-html-projects">Configuring Sass</a> isn't a tough job. If you don't want to configure manually then you can use tools listed on the site. I use <a href="http://mhs.github.io/scout-app/" target="_blank">Scout</a> for HTML projects and <a href="https://wordpress.org/plugins/wp-scss/" target="_blank">WP-SCSS</a> for WordPress. Liferay has `@compass` built-in, so you can directly start writing Sass with importing of compass at the top of the `.scss` file.

This article will focus on some of the most used features of the Sass with some easy-to-understand examples.
<h2>First Thing First - Why Sass</h2>
The CSS is an important asset for a front end developer. And hence, it has to be the way he wanted and pre-processors can be the mediator to achieve this goal. Sass stands in a popular category as a pre-processor. It can reduce the burden of writing and managing stuffs with some cool techniques with steps of simple configuration. It comes with set of meaningful features. So, let's jump into it and make our life more easier!
<h3>What We Can Do with Sass</h3>
I remember that when I first heard about the pre-processor, I couldn't convince that why should we have it because at the end, everything being converted to CSS. But, believe me, after getting understood Sass features, I would highly recommend it.

Let's start looking into Sass's most popular features.
If you have any confusion, kindly add your <a href="/#comments">comment</a> below. I would try to get over it soon.
<ul>
	<li>Improved Branding</li>
	<li>Clubbing &amp; Nesting</li>
	<li>Partials &amp; Importing</li>
	<li>Extending</li>
	<li>Including</li>
	<li>Functioning</li>
	<li>Community Aspect</li>
</ul>
<h2>Improved Branding</h2>
Giving default branding options, which can be configured from control panel/backed of the site, is one of the important thing for any large project. In simple term "Branding" means color options, which admin/user can change as per his preferences. This configurable options can be...
<ul>
	<li>Color Schemes</li>
	<li>Background color</li>
	<li>Font color</li>
	<li>Font Family, etc...</li>
</ul>
Using CSS all these we can do but that would take more efforts and might we have to be dependent on core developers for the logic. And if we have 4-5 different color options then you can imagine the number of lines in CSS for color schemes only. On the other hand, if client changes his mind to change the color then we have to search the color code and replace all over. OMG! How frustrating!
<h3>Sass Variable</h3>
You have facility to define variables in Sass. It is the same concept as in JavaScript.

<strong>Syntax</strong>:
<pre>$variableName: value;</pre>
Variable increases the efficiency. Like in above discussion where we have 4-5 color options to be configured as a branding options, you can define 5 different variables and assign color properties to each. So in future, if you have to change any color for branding, you can simply change variable's value and it will affect the color for all CSS where the same variable has been used.

<strong>Example</strong>:
<pre>$primary-color: blue;
$secondary-color: green;
// etc</pre>
<h2>Clubbing &amp; Nesting</h2>
From the start, I wanted CSS be written in modular way (yes of course, we can add comment blocks and give proper indentation but yet it's not actually the modular). What mean by modular? Well, in JavaScript, we can define functions or create modules and all its respectives, like properties or variables are limited to its scope. This way we can define our code in more readable form.

Many times we required CSS grouping concept where to give the same CSS properties to multiple elements. But Sass has different grouping mechanism and this is the first thing, attracted me to use Sass! Yes, I started using Sass because it allows nesting. We can build parent-child relationship with the elements.

Let's have an example of the Navigation component/element to understand the nesting.
<blockquote>Using Sass means, thinking of CSS as a component.</blockquote>
Navigation is an essential component for any project. Below is sample CSS to manage the navigation horizontally on a web page.

**Sample CSS for Navigation**
```
nav{ background: #eee; }
nav li{ float: left; }
nav li a{ display: block; padding: 5px 10px; }
```
**Sass**
```
nav{
background: #eee;
li{
float: left;;
a{
display: block;
padding: 5px 10px;
}
}
}
```
As you can see in above Sass snippet, the code is more readable and we have actually define `nav` as an component. `li` tag and `a` tag can be considered as a child element to `nav`.