---
ID: 4429
post_title: >
  How to Deal with Specificity Issues in
  CSS
author: Kushal Jayswal
post_date: 2015-11-16 16:39:42
post_excerpt: ""
layout: post
permalink: http://teckstack.com/?p=4429
published: false
---
No matter whether you're working on a small or a large-sized web design and development project, you can't overlook the coding part, since it can help adjust your solution according to your specifications.

However, writing code can be a challenging task since even a little typographical error can have a huge negative impact on your end-product. Besides, a lot of other issues crop up during the coding phase that you will need to resolve, especially when working with Cascading Style Sheets. For instance, CSS Specificity is an issue that more likely concerns developers working on bigger projects.

If you want to reduce the time that is spent on finding bugs, it is important for you to understand how your code is interpreted by the browsers. And for that, you require a good understanding of CSS Specificity and how it works. In this post, I'll be helping you explore CSS Specificity and how you can handle the issues associated with it using Preprocessors.
<h2>Understanding CSS Specificity and Its Issue</h2>
Specificity in Cascading Style Sheets is basically a process that helps decide about the CSS rules that need to be applied by web browsers. In fact, CSS Specificity is the main reason because of which cascading style sheet (CSS) rules can't be applied to certain elements. Moreover, it helps in deciding which rule will have priority over other CSS-rules.

If you want an easy way to handle the selector specificity issue, then a viable option is to use the BEM or Block Element Modifier method. BEM is a brilliant front-end toolkit that organizes the structure of cascading style sheet (CSS) and make it easy to understand. This method refrains users from having to reflect a block that comes prepackaged with nested DOM structure. And, the best thing about the BEM method is that the specificity does not change for every selector. Thus, you won't have to worry about issues caused due to overly specific selectors.

In order to keep specificity low, the BEM methodology allows to write classes and not IDs in an HTML document. Now, since you will only have to use classes for your CSS, the specificity of each and every CSS selector will be 0,1,0.

While BEM is an effective technique to handle specificity issues for front-end developers who are involved mainly with HTML based projects, it does not prove a great option for developers who develop content management systems. After all, CMS code editors do not need HTML coding knowledge for laying out the content structure. This is why, you cannot use BEM for all your projects. A viable alternative is to make use of CSS Preprocessors like SASS, LESS and a few others.
<h2>How You Can Deal With CSS Specificity?</h2>
As discussed above, you can deal with the CSS Specificity issues with the help of CSS Preprocessors. Here. I'll be talking about two approaches that use CSS Preprocessors to resolve the specificity problem:
<ol>
	<li>
<h3>Prepend the Existing Selector</h3>
Whenever you face a specificity problem and are forced to make a selector heavier compared to another, then it is recommended that you should prepend your already existing selector with a new class, id, type selectors, etc. You can either prepend the reference selector (&amp;) used in your cascading style Sheets or else use CSS to accomplish the task, using the following code snippet:
<pre>.yellow{</pre>
<pre>    .btn &amp; {</pre>
<pre>        color: yellow;</pre>
<pre>    }</pre>
<pre>}</pre>
</li>
</ol>