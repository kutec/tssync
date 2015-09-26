---
ID: 1906
post_title: >
  WordPress Gravity Forms Paypal Add-on
  INR Setup
author: Rishi Mehta
post_date: 2013-06-14 23:06:30
post_excerpt: ""
layout: post
permalink: >
  http://teckstack.com/wordpress-gravity-forms-paypal-add-on-inr-setup
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
  - "1402297756"
quality_blog_tip_done1:
  - 'no'
quality_blog_tip_done2:
  - 'no'
quality_blog_tip_done3:
  - 'no'
quality_blog_tip_done4:
  - 'no'
quality_blog_tip_done5:
  - 'no'
quality_blog_tip_done6:
  - 'no'
quality_blog_tip_done7:
  - 'no'
quality_blog_tip_done8:
  - 'no'
quality_blog_tip_done9:
  - 'no'
quality_blog_tip_done10:
  - 'no'
quality_blog_tip_done11:
  - 'no'
quality_blog_tip_done12:
  - 'no'
quality_blog_tip_done13:
  - 'no'
quality_blog_tip_done14:
  - 'no'
quality_blog_tip_done15:
  - 'no'
quality_blog_tip_done16:
  - 'no'
quality_blog_tip_done17:
  - 'no'
quality_blog_tip_done18:
  - 'no'
quality_blog_tip_done19:
  - 'no'
quality_blog_tip_done20:
  - 'no'
quality_blog_tip_done21:
  - 'no'
quality_blog_tip_done22:
  - 'no'
quality_blog_tip_done23:
  - 'no'
quality_blog_tip_done24:
  - 'no'
quality_blog_tip_done25:
  - 'no'
views:
  - "2567"
post_views_count:
  - "0"
ac_is_copyprotect:
  - "1"
ac_is_advanced_tracking:
  - "1"
ac_postid:
  - 41aL9Y0UkBo.text
ac_is_process:
  - "1"
ac_embedid:
  - 68FqL0yZ8ut
vortex_system_likes:
  - "0"
vortex_system_dislikes:
  - "0"
---
<blockquote>Gravity Forms is popular plugin to create customized multipurpose forms in WordPress with Paypal addon. You can use it as mini e-commerce forms by which you can sell products and collect money on Paypal directly.</blockquote>
Last time I written on <a title="WordPress WooCommerce – Setup PAYPAL for INR" href="http://www.teckstack.com/wordpress-woocommerce-setup-paypal-for-inr/" target="_blank">WordPress WooCommerce – Setup PAYPAL for INR</a>. After number of comments on it, I got some requests to make it for <a title="Gravity Forms" href="https://www.e-junkie.com/ecom/gb.php?cl=54585&amp;c=ib&amp;aff=245414" target="_blank">Gravity Forms with Paypal add-on</a>. So I tried on it and finally get it done. So here's the code.

First of all you need to add <a title="Gravity Forms" href="https://www.e-junkie.com/ecom/gb.php?cl=54585&amp;c=ib&amp;aff=245414" target="_blank">Gravity Forms</a> and <a title="Paypal Addon Plugins" href="http://www.gravityforms.com/add-ons/paypal/" target="_blank">Paypal add-on plugins</a> in your WordPress and make sure both activated.

Now, if you go to setting page of <a title="Gravity Forms" href="https://www.e-junkie.com/ecom/gb.php?cl=54585&amp;c=ib&amp;aff=245414" target="_blank">Gravity Forms</a>, you have option to select currency. You need INR or Indian Rupees there. To get it you can add below code to your theme's <strong>function.php</strong> file.
<pre>add_filter("gform_currencies", "update_currency");

function update_currency($currencies) {
	$currencies['INR'] = array(
	"name" =&gt; __("INR", "gravityforms"),
	"symbol_left" =&gt; "₹",
	"symbol_right" =&gt; '',
	"symbol_padding" =&gt; " ",
	"thousand_separator" =&gt; ',',
	"decimal_separator" =&gt; '.',
	"decimals" =&gt; 2);

	return $currencies;
}</pre>
Now you can select INR currency on setting page and save it. So we have amount in INR for <em>website only</em>. But as <a title="Goto #8 on Article" href="http://www.teckstack.com/wordpress-woocommerce-setup-paypal-for-inr/" target="_blank">last time we see</a>, when you submit form to Paypal, it consider as USD though. It means we have changed only symbol yet for currency. Actual conversion from ₹ to $ is pending. <em>(i.e.: for now it will consider ₹100 = $100)</em> So we need to convert ₹ in $ before they submitted to Paypal.

So for that we are going to edit <em>Paypal add-on core file</em>. Go to your plugin directory, open Paypal add-on directory and check for <strong>paypal.php</strong> file. I guess it will be easy as there are only 2 files there. Now open paypal.php file in your favorite code-editor.

<strong>Go to line no : 2596</strong>

Existing code will be like this :
<pre>if(is_array(rgar($product,"options"))){
	$option_index = 1;
	foreach($product["options"] as $option){
		$field_label = urlencode($option["field_label"]);
		$option_name = urlencode($option["option_name"]);
		$option_fields .= "&amp;on{$option_index}_{$product_index}={$field_label}&amp;os{$option_index}_{$product_index}={$option_name}";
		$price += GFCommon::to_number($option["price"]);
		$option_index++;
	}
}</pre>
Just below this code add following code to the same file:
<pre>$current_currency = GFCommon::get_currency();

if($current_currency == "INR") {
	$convert_rate = self::get_exchange_rate(); //Set converting rate
	$price = round( $price / $convert_rate, 2);
}</pre>
So basically, we added our currency conversion to ₹. But we didn't <strong>declare our conversion rates function</strong> yet. So to do so just go to end of this function and add our exchange rate function.
<pre>public static function get_exchange_rate($from='USD', $to='INR') {
	$url = "http://www.google.com/ig/calculator?hl=en&amp;q=1%s=?%s"; //url for the currency convertor
	$result = wp_remote_retrieve_body($response = wp_remote_get(sprintf($url, $from, $to))); // fetches the result from the url

	if(is_wp_error( $response )) {
		return FALSE;
	}

	$result = explode('"',$result);
	$result = str_replace(chr(160), '', substr( $result[3], 0, strpos($result[3], ' ') ) );

	return ( $result == 0 ) ? FALSE : $result;
}</pre>
So, we done for the ₹ now, if you check now everything goes perfect for product prices and quantity too. But there is still one mysterious thing remains and that is <strong>shipping price</strong>. if you are using shipping price than you also need to convert it for $ too.

<strong>For that go to the line no : 2620</strong>
Code will be like this:
<pre>$shipping = !empty($products["shipping"]["price"]) ? "&amp;shipping_1={$products["shipping"]["price"]}" : "";</pre>
Replace code with the following one:
<pre>$shiiping_product = $products["shipping"]["price"];

if($current_currency == "INR") {
	$convert_rate = self::get_exchange_rate(); //Set converting rate
	$shiiping_product = round( $shiiping_product / $convert_rate, 2);
}

$shipping = !empty($products["shipping"]["price"]) ? "&amp;shipping_1={$shiiping_product}" : "";</pre>
That's it!!. You can again use this full code with any custom currency and for that need to update currency symbols and name for theme function file and currency in our exchange rate function declaration.

Happy Coding!