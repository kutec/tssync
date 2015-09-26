---
ID: 1790
post_title: How To Create Custom Widget in WordPress
author: Rishi Mehta
post_date: 2013-05-07 21:36:37
post_excerpt: 'Create Custom Widget in Wordpress -  WordPress has default widgets that can use easily. Specific needs force to write custom code.'
layout: post
permalink: >
  http://teckstack.com/create-custom-widget-in-wordpress
published: true
networkpub_postmessage:
  - ""
networkpub_postsummary:
  - ""
networkpub_twitterhandle:
  - ""
networkpub_twitterhash:
  - ""
networkpub_ogtype_facebook:
  - ""
networkpub_post_image_video:
  - ""
disclosure_dropdown:
  - None
disclosure_position:
  - Above the Content
dsq_thread_id:
  - "1270547143"
views:
  - "2056"
ac_is_copyprotect:
  - "1"
ac_is_advanced_tracking:
  - "1"
ac_postid:
  - 2DB_C8QXbYY.text
ac_is_process:
  - "1"
ac_embedid:
  - 3Zv_E0xJu1O
vortex_system_likes:
  - "0"
vortex_system_dislikes:
  - "0"
---
WordPress is great tool for Freelancers for creating small websites very quickly. But sometimes you need to be smart enough while the need have specification. Instead of googling for a plugins OR widgets, you should try for custom development. Yes! If you try coding yourself, skill can be enhanced and you will feel more confident.

[note]<a title="DOWNOLAD" href="http://demo.teckstack.com/custom_widget/custom-widget.php" target="_blank">Download Code</a> (Right Click <em>to save</em>)[/note]

Here I am going to discuss about “<b>How To Create Custom Widget in Wordpress</b>”. WordPress has some default widgets that you can use easily by just dragging it to the dropbox (widget area). But if you want something special OR in your way you need to write your own custom code.

Let's start with creating a custom widget for your theme.

<em>Note: I would use “include” directory inside theme folder to start with. If you are using some premium theme “include” can be there already.</em>

Lets assume the requirement like some <strong>form</strong> <em>as a widget</em>.
<ol>
	<li>Create <span style="font-family: 'courier new', courier;">include</span> folder. <em>(i.e.:  website.com/wp-content/themes/)</em></li>
	<li>Create new file <strong><span style="font-family: 'courier new', courier;">widget.php</span></strong></li>
	<li>Open <strong><span style="font-family: 'courier new', courier;">function.php</span></strong> and include newly created widget.php file. [code lang="php"]include('includes/widget.php');[/code]</li>
</ol>
<h2>Few Words</h2>
Many developers have common practice to add custom code into main library file. But I would suggest to create separate file instead of mess them all in one. Why? Because when you will have same kind of requirement you can take the file and put it to your new theme without hesitation. And I think it is obviously good thing while you do not remember and search for that code line-by-line in a file. So we can say, creating a separate file is more professional approach.
<h2>Let's Code Now</h2>
<em>I generally use Adobe Dreamweaver as a code/text editor. </em><strong>Open <span style="font-family: 'courier new', courier;">widget.php</span></strong> file now.

First we need to say wordPress that I am creating new widget by using your library function so please start the process...
<pre>add_action( 'widgets_init', 'load_my_widgets' );</pre>
<strong><span style="font-family: 'courier new', courier;">load_my_widgets</span></strong> is function which would give name to new widget and load it.
<h3>Defining Custom Widget</h3>
<pre>function load_my_widgets() {
    //your code here
 }</pre>
<em>Now I am assuming the requirement as adding telephone number. And while we save the widget it will show that information on a website.</em>
<h3>Registering a Widget</h3>
We are going to register our new widget as "<strong>my_phone_widget</strong>".
<pre>function load_my_widgets() {
    register_widget('my_phone_widget');
 }</pre>
<h3>Few Tips</h3>
<ol>
	<li>You need to declare widget as a class so that which can actually extends WordPress' default <strong>wp_widget</strong> class.</li>
	<li>Every widget class needs 4 functions to declare
<ul>
	<li>main function which will have <strong>Widget Arguments</strong></li>
	<li><strong>Widget Function</strong> which shows data outside and create <em>print function</em></li>
	<li><strong>Update Function</strong> which updates data in widget when you <em>save</em></li>
	<li>Form which contains widget HTML/PHP for back-end. So when you add data, or update data it pass to functions respectively</li>
