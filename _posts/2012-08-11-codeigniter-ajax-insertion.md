---
ID: 263
post_title: CodeIgniter AJAX Insertion
author: Rishi Mehta
post_date: 2012-08-11 16:11:08
post_excerpt: >
  AJAX makes your system very fast. So I
  have created AJAX based Data Insertion
  method with popular PHP CodeIgniter AJAX
  Insertion.
layout: post
permalink: >
  http://teckstack.com/codeigniter-ajax-insertion
published: true
networkpub_postmessage:
  - ""
networkpub_twitterhandle:
  - ""
networkpub_twitterhash:
  - ""
better-related-:
  - 'a:6:{s:6:"offset";i:0;s:5:"stime";d:1365857649.70600795745849609375;s:7:"queries";i:13;i:263;a:43:{i:1618;d:43.0349273681640625;i:1590;d:26.97623789085532308718029526062309741973876953125;i:1559;d:0.817193508148193359375;i:1519;d:40.35143244041586996218029526062309741973876953125;i:1352;d:32.5916900634765625;i:1323;d:29.1872158050537109375;i:206;d:41.44758497993901613654088578186929225921630859375;i:1197;d:19.07275390625;i:1104;d:32.780216217041015625;i:970;d:21.1892948150634765625;i:937;d:17.3006439208984375;i:912;d:30.77295684814453125;i:893;d:16.254070281982421875;i:874;d:109.81074034492922919525881297886371612548828125;i:846;d:36.5189971923828125;i:792;d:26.9923095703125;i:774;d:18.67791748046875;i:731;d:25.1379070281982421875;i:638;d:31.596309661865234375;i:641;d:11.95060443878173828125;i:439;d:25.4625759124755859375;i:401;d:22.3371906280517578125;i:340;d:63.26464354317143801154088578186929225921630859375;i:200;d:21.577152252197265625;i:256;d:35.610942840576171875;i:240;d:58.83736383690024496218029526062309741973876953125;i:220;d:57.21863138450766683718029526062309741973876953125;i:193;d:27.7529850006103515625;i:181;d:37.25368845237876058718029526062309741973876953125;i:165;d:10.35413360595703125;i:154;d:5.333979129791259765625;i:146;d:15.53416156768798828125;i:141;d:4.245300769805908203125;i:134;d:16.3911075592041015625;i:126;d:18.6337909698486328125;i:111;d:22.0942480519132828931105905212461948394775390625;i:99;d:6.589353084564208984375;i:88;d:13.08765125274658203125;i:82;d:15.317562103271484375;i:78;d:3.1601865291595458984375;i:48;d:4.58261585235595703125;i:42;d:0.795587480068206787109375;i:24;d:69.4852745488004757135058753192424774169921875;}s:5:"etime";d:1365857649.744831085205078125;s:5:"ctime";i:1365857649;}'
dsq_thread_id:
  - "801464540"
networkpub_ogtype_facebook:
  - ""
disclosure_dropdown:
  - None
networkpub_postsummary:
  - ""
networkpub_post_image_video:
  - ""
awd_fcbk:
  - 'a:4:{s:11:"like_button";a:3:{s:8:"redefine";s:1:"0";s:7:"enabled";s:1:"0";s:5:"place";s:3:"top";}s:9:"opengraph";a:1:{s:11:"object_link";s:0:"";}s:7:"awd_ogp";a:16:{s:2:"id";s:0:"";s:12:"object_title";s:0:"";s:6:"locale";s:5:"en_US";s:10:"determiner";s:4:"auto";s:5:"title";s:7:"%TITLE%";s:4:"type";s:7:"article";s:11:"custom_type";s:10:"teckstack:";s:11:"description";s:13:"%DESCRIPTION%";s:9:"site_name";s:12:"%BLOG_TITLE%";s:3:"url";s:5:"%URL%";s:27:"auto_load_images_attachment";s:1:"0";s:6:"images";a:1:{i:0;s:0:"";}s:27:"auto_load_videos_attachment";s:1:"0";s:6:"videos";a:1:{i:0;s:0:"";}s:27:"auto_load_audios_attachment";s:1:"0";s:6:"audios";a:1:{i:0;s:0:"";}}s:30:"_nonce_options_save_ogp_object";s:10:"89f594fc89";}'
disclosure_position:
  - Above the Content
views:
  - "2185"
ac_is_copyprotect:
  - "1"
ac_is_advanced_tracking:
  - "1"
ac_postid:
  - 2yZw8fASzEv.text
ac_is_process:
  - "1"
