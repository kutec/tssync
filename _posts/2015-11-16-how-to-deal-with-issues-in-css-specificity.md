---
ID: 4429
post_title: >
  How to Deal with Issues in CSS
  Specificity
author: Guest Author
post_date: 2015-11-16 18:17:59
post_excerpt: ""
layout: post
permalink: >
  http://teckstack.com/how-to-deal-with-issues-in-css-specificity
published: true
---
No matter whether you're working on a small or a large-sized web design and development project, you can't overlook the coding part, since it can help adjust your solution according to your specifications.

However, writing code can be a challenging task since even a little typographical error can have a huge negative impact on your end-product. Besides, a lot of other issues crop up during the coding phase that you will need to resolve, especially when working with Cascading Style Sheets. For instance, CSS Specificity is an issue that more likely concerns developers working on bigger projects.

If you want to reduce the time that is spent on finding bugs, it is important for you to understand how your code is interpreted by the browsers. And for that, you require a good understanding of CSS Specificity and how it works. In this post, I'll be helping you explore CSS Specificity and how you can handle the issues associated with it using Preprocessors.
<h2>Understanding CSS Specificity and Its Issue</h2>
Specificity in Cascading Style Sheets is basically a process that helps decide about the CSS rules that need to be applied by web browsers. In fact, CSS Specificity is the main reason because of which cascading style sheet (CSS) rules can't be applied to certain elements. Moreover, it helps in deciding which rule will have priority over other CSS rules.

If you want an easy way to handle the selector specificity issue, then a viable option is to use the <strong>BEM</strong> or <strong>Block Element Modifier</strong> method. BEM is a brilliant front-end toolkit that organizes the structure of cascading style sheet (CSS) and make it easy to understand. This method refrains users from having to reflect a block that comes prepackaged with nested DOM structure. And, the best thing about the BEM method is that the specificity does not change for every selector. Thus, you won't have to worry about issues caused due to overly specific selectors.

In order to keep specificity low, the BEM methodology allows to write classes and not IDs in an HTML document. Now, since you will only have to use classes for your CSS, the specificity of each and every CSS selector will be 0,1,0.

While BEM is an effective technique to handle specificity issues for front-end developers who are involved mainly with HTML based projects, it does not prove a great option for developers who develop content management systems. After all, CMS code editors do not need HTML coding knowledge for laying out the content structure. This is why, you cannot use BEM for all your projects. A viable alternative is to make use of CSS Preprocessors like SASS, LESS and a few others.
<h2>How You Can Deal With CSS Specificity</h2>
As discussed above, you can deal with the CSS Specificity issues with the help of CSS Preprocessors. Here. I'll be talking about two approaches that use CSS Preprocessors to resolve the specificity problem:
<ol>
	<li>
<h3>Prepend the Existing Selector</h3>
Whenever you face a specificity problem and are forced to make a selector heavier compared to another, then it is recommended that you should prepend your already existing selector with a new class, id, type selectors, etc. You can either prepend the reference selector <code>&amp;</code> used in your cascading style Sheets or else use CSS to accomplish the task, using the following code snippet:
<pre>.yellow{
    .btn &amp; {
        color: yellow;
    }
}</pre>
This will produce the following output:
<pre>.btn .yellow {
    color: yellow;
}</pre>
Probably, you might wish to prepend the selector with the help of an html or a body tag. However, a better option is to use something more specific available on your pages like the <code>#wrapper</code>, <code>.page</code>, etc. Also, you can make your selector ready to adapt to any changes that will take place in the future. For this purpose, you can make use of <a href="http://teckstack.com/tag/sass">Sass</a> that helps add the prepending selector in a variable as follows:
<pre>$PrependVar1: "header &amp;";
$PrependVar2: "footer &amp;";

.block {
    #{$PrependVar1} {
        width: 55%;
    }
    #{$PrependVar1} {
        width: 37%;
    }
}
</pre>
The above code will produce the following output:
<pre>header .block {
    width: 55%;
}

footer .block {
    width: 37%;
}</pre>
</li>
	<li>
<h3>Use a Self-chained Selector</h3>
Undoubtedly, prepending a selector proves a useful approach, but isn't a good scalable solution. A better alternative is to make use of CSS’s feature that increases the specificity using self-chained selectors.

The self-chained selectors also work well with ids, classes, etc. except for type selectors. When using classes for styling your CSS, using a self-chained selector provides a scalable way to override any specific selector.

Thanks to the parent reference selector, you can chain the same selector to itself many different times, as you can see in the code below:
<pre>.classSelector {
    &amp;#{&amp;} {
       width: 55%;
    }
    &amp;#{&amp;}#{&amp;} {
        width: 37%;
    }
}

.classSelector.classSelector {
    width: 55%;
}

.classSelector.classSelector.classSelector {
    width: 55%;
}</pre>
In case, you find the above code confusing, you can create a <strong>mixin</strong> to increase the specificity along with Sass 3.4, as follows:
<pre>@mixin block($number: 1) {
    $selector: &amp;;

    @if $number &gt; 1 {
        @for $i from 1 to $number {
            $selector: $selector + &amp;;
        }

        @at-root #{$selector} {
            @content;
        }
    }
    @else {
        @content;
    }
}

.selector {
    @include block(2) {
        width: 55%;
    }

    @include block(3) {
        width: 37%;
    }
}</pre>
The resulting CSS will look something like:
<pre>.selector. selector {
    width: 55%;
}

.selector.selector.selector {
    width: 37%;
}</pre>
</li>
</ol>
You can also use LESS and Stylus CSS Pre Processors for self-chaining.

Self-chaining will help in increasing the specificity of any selector and will help in making it infinitely scalable.
<h3>Final Thought</h3>
The CSS Preprocessors are getting evolved, however, developers still don't pay much attention to using them in the correct way. The biggest benefit of CSS Preprocessors is that they can help you tackle with specificity problems that you might encounter when working on your style sheets.
<h4>Resources</h4>
<ul>
	<li><a href="http://www.smashingmagazine.com/2007/07/css-specificity-things-you-should-know/" target="_blank">CSS Specificity: Things You Should Know - Smashing Magazine</a></li>
	<li><a href="https://developer.mozilla.org/en-US/docs/Web/CSS/Specificity" target="_blank">MDN - Specificity</a></li>
	<li><a href="http://specificity.keegan.st/" target="_blank">Tool - Specificity Calculator</a></li>
</ul>
&nbsp;
<div class="panel panel-default">
<div class="panel-body"><img class="pull-left" style="margin-right: 10px; border-radius: 50em;" src="https://lh3.googleusercontent.com/-4v72j5cjOSE/AAAAAAAAAAI/AAAAAAAAACU/9bGCvpe-iVE/s90-c-k-no/photo.jpg" alt="" />This is guest post by <a href="mailto:victoria.appsted@gmail.com?subject=TeckStack.com (How to Deal with Specificity Issues in CSS)" target="_blank">Victoria Brinsley</a>. is a skilled Android app developer for Appsted Ltd - <a href="http://www.appsted.com/services/android-development" target="_blank">Android apps development company</a>. You can explore more about the development tips and tricks by clearing your queries with her.</div>
</div>