---
ID: 2049
post_title: Branding Google Sheets for Reports
author: Kushal Jayswal
post_date: 2013-09-16 13:35:08
post_excerpt: >
  Using Google Sheets for representation
  of statistical reports with your brand
  is quiet amazing and easy thing.
layout: post
permalink: >
  http://teckstack.com/branding-google-sheets
published: true
dsq_thread_id:
  - "1765978459"
dcssb_short_url:
  - http://j.mp/1hnyDtY
authorsure_include_css:
  - ""
views:
  - "1650"
wbounce_status:
  - default
ac_is_copyprotect:
  - "1"
ac_is_advanced_tracking:
  - "1"
ac_postid:
  - 5Mg0zP6HFQe.text
ac_is_process:
  - "1"
ac_embedid:
  - 3MLCKuE5zCu
vortex_system_likes:
  - "0"
vortex_system_dislikes:
  - "0"
---
Usually we use Presentation Slide (i.e: <abbr title="Extension - MS PowerPoint">PPT</abbr>) to represent statistical reports to client. But somehow I found PPT very limited as far as space concern. We get limited and fixed-square space to showcase. If we place graph and numerical statistics on the same slide, we would get visually grunge result. And in genuine business, report is the key to success.

I found a way - the <strong>Google Sheets</strong>. Using GD, you can create statistical report using Google Sheet and this article will focus on some tips to create a branding over it with your preferences. (i.e.: like colors, logo, etc.).
<h3>What You Should Know</h3>
<ol>
	<li><a title="MS Office - Excel" href="http://office.microsoft.com/en-us/excel/" target="_blank" rel="nofollow">Microsoft Office</a> or</li>
	<li><a title="Open Office" href="http://www.openoffice.org/product/calc.html" target="_blank" rel="nofollow">Open Office</a> or</li>
	<li><a title="Libre Office" href="http://www.libreoffice.org/features/calc/" target="_blank" rel="nofollow">Libre Office</a></li>
</ol>
<h2>What You Will Learn</h2>
<ol>
	<li>Creating a spread sheet</li>
	<li>Publishing files on the Web</li>
	<li>Changing access</li>
	<li>Embedding spread sheet in HTML file with your own branding</li>
</ol>
<a title="DEMO" href="http://demo.teckstack.com/files/gd-sample.html" target="_blank">DEMO</a>
<h2>What is Google Drive</h2>
<a title="Google Drive" href="http://drive.google.com" target="_blank" rel="nofollow">Google Drive</a> is utility tool based on  cloud services from <a title="Google Inc." href="http://google.com" target="_blank">Google Inc</a>. It is widely used because of free storage and hassle-free sharing ability. Also, you can download created documents or sheets anytime to use in your local machine.

You should have <a title="Get GMAIL id" href="https://mail.google.com/" target="_blank" rel="nofollow">Google email</a> to use GD services. GD has a tool to <a title="Google Drive - Download" href="https://tools.google.com/dlpage/drive" target="_blank" rel="nofollow">download</a> and install as utility to your OS. Once installed, you will get folder named "Google Drive" on your desktop or specified location. And further you will get options added as a context menu of while exploring something into your OS.

With the use of GD (as an Admin) you can change / edit access to the file. You can choose accessibility of the sharing.

Even more you can publish the file on the internet. This feature inspired me to write this article that can enhance the way to represent statistical reports for your company.
<h2><span style="font-size: 13px;"> </span>Publish on The Web</h2>
<ol>
	<li>Open a spread sheet file online from your GD</li>
	<li>Navigate to <strong>File</strong> menu</li>
	<li>Click on "<strong>Publish to the Web...</strong>"</li>
	<li>And now click on "<strong>Start Publishing</strong>", will allow your file visible with shared entities (users).</li>
</ol>
You can choose users to give access for viewing and editing.
<h2>The Branding Things</h2>
Following are the steps that helps you to meet our goal mentioned in YELLOW BOX above.
<ol>
	<li><strong> Create a New Folder</strong> somewhere in GD. (You need a new folder because we are going to share this folder for public access).</li>
	<li>Create a new HTML file (or <a title="Right Click to Download Sample File" href="http://demo.teckstack.com/files/gd-sample.html" target="_blank">download sample file</a>).</li>
	<li>Open specific file that you want to represent with your logo.</li>
	<li>Follow steps 1-4 described in above for "<strong>Google Drive - File Publishing for the Web</strong>".</li>
	<li>Select "<strong>HTML to embed in a page</strong>" as shown in GD (figure 1.2) and copy IFRAME code.</li>
	<li>Replace the IFRAME code and <em>change height and width to 100% </em>in sample file (this will make your sheet spread over the screen size of your browser window).</li>
</ol>
Few more steps you need to follow for URL purpose. If you have your own hosting space there is no problem you can map you domain to open INDEX.html by opening folder path. Inside folder you just need to put INDEX.html file with iframe code will show the sheet.
<h3>Placing a Logo</h3>
I have used default GD CSS in sample file. But you can write your own CSS and HTML.

<strong>HTML</strong> is just placing a `&lt;img&gt;` tag as below.
<pre>&lt;img src="http://domainname.com/logo1.png" width="183px" height="31px" alt="Logoname"&gt;</pre>
<h3><b>Embedding a Sheet</b><strong> </strong></h3>
<pre>&lt;iframe width='500' height='300' frameborder='0' src='https://docs.google.com/spreadsheet/pub?key={0AolQtcKU5grKdGYzYjRoVXJoV3BCX1YxSG1uX2k2bWc}&amp;output=html&amp;widget=true'&gt;</pre>
You have to replace the `key` value with your own.
<h3><strong>CSS</strong></h3>
<pre>#wrapper { 
    padding-top: 67px; 
}
.folder-overlay-header .folder-overlay-top-bar { 
    height: 65px !important; 
}
.folder-overlay-header {
    padding-left: 0 !important;
    text-align: center;
}
.folder-drive-logo { 
    position: relative; 
}</pre>
Kindly share your views in below <a href="#comments" target="_blank">comment</a> section.