ac_embedid:
  - 30sBg72gs-X
vortex_system_likes:
  - "0"
vortex_system_dislikes:
  - "0"
---
<blockquote><a class="zem_slink" title="Ajax (programming)" href="http://en.wikipedia.org/wiki/Ajax_%28programming%29" target="_blank" rel="wikipedia">AJAX</a> is the term used globally for successful application. AJAX makes your system very fast and lightweight. So I have decided to create some nice <strong>AJAX based Data Insertion</strong> method with popular <a class="zem_slink" title="PHP" href="http://www.php.net" target="_blank" rel="homepage">PHP</a> Framework the <strong>Codeigniter.</strong></blockquote>

I have written excellent for <a class="zem_slink" title="JQuery" href="http://jquery.com/" target="_blank" rel="homepage">JQUERY</a> AJAX to work with CodeIgniter. You can use it in CodeIgniter in full fledged.
<h2>Controller Code</h2>
<div class="wp_syntax">
<div class="code">
<pre class="prettyprint">
public function ajax_payment(){
	$this-&gt;load-&gt;model('payment_model');
	$invoice_id = $this-&gt;input-&gt;post('invoice_id');
	$payment = $this-&gt;input-&gt;post('payment');

	$this-&gt;payment_model-&gt;ajax_payment_m($invoice_id, $payment);
	return $invoice_id;
}
</pre>
</div>
</div>
<h2>Model Code</h2>
<div class="wp_syntax">
<div class="prettyprint">
<pre class="css" style="font-family: monospace;">public function ajax_payment_m($invoice_id, $payment){

    if($this-&gt;session-&gt;userdata('logged_in'))
    {
        $session_data = $this-&gt;session-&gt;userdata('logged_in');
        $user_id = $data['id'] = $session_data['id'];
    }
    $datestring = "%Y-%m-%d";
    $time = time();
    $now = mdate($datestring, $time);
    $rcv_date = date('Y-m-d', strtotime($now));

    $pay['invoice_id'] = $invoice_id;
    $pay['payment'] = $payment;
    $pay['received_date'] = $rcv_date;
    $pay['user_id'] = $user_id;

    $this-&gt;db-&gt;insert('payment', $pay);

}</pre>
</div>
</div>
<h2>JQUERY and AJAX Code</h2>
<div class="wp_syntax">
<div class="code">
<pre class="prettyprint">
$('.add_pay').click(function(){
    var id = $(this).attr('id');
    var val = $(this).attr('id').split('-');
    var ids = val[1];

    var amt = document.getElementById('pay_am-'+ids).value;

    var postData = {
        'invoice_id':ids,
        'payment':amt,
        submit:true
    };

    if(amt != ""){
        $.ajax({
        type: "POST",
        url: "http://localhost/CodeIgniter_2.1.2/index.php/payment/ajax_payment",
        dataType: "json",
        data: postData,
        success: function(){  
            alert("you added payment of amount "+amt+" USD for this invoice.");
            $('#pay_am-'+ids).value = "";
            $('#add-'+ids).hide();
            $('#pay_am-'+ids).hide();
        }
        });
    } else {
        alert("Insert Amount.");    
    }
});</pre>
</div>
</div>
<h2><a class="zem_slink" title="HTML" href="http://en.wikipedia.org/wiki/HTML" target="_blank" rel="wikipedia">HTML</a> Code</h2>
<pre class="prettyprint">
<input class="button ar hide add_pay" id="add-&amp;&lt;?php echo $invoice_item['invoice_id'] ?&gt;" type="button" name="add-&lt;?php echo $invoice_item['invoice_id'] ?&gt;" value="Add" />

<input class="textbox short ar hide" id="pay_am-&lt;?php echo $invoice_item['invoice_id'] ?&gt;" type="text" name="pay_am-&lt;?php echo $invoice_item['invoice_id'] ?&gt;" value="" />
</pre>
Also do not forget to add controller view in route file. If you forget to do so, AJAX never find such <a class="zem_slink" title="Uniform Resource Locator" href="http://en.wikipedia.org/wiki/Uniform_Resource_Locator" target="_blank" rel="wikipedia">URL</a> in the system.

In my case its something like this :

"<strong>payment</strong>" is my controller and "<strong>ajax_payment</strong>" is a function of view.
<div class="wp_syntax">
<div class="code">
<pre class="prettyprint"> 
$route['payment/ajax_payment'] = 'payment/ajax_payment';
</pre>
</div>
</div>
So now you are all set to go. Please share your opinion that will help me to improve the code in a better way.