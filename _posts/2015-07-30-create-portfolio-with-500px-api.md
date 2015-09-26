---
ID: 3664
post_title: >
  How to Build Creative Portfolio with
  500PX API
author: Kushal Jayswal
post_date: 2015-07-30 11:39:52
post_excerpt: >
  A discussion with Deval Jayswal, who is
  well know photo artist, encouraged me to
  create a portfolio, with photo uploading
  and a sync feature using 500px api.
layout: post
permalink: >
  http://teckstack.com/create-portfolio-with-500px-api
published: true
dsq_thread_id:
  - "3986984349"
feedweb_post_sort_value:
  - "-2"
ac_is_copyprotect:
  - "1"
ac_is_advanced_tracking:
  - "1"
ac_postid:
  - 3GHcTMbN0jz.text
ac_is_process:
  - "1"
ac_embedid:
  - 59mGdsqQqDb
vortex_system_likes:
  - "0"
vortex_system_dislikes:
  - "0"
---
<blockquote>There are many sites&nbsp;allow you to host your work&nbsp;online. You will get a link to share with anyone in the world. I like the concept and if you are from the creative field like designing or photography, people must consider your portfolio before&nbsp;giving you a job.</blockquote>
Well, I am a front end developer and I am lucky to have many friends from design backgrounds. I understand the importance of having an awesome portfolio site.

Also&nbsp;my brother, <a href="http://devaljayswal.com" target="_blank">Deval Jayswal</a>, who is well know&nbsp;photo artist,&nbsp;asked me to create a portfolio site for him, which would&nbsp;have <em>manual photo uploading and a&nbsp;sync feature.</em>&nbsp;He wanted to sync his pictures (work) from popular photographers community site - <strong>500px.com</strong>.

Before we jumped to the API, let's first understand various types of website portfolio.
<h2>Types&nbsp;of Portfolio</h2>
<ol>
	<li><strong>Static&nbsp;</strong><em>-&nbsp;HTML, CSS, JS, Images</em></li>
	<li><strong>Dynamic</strong> - <em>PHP/DOTNET/JAVA, Templates, Database</em></li>
	<li><strong>Super Dynamic</strong> <em>- Static&nbsp;with APIs</em></li>
</ol>
<strong>Static</strong> portfolio&nbsp;required front-end knowledge to maintain&nbsp;different pages as per requirement.

<strong>Dynamic</strong> type of portfolio needs core knowledge of&nbsp;backed technology&nbsp;to deal with the code and database. Here&nbsp;you would&nbsp;maintain templates instead of different pages. And this would be easier in terms of user experience.

The sites which uses APIs, I called them <strong>super dynamic</strong>. Because with use of API you can get&nbsp;data from external site and represent on your own site or app. It's great feature and saves little penny too&nbsp;as we don't need to store data on our server.

Now, let's talk about API...
<h2>What is API</h2>
API is abbreviation for <strong>Application Programming Interface</strong>. As the name suggests, it provides a layer between your application/site&nbsp;to the user with/without authentication. Well I would not stretch the point but today we will focus on "How to Build Creative Portfolio with 500PX APIs".
<h2>Get Started with 500PX API</h2>
I am assuming that you are familiar with <a href="http://teckstack.com/html">HTML</a>, <a href="http://teckstack.com/css">CSS</a> and <a href="http://teckstack.com/js">JavaScript</a>. So very first thing required is to create a 500px&nbsp;profile, where you can upload photographs and use the same to&nbsp;create&nbsp;a&nbsp;demo for your own profile.

I have used Deval Jayswal's <a href="https://500px.com/devjayswal" target="_blank">500px profile</a> to get&nbsp;and show data in a&nbsp;<a href="http://kutec.github.io/500PX-API-Test/" target="_blank">demo</a>. If you&nbsp;are a developer can <a href="https://github.com/kutec/500PX-API-Test" target="_blank">fork</a> the code.

Also, I have used <a href="http://teckstack.com/bootstrap">Bootstrap</a> to keep up responsive behavior of a demo but I am not concentrating on that part.

You may need to follow below steps before jumping to HTML and jQuery sections.
<h3>Register&nbsp;an Application</h3>
You need an application which will have KEY that holds a reference to get and post data. Please follow below steps to start.
<ol>
	<li>Go to <a href="https://500px.com/">https://500px.com</a>.</li>
	<li>If you already have an account, please login or else create one for the access.</li>
	<li>Now go to "Settings" link from Profile drop down: <a href="https://500px.com/settings">https://500px.com/settings</a>.</li>
	<li>Under settings, click on "Applications" and here you have to register your app:&nbsp;<a href="https://500px.com/settings/applications">https://500px.com/settings/applications</a>.</li>
	<li>Make sure to configure all URLs correctly.</li>
	<li>Now you will see "<strong>JavaScript SDK Key</strong>". Copy that key and replace that in below jQuery snippet section.</li>