</ul>
</li>
</ol>
<h2>MAIN FUNCTION</h2>
<pre>class my_phone_widget extends WP_Widget {
    function my_phone_widget (){
        $widget_ops = array( 'classname' =&gt; 'phone', 'description' =&gt; 'A widget that displays your phone number' );
        $control_ops = array( 'width' =&gt; 250, 'height' =&gt; 120, 'id_base' =&gt; 'phone-widget' );
        $this-&gt;WP_Widget( 'phone-widget', 'RB Phone Widget', $widget_ops, $control_ops );
    }
 }</pre>
<h2>WIDGET FUNCTION</h2>
This will print data on site.
<pre>function widget($args, $instance){
    extract($args);
    $title = apply_filters('widget_title', $instance['title']);
    $phone = $instance['number'];
    $text = $instance['text'];
    echo $before_widget;
    echo $before_title.$title.$after_title;
    echo '' . $text . ' <strong>' . '<a href="callto:' . str_replace(array('(', ')', '-', ' '), '', $phone) . '">' . $phone . '</a>' . '</strong>';
    echo $after_widget;
}</pre>
Above function adds two variables in function <span style="font-family: 'courier new', courier;">$arg</span> coming from WordPress and theme sidebar functions and <span style="font-family: 'courier new', courier;">$instance</span> is coming from our widget data. Above code will print <strong>phone number</strong> and <strong>text</strong> <em>on site</em>.

Now we need <strong>Update Function</strong> and a <strong>Form</strong> <em>to add data</em>.
<h2>UPDATE FUNCTION</h2>
<pre>function update($new_instance, $old_instance){
    $instance = $old_instance;
    $instance['title'] = strip_tags($new_instance['title']);
    $instance['text'] = strip_tags($new_instance['text']);
    $instance['number'] = strip_tags($new_instance['number']);
    return $instance;
 }</pre>
<h2>THE FORM</h2>
<pre>function form($instance){
    $defaults = array( 'title' =&gt; 'Phone Number', 'text' =&gt; 'Call Us', 'number' =&gt; '' );
    $instance = wp_parse_args((array) $instance, $defaults);
?&gt;</pre>
<pre>&lt;p&gt;
    <label for="&lt;?&lt;span class=">php echo $this-&gt;get_field_id( 'title' ); ?&gt;"&gt;<!--?php _e('Title:', 'mythemename'); ?--></label>
    &lt;input id="<!--?php echo $this--->get_field_id( 'title' ); ?&gt;" name="<!--?php echo $this--->get_field_name( 'title' ); ?&gt;" value="<!--?php echo $instance['title']; ?-->" style="width:100%;" /&gt;
&lt;/p&gt;</pre>
<pre>&lt;p&gt;
    <label for="&lt;?&lt;span class=">php echo $this-&gt;get_field_id( 'text' ); ?&gt;"&gt;<!--?php _e('Text:', '<span class="hiddenSpellError" pre=""-->mythemename'); ?&gt;</label>
    &lt;input id="<!--?php echo $this--->get_field_id( 'text' ); ?&gt;" name="<!--?php echo $this--->get_field_name( 'text' ); ?&gt;" value="<!--?php echo $instance['text']; ?-->" style="width:100%;" /&gt;
&lt;/p&gt;</pre>
<pre>&lt;p&gt;
    <label for="&lt;?php echo $this-&gt;get_field_id( 'number' ); ?&gt;"><!--?php _e('Phone number:', '<span class="hiddenSpellError" pre=""-->mythemename'); ?&gt;</label>
    &lt;input id="<!--?php echo $this--->get_field_id( 'number' ); ?&gt;" name="<!--?php echo $this--->get_field_name( 'number' ); ?&gt;" value="<!--?php echo $instance['number']; ?-->" style="width:100%;" /&gt;
&lt;/p&gt;
&lt;?php }</pre>
[note]<a title="DOWNOLAD" href="http://demo.teckstack.com/custom_widget/custom-widget.php" target="_blank">Download Code</a> (Right Click <em>to save</em>)[/note]