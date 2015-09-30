---
ID: 3822
post_title: Dialog
author: Manish Sharma
post_date: 2015-07-18 19:14:05
post_excerpt: ""
layout: webdocs
permalink: >
  http://teckstack.com/webdocs/html5/elements/d/dialog
published: true
---
HTML5 now has a semantic Dialog tag. New Dialog tag behaves like a modal pop to show content, forms, buttons and many more. It will work in all modern browsers. We can create Model pop using HTML5 dialog tag without any JS library.
<h2>Methods</h2>
[list icon="icon: minus"]
<ul>
	<li><code>Show()</code>
We can use show() method to display the dialog. This is the default JS method to display hidden content, but it will not able to align vertically the dialog and user can interact with other elements.</li>
	<li><code>ShowModal()</code>
This is the default method to show the dialog box. It will align center by default in browser. `ShowModel()` method give a backdrop to dialog to prevent the other element.</li>
	<li><code>Close()</code>
This is the default method to hide the dialog box.</li>
</ul>
[/list]
<h2>Attributes</h2>
[list icon="icon: minus"]
<ul>
	<li><code>open</code>
We can use <code>(open)</code> attribute to show the dialog on page load, same as <code>show()</code> method work, but the overlay of the dialog will not be aligned in middle of the screen.</li>
</ul>
[/list]
<h2>Code</h2>
<h4>HTML</h4>
<pre>&lt;dialog id="MyDialog"&gt;&lt;/dialog&gt;</pre>
<h4>Script</h4>
<pre>// assign var dialog using ID
var dialog = document.getElementById('MyDialog');

// show dialog and overlay method
document.getElementById('show').onclick = function() { &nbsp;
&nbsp;&nbsp; &nbsp;dialog.showModal();
};

// close dialog and overlay method
document.getElementById('close').onclick = function() { &nbsp;
&nbsp;&nbsp; &nbsp;dialog.close();
};</pre>
Using the JavaScript <code>onclick</code> event user can simply call the default dialog methods.