</ol>
<h3>HTML</h3>
We need a <span class="lang:default decode:true crayon-inline">&lt;div&gt;</span>&nbsp;&nbsp;with CSS&nbsp;class&nbsp;or id,&nbsp;which we will use as a placeholder to display fetched photos from 500px site.
<pre class="lang:default mark:3 decode:true ">&lt;script src="js/500px.js"&gt;&lt;/script&gt;
&lt;script src="http://ajax.googleapis.com/ajax/libs/jquery/1.8.1/jquery.min.js"&gt;&lt;/script&gt;
&lt;section id="main-content" class="col-md-9"&gt;
    &lt;h2&gt;A Demo&lt;/h2&gt;
    &lt;div id="grid"&gt;&lt;/div&gt;
&lt;/section&gt;</pre>
<h3>jQuery</h3>
You need to <a href="http://500px.github.io/500px-js-sdk/500px.js" target="_blank">include a script</a>&nbsp;at the top of all&nbsp;custom script for api. Or&nbsp;if you stuck somewhere, this <a href="https://github.com/500px/api-documentation" target="_blank">documentation</a> might be helpful.
<pre class="lang:default decode:true">$(function() {
      _500px.init({
          sdk_key: '1234567890123456789012345678901234567890'   //replace with your 500px js sdk key
      });

      // Get my user id
      _500px.api('/users', function(response) {
          var me = "DevJayswal";
          var siteurl = "http://500px.com/photo/"

          // Get my favorites
          _500px.api('/photos', {
              feature: 'user',
              username: me,
              total_items: 5000
          }, function(response) {
              if (response.data.photos.length == 0) {
                  alert('Nothing found! Please refresh...');
              } else {
                  $.each(response.data.photos, function() {
                      $('#grid').append('&lt;article class="post col-md-3 col-sm-4 col-xs-12 panel panel-default"&gt;&lt;h3&gt;' + this.name + '&lt;/h3&gt;&lt;a href="' + siteurl + this.id + '" target="_blank"&gt;&lt;img src="' + this.image_url + '"&gt;&lt;/a&gt;&lt;/article&gt;');
                  });
              }
          });
      });
  });</pre>
In above code there are various code needs clarification.

We have started&nbsp;with a&nbsp;anonymous function to initiate <span class="lang:default decode:true crayon-inline ">_500px.init</span>&nbsp;in which <span class="lang:default decode:true crayon-inline ">sdk_key</span>&nbsp;needs to be replaced with your own key.

After that we have a code for getting user information. This code is little tricky. I have used username instead of user ID. <span class="lang:default decode:true crayon-inline ">var me</span>&nbsp;is showing&nbsp;of a user profile and afterward we are passing <span class="lang:default decode:true crayon-inline ">siteurl</span>&nbsp;which will be destination to get data. The same way you can manipulate with other properties as well. For&nbsp;getting deep knowledge on this, please refer <a href="https://github.com/500px/api-documentation/blob/master/basics/formats_and_terms.md#short-format" target="_blank">this page</a>.

After all configuration we would expect a response, which will show us a data in to <span class="lang:default decode:true crayon-inline ">&lt;div id="grid"&gt;&lt;/div&gt;</span>&nbsp;element. The rest of the things are pretty much easy to understand.

I would like to&nbsp;know your reaction at&nbsp;below comment section. Also share idea, how creatively we can be more creative&nbsp;with such a concept.
<h4>Resources</h4>
<ul>
	<li><a href="https://github.com/500px/api-documentation" target="_blank">GitHub API Documentation</a></li>
	<li><a href="https://500px.com/settings/applications" target="_blank">Register Application</a></li>
	<li><a href="https://github.com/500px/api-documentation/blob/master/basics/formats_and_terms.md#short-format" target="_blank">Format and Terms</a></li>
	<li><a href="http://kutec.github.io/500PX-API-Test/" target="_blank">Demo</a></li>
	<li><a href="https://github.com/kutec/500PX-API-Test" target="_blank">Fork</a> on Github</li>
</ul>
<h6>Special thanks to <strong>Deval Jayswal</strong> to allow us&nbsp;to use data&nbsp;from his&nbsp;profile for&nbsp;a demo.</h6>