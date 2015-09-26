---
ID: 4233
post_title: Grunt for Front End Developers
author: Guest Author
post_date: 2015-09-22 02:23:23
post_excerpt: >
  Front End Developers have to do
  development, optimization and
  minification. These takes lot of time.
  Grunt automated tasks and helps to
  improve work flow.
layout: post
permalink: http://teckstack.com/grunt-for-front-end
published: true
ac_is_process:
  - "1"
ac_is_copyprotect:
  - "1"
vortex_system_user_11:
  - 'a:2:{s:5:"liked";s:7:"noliked";s:8:"disliked";s:8:"disliked";}'
vortex_system_likes:
  - "1"
ac_is_advanced_tracking:
  - "1"
vortex_system_dislikes:
  - "0"
ac_postid:
  - 1OYvWjsK7Gs.text
ac_embedid:
  - 7wSZPXodEYG
---
Life has always been unfair to front end developers, as they have to do a lot of tasks which are indeed quite a task for them. They have to work in a lot disconcerted way and this is quite in a haphazard manner, such as-

[list icon="icon: check"]
<ul>
	<li>Work with <strong>fragments of JavaScript and CSS</strong> and then assimilate it all to put them together so that they all can work in tandem on a website.</li>
	<li>They have to <strong>minify</strong> JavaScript and compress CSS so as to make the file sizes, as small as possible so as to make a website lighter in size.</li>
	<li>They have to carry out the <strong>optimization</strong> of images, so as not to affect the quality of the images without distorting the quality.</li>
	<li>Next they also have to use <strong>Sass</strong> for CSS authoring for considering the abstractions it allows.</li>
</ul>
[/list]

What is the answer to this plight? Well, I guess as every problem has a solution so do this. We now have <a href="http://gruntjs.com/" target="_blank" rel=""><strong><span style="color: #ff6600;">Grunt</span></strong></a>, which is a panacea for this problem, as this is a <em>task runner</em> which can help you to carry on all the tasks easily. All you need is to easily set it up which is certainly not a difficult task and you can easily install it and all your tasks can be accomplished very smoothly.

Though it is really very difficult to adapt new changes, but yes  change is unavoidable and one can never grow until you are prone to changes. In this blog we will discuss how using Grunt can help us save time and evolve in the technological era.

<h2>Get Set <strong>Grunt</strong></h2>

The <a href="https://nodejs.org" target="_blank" rel="nofollow">Node</a> is a primary requirement for Grunt. You need to first install Node, but do not worry if you haven't installed it yet, as it is not a very arduous task. All you need to do is to download an installer and run it . You need to go to the node website and just click on the big Install button on it.
Grunt is installed on a project basis. You need to go to the project's folder. At the root level you will get a file named <code>package.json</code>. You need to create one file and keep it over there. The file should contain the following code.

<pre>{
    "name": "example-project",
    "version": "0.1.0",
    "devDependencies": {
         "grunt": "~0.4.1"
    }
}
</pre>

You can certainly take inspiration from this code and change the version and project bit the <code>devDependencies</code> are ought to be same.

There is a package manager called a  <a href="https://www.npmjs.com/" target="_blank" rel="nofollow">NPM</a> (Node packaged modules ) for managing Node dependencies. For instance, you can take it as a <em>plug-in for <a href="/wordpress">WordPress</a></em>. This is the way how node takes care of dependencies.

After keeping the <code>package.json</code> file in the requisite place, you need to visit the terminal and then go to the folder.

Then after you need to run this command:

<pre>npm install</pre>

After running this command, a new folder named as <strong>node_modules</strong> will come up in your project. Along with this you will get two more files, such as <em>LICENCE</em> and <em>READ.ME</em>. These files are there as the project will be kept on <a href="https://github.com/" target="_blank" rel="nofollow">GitHub</a> and this is the standard file system there.

Now, after completing all the other step, we have the culmination step where we have to <em>install command line interface</em> of  Grunt. The absence of this will lead you to a style error of  “command-not-found”. It is installed in order to improve the efficiency of the interface. Else, if you have to make ten projects, then you would have ten odd copies of Grunt CLI.

All you need to do to install CLI is just open up the terminal and run a single line command :

<pre>npm install -g grunt-cli</pre>

After running this you all you need to do is to <strong>close and open the terminal again</strong> in order to ensure that whether the things are working perfectly.

<h2>Some Features of <strong>Grunt</strong></h2>

One can certainly not deny the fact that we front end developers do not have to do all that stuff discussed in the very beginning of the article in order to make our websites look perfect and these things are an indispensable part of our life. It is certainly obvious that you need to go to various other tools for developing the best web product. This unarguably is a very time consuming process and this is why we must switch to Grunt. After using Grunt you will yourself realize the fact that there is a lot of difference in doing a job in a fragmented way and in a synchronized and collective way.

<strong>Grunt can </strong>-

<ol>
    <li>Grunt can concatenate your files.
Let us suppose that there are two different JavaScript files in a project namely:
- <strong>jquery.js</strong> – The library which we need.
- <strong>global.js</strong> – Our authored JavaScript file where we configure and call the plug-in.With the help grunt one can <em>concatenate these files together </em> in order to improve the performance of our project.</li>
    <li>Grunt can optimize images:
In order to optimize images Grunt uses <code>grunt-contrib-imagemin</code>, which you need to install using:
<pre>npm install grunt-contrib-imagemin --save-dev</pre>
Then you need to register it in the  Gruntfile.js
<pre>grunt.loadNpmTasks('grunt-contrib-imagemin');</pre>
In order to configure it you need the following code:
<pre>imagemin: {
    dynamic: {
        files: [{
            expand: true,
            cwd: 'images/',
            src: ['**/*.{png,jpg,gif}'],
            dest: 'images/build/'
        }]
    }
}</pre>
After configuring it, run it:
<pre>grunt.registerTask('default', ['concat', 'uglify', 'imagemin']);</pre>
This is one of the most minimalistic effort one can apply in order to optimize the images. Other than this Grunt can help you to easily Minify your JavaScript, makes processing faster and automates the development.</li>
</ol>

<h2>Why <strong>Grunt</strong></h2>

Another most advantageous thing about Grunt is the consistency it induces to the development teams. As we know that development is not done single handedly, but requires teams to work in a collaborative manner. The inconsistency at times can prove to be one of the most disgusting things. This is where the role of Grunt comes in. Using Grunt one can ensure that all the teams are writing the code in a standard way. This helps you save your build from failing as a lot of efforts are put in while making a build.

<h3>Wrapping Up</h3>

Do not take Grunt as a newbie market entrant in the development world. After all it has a big community of programmers, which are responsible for making new plugins and updates every now and then. Moreover, there are already a lot of tools provided by grunt which makes any new market entries of this type very less.

<div class="panel panel-default">
<div class="panel-body">This is a guest post by <a href="mailto:info.samueldawson@gmail.com?subject=TeckStack.com(Article: Choosing Grunt Front End Development)" target="_blank">Samuel Dawson</a>. With encouraging efforts from so many years Samuel has been a top-notch professional in Designs2html Ltd. Currently he is able to convert <a href="http://www.designs2html.com/services/psd-to-html">PSD to HTML5</a> with responsive design and creativity. Samuel also loves to read latest frameworks and themes in trend.</div>
</div>