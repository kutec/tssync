---
ID: 4419
post_title: 7 Signs You Should Invest In Sass
author: Kushal Jayswal
post_date: 2015-11-28 14:58:32
post_excerpt: ""
layout: post
permalink: http://teckstack.com/?p=4419
published: false
---
<blockquote>Writing CSS is an easy task. But doing the same in proper manner, which can be understood by all developers in a team that is more important.</blockquote>
Before you start a project with <a href="http://sass-lang.com/" target="_blank">Sass</a>, you should understand that how it can help for CSS authoring. Sass stands for "Syntactically Awesome Style Sheets" and people using Sass won't disagree on the statement. Today major projects demand for media query and branding options. From the experience, I found Sass as one of the best solution. Let's see how...

For big projects, writing pure CSS to manage everything becomes hectik sometime (and especially when you have numbers of developers working on the same project) and here in, pre-processors comes in a picture. I am personally big fan of Sass. [Configuring Sass] is a tough job. If you don't want to configure manually then you can use tools listed on the site. I use [Skout] for HTML projects and [WP-SCSS] for WordPress. Liferay has `@compass` built-in, so you can directly start writing Sass with importing of compass at the top of the `.scss` file.

This article will focus on some of the most used features of the Sass with some easy-to-understand examples.

### First Thing First - Why Sass
The CSS is an important asset for a front end developer. And hence, It has to be the way he want and pre-processors can be the mediator to achieve this goal. The adoption ratio of pre-processor is too high. Developers used to it now. Sass stands in a popular category. It can reduce the burden of writing and managing stuffs with some cool techniques. It comes with set of meaningful features. So, let's jump into it!

### What I Can Do with Sass
I remember that when I first heard about the pre-processor, I couldn't convince that why should we use Sass and how it can save lot of time and efforts. Let's elaborate with the list below.

If you have any question, kindly add your comment below. I would try to get over it soon.

- Improved Branding
- Clubbing &amp; Nesting
- Partials &amp; Importing
- Extending
- Including
- Functioning
- Community Aspect

## Improved Branding
Giving default branding options, which can be configurable from control panel or backed of the site, is one of the important thing for any large project.

In simple term "Branding" means color options. Admin/user can change site's background and color dynamically, which has been define through CSS. But if you have 4-5 different color options then you can imagine the number of lines in CSS. And on the other hand, if client changes his mind to change the color then you know how frustrating it is. We have to search the color code and replace all over. OMG!

### Sass Variable
You have facility to define variables in Sass. It is the same concept as in JavaScript.

Syntax:
```
$variableName: value;
```
Variable increases the efficiency. Like for above example where you have 4-5 color options to be configured as a branding options, you can define 5 different variables and assign color properties to each. So in future if you have to change any color for branding, you can simply change variable's value and it will affect the color for all CSS where the same variable has been used.

Example:
```
$primary-color: blue;
$secondary-color: green;
// etc
```

## Clubbing &amp; Nesting
From the start, I wanted CSS be written in modular way (yes of course we can add comment blocks and give proper indentation but yet it's not actually modular). What I mean by modular? Well, in JavaScript we can define functions or create modules and all its respectives like properties or variables are limited to its scope.

CSS has grouping concept where, we can give the same CSS properties to multiple elements. But Sass has different grouping mechanism and this is the first thing attracted me to use Sass! Yes, I started using Sass because it allows nesting. We can build parent-child relationship with the elements using Sass.

Let's have an example of the Navigation component/element to understand the nesting.

&gt; Using Sass means, thinking of CSS as a component.

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