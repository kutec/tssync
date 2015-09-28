---
ID: 4271
post_title: >
  A stepwise guide on creating Responsive
  Images using CSS
author: Guest Author
post_date: 2015-09-27 10:07:24
post_excerpt: ""
layout: post
permalink: >
  http://teckstack.com/create-responsive-images-using-css
published: false
ac_is_process:
  - "1"
ac_is_copyprotect:
  - "1"
---
Images have played a vital role in enhancing the visual quality of a website or web application. Especially, if you are targeting mobile users, then paying special attention of the proper placement of images is something you can't ignore for sure. Responsive images have become the need of the hour. With continuous efforts being made to alter the size and format of images so as to fit different devices and screen resolutions, there's no denying the fact that effective creation of responsive images has become a must. Smooth implementation of responsive images has become a vital concern among entrepreneurs who are keen on impressing their target audience via high resolution images of their business products and services. Today, through this post, I'll be offering you a step-by-step guide on creating responsive images using CSS. So, let's get straight to the steps.

<h2>Basic Responsive Image</h2>

You can use CSS for rendering a percentage-length unit(in related to width and height properties) to your images as shown below:

<pre>img {
    width: 100%;
    height: auto;
}</pre>

On observing the above code carefully, you'll find that the width property of image element has been set to 100%. The reason for this is that the image's width is equal to its related container; irrespective of the size of gadget that is being used for viewing the image. Additionally, you can also find that height of image element has been set to auto, making the image fully scalable.

Next, there is a <code>div</code> which serves as the element's container. The HTML structure for the same is shown below:

<pre>&lt;div class="imageDiv"&gt;
    &lt;img src="image.jpg" width="800" height="480" /&gt;
&lt;/div&gt;</pre>

Here, the element's container has a width property of 96% along with left and right margins. The maximum width has been set to 800px to ensure that the image layout doesn't widen up when viewed using devices with larger dimensions. Here, the CSS code snippet used for building a basic responsive image is shown below:

<pre>div. imageDiv {
    width: 96%;
    max-width: 800px;
}
div. ImageDiv img {
    width: 100%;
    height: auto;
}</pre>

<h2>Creating a Full-width Responsive Image</h2>

When it comes to a full-width responsive image, it is the one which is 100% of the viewport size. For achieving such an image, you simply need to remove the image container's max-width property and assign it a width of 100%. The CSS code associated with creation of a full-width responsive image is shown below:

<pre>. ImageDiv {
    width: 100%;
}
.ImageDiv img {
    width: 100%;
}</pre>

<h2>Creating responsive images that need to be displayed in columns</h2>

For creating responsive images which are displayed in a column(available within a grid), then all you need to do is simply reduce the value for CSS width property. Also, you need to assign a display property value to the image element. Let us understand this using two different scenarios.

<ol>
    <li>
<h3>Building a two-column Responsive Image Layout</h3>
In accordance to the basic responsive image example covered above, in order to create a two-column responsive image layout, all you need to do is set the CSS width property of the image to 47% which is nearly half of the imagecontainer. Do remember, setting the value for CSS width to 50% may not allow spaces for the margins. Hence, it is recommended to avoid the same. The modified HTML and CSS for the same would look like this:
<h4>HTML</h4>
<pre>&lt;div class="imgDiv"&gt;
    &lt;img src="image1.jpg" width="800" height="800" /&gt;
    &lt;img src="image2.jpg" width="800" height="480" /&gt;
&lt;/div&gt;</pre>
<h4>CSS</h4>
<pre>.imgDiv img {
    width: 48%;
    height: auto;
    display: inline-block;
}</pre>
<h4>Output</h4>
<img class="aligncenter wp-image-4323 size-full" src="http://teckstack.com/tsdir/wp-content/uploads/2015/09/1.jpg" alt="Two Column Responsive Image Layout" width="640" height="157" /></li>
    <li>
<h3>Building a three-column Responsive Image Layout</h3>
For a three-column responsive image layout, you need to set the width property to one-third of the container's width i.e nearly 31%  as shown in the below HTML and CSS code snippets:
<h4>HTML</h4>
<pre>&lt;div class="imgDiv"&gt;
    &lt;img src="image1.jpg" alt="" width="800" height="480" /&gt;
    &lt;img src="image2.jpg" alt="" width="800" height="480" /&gt;
    &lt;img src="image3.jpg" alt="" width="800" height="480" /&gt;
&lt;/div&gt;</pre>
<h4>CSS</h4>
<pre>. imgDiv img {
      width: 30%;
      height: auto;
     display: inline-block;
}
</pre>
<img class="aligncenter size-full wp-image-4324" src="http://teckstack.com/tsdir/wp-content/uploads/2015/09/2.jpg" alt="Three Column Responsive Image Layout" width="640" height="146" /></li>
</ol>

<h4>Conclusion</h4>

Stunning responsive images serve as the backbone for varied types of websites and apps that need to cater to the mobile audience. Here's hoping the details jotted down in the above post would serve as your right guide the next time you plan to create a responsive image for your mobile-friendly website/app.

<div class="panel panel-default">
<div class="panel-body">This is a guest post by <a href="mailto:rick.mobiers@gmail.com?subject=TeckStack.com(Article: Choosing Grunt Front End Development)" target="_blank">Rick Brown</a>. He is a highly skilled mobile app developer for Mobiers Ltd – a renowned <a href="http://www.mobiers.com/services/iphone-development">iOS app development company</a>. In order to avail his assistance either to clear your queries or to avail detailed information, get in touch with him.</div>
</div>