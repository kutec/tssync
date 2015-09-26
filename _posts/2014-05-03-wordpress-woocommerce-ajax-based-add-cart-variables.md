---
ID: 2550
post_title: 'WordPress Woocommerce &#8211; AJAX based Add to Cart for Variables'
author: Rishi Mehta
post_date: 2014-05-03 13:21:18
post_excerpt: "WordPress WooCommerce doesn't have functionality of AJAX for variable products and this article will show you can can do the same."
layout: post
permalink: >
  http://teckstack.com/wordpress-woocommerce-ajax-based-add-cart-variables
published: true
authorsure_include_css:
  - ""
authorsure_hide_author_box:
  - ""
dsq_thread_id:
  - "2678812827"
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
  - "4106"
post_views_count:
  - "1"
ac_is_copyprotect:
  - "1"
ac_is_advanced_tracking:
  - "1"
ac_postid:
  - 441Rp0YN_bV.text
ac_is_process:
  - "1"
ac_embedid:
  - 4a2YeskG65r
vortex_system_likes:
  - "0"
vortex_system_dislikes:
  - "0"
---
If you are familiar with WordPress CMS then you might know about <a title="WooCommerce" href="http://www.woothemes.com/woocommerce/" target="_blank">WooCommerce</a> plugin. Well, WooCommerce is an eCommerce plugin that converts your WordPress CMS into dynamic shopping cart. It provides easy to use interface to play with products that you want to sell and earn money online.

I am using WooCommerce from 2 years. In my earlier article - I have written about <a title="WordPress Gravity Forms Paypal Add-on INR Setup" href="http://teckstack.com/wordpress-gravity-forms-paypal-add-on-inr-setup/">setting up PayPal for INR in WooCommerce</a>. You should have used WooCommerce to understand this article. Recently one of my project stuck and I will explain the solution that might help other developers too.

<h2>The Requirement</h2>

Most of eCommerce website has <a title="Variable Products in WooCommerce" href="http://docs.woothemes.com/document/product-variations/" target="_blank">variable products</a> to make an easy buy. But WordPress WooCommerce does not give variable product with <a title="AJAX - Wikipedia" href="http://en.wikipedia.org/wiki/Ajax_(programming)" target="_blank">AJAX.</a> The project I was working was having all variable products and client wanted <strong>add to cart functionality</strong> on a single page. Also there should not be a separate product page instead everything should work on shopping page, category page or archive page. It means all variations of products should visible on archive page and we should able to add them to cart using AJAX.

<h2>Google Didn't Help</h2>

It was easy to show variables on archive page and I had done it within 15-20 minutes. After that real challenge started. I googled for "<strong>AJAX based Add to Cart for Variable Products</strong>" for couple of days and I found no solution but many tickets need solution for the same. That pushed me to find the solution by my own.

I took 2 hours for adding <strong><em>AJAX based Add to Cart Variable Products</em></strong> functionality.

Solution needs to change WooCommerce default core file, I would not suggest to do so if you are not a developer. Instead you should contact <a title="Rishi Mehta - WordPress Expert" href="mailto:rishi@rcreators.com?subject=Post%20(WordPress Woocommerce – AJAX based Add to Cart for Variable Products)" target="_blank">me</a> for better solution.

<h2>The Solution</h2>

Might below video will guide you on <em>adding variable products to WooCommerce</em>.
http://youtu.be/_qOmOIxpjDw

First of all we need variable product option selection on archive page. you can add below code in your <em>theme function</em> file.

<pre>if ( ! function_exists( 'woocommerce_template_loop_add_to_cart' ) ) {
     function woocommerce_template_loop_add_to_cart() {
         global $product;

         if ($product-&gt;product_type == "variable" ) {
             woocommerce_variable_add_to_cart();
         }
         else {
             woocommerce_get_template( 'loop/add-to-cart.php' );
         }
     }
}
</pre>

Above code will get option to select variable option on your archive or category page. Means <strong>select option button</strong> will change with your selected variable drop-down.

Now if you try to add product in cart - current page will reload and you will also get it done successfully (as per WooCommerce default functionality). But with AJAX WooCommerce has not implemented yet.

<blockquote>AJAX means no more page reload in very simple term.</blockquote>

<ul>
  <li>You need a JavaScript file to write custom code which manipulate AJAX request</li>
  <li>I have created a JavaScript file - `add-to-cart-variable.js`</li>
</ul>

<h2>jQuery Changes</h2>

<strong>Now create a new JavaScript file with below code and save it in your theme's JS directory and include file in your <em>theme footer</em>.</strong>

<pre>jQuery( function( $ ) {

    // wc_add_to_cart_params is required to continue, ensure the object exists
    if ( typeof wc_add_to_cart_params === 'undefined' )
        return false;

    // Ajax add to cart
    $( document ).on( 'click', '.product_type_variable', function() {
        
        $variation_form = $( this ).closest( '.variations_form' );
        var var_id = $variation_form.find( 'input[name=variation_id]' ).val();
        var att_grind = $variation_form.find( 'select[name=attribute_grind]' ).val();
        var att_size = $variation_form.find( 'select[name=attribute_size]' ).val();
        
        // AJAX add to cart request
        
        var $thisbutton = $( this );

        if ( $thisbutton.is( '.product_type_variable' ) ) {

            if ( ! $thisbutton.attr( 'data-product_id' ) )
                return true;

            $thisbutton.removeClass( 'added' );
            $thisbutton.addClass( 'loading' );

            var data = {
                action: 'woocommerce_add_to_cart_variable_rc',
                product_id: $thisbutton.attr( 'data-product_id' ),
                quantity: $thisbutton.attr( 'data-quantity' ),
                variation_id: var_id,
                variation: { attribute_grind: att_grind, attribute_size: att_size }
            };

            // Trigger event
            $( 'body' ).trigger( 'adding_to_cart', [ $thisbutton, data ] );

            // Ajax action
            $.post( wc_add_to_cart_params.ajax_url, data, function( response ) {

                if ( ! response )
                    return;

                var this_page = window.location.toString();

                this_page = this_page.replace( 'add-to-cart', 'added-to-cart' );

                if ( response.error &amp;&amp; response.product_url ) {
                    window.location = response.product_url;
                    return;
                }

                // Redirect to cart option
                if ( wc_add_to_cart_params.cart_redirect_after_add === 'yes' ) {

                    window.location = wc_add_to_cart_params.cart_url;
                    return;

                } else {

                    $thisbutton.removeClass( 'loading' );

                    fragments = response.fragments;
                    cart_hash = response.cart_hash;

                    // Block fragments class
                    if ( fragments ) {
                        $.each( fragments, function( key, value ) {
                            $( key ).addClass( 'updating' );
                        });
                    }

                    // Block widgets and fragments
                    $( '.shop_table.cart, .updating, .cart_totals' ).fadeTo( '400', '0.6' ).block({ message: null, overlayCSS: { background: 'transparent url(' + wc_add_to_cart_params.ajax_loader_url + ') no-repeat center', backgroundSize: '16px 16px', opacity: 0.6 } } );

                    // Changes button classes
                    $thisbutton.addClass( 'added' );

                    // View cart text
                    if ( ! wc_add_to_cart_params.is_cart &amp;&amp; $thisbutton.parent().find( '.added_to_cart' ).size() === 0 ) {
                        $thisbutton.after( ' &lt;a class="added_to_cart wc-forward" title="' + wc_add_to_cart_params.i18n_view_cart + '" href="' + wc_add_to_cart_params.cart_url + '"&gt;' + wc_add_to_cart_params.i18n_view_cart + '&lt;/a&gt;' );
                    }

                    // Replace fragments
                    if ( fragments ) {
                        $.each( fragments, function( key, value ) {
                            $( key ).replaceWith( value );
                        });
                    }

                    // Unblock
                    $( '.widget_shopping_cart, .updating' ).stop( true ).css( 'opacity', '1' ).unblock();

                    // Cart page elements
                    $( '.shop_table.cart' ).load( this_page + ' .shop_table.cart:eq(0) &gt; *', function() {

                        $( 'div.quantity:not(.buttons_added), td.quantity:not(.buttons_added)' ).addClass( 'buttons_added' ).append( '&lt;input id="add1" class="plus" type="button" value="+" /&gt;' ).prepend( '&lt;input id="minus1" class="minus" type="button" value="-" /&gt;' );

                        $( '.shop_table.cart' ).stop( true ).css( 'opacity', '1' ).unblock();

                        $( 'body' ).trigger( 'cart_page_refreshed' );
                    });

                    $( '.cart_totals' ).load( this_page + ' .cart_totals:eq(0) &gt; *', function() {
                        $( '.cart_totals' ).stop( true ).css( 'opacity', '1' ).unblock();
                    });

                    // Trigger event so themes can refresh other areas
                    $( 'body' ).trigger( 'added_to_cart', [ fragments, cart_hash ] );
                }
            });

            return false;

        }

        return true;
    });

});
</pre>

Now in above code there is lots of thing you need to change according to your template and your product variations.

<ol>
  <li>Make sure your variable products' add to cart button have a class `product_type_variable`.</li>
  <li>If you check into code there is a `var` declaration. In that list you need to declare your own products' variables name like in my example variation name is <strong>grind and size</strong>. you can add or change so.</li>
  <li>In data array, you need to update your "variation" values according to your variations. It will be same as below. Just replace grind and size with your variation.
    <pre>var att_variation_name = $variation_form.find( 'select[name=attribute_variation_name]' ).val();
// Like in above code we have a variation size it will be convert to below //
var att_size = $variation_form.find( 'select[name=attribute_size]' ).val();
</pre>
  </li>
</ol>

That's it you are done with jQuery changes. Now if you try to add variable product in cart, AJAX will work and <strong>loading icon</strong> will come.

Also it will show <strong>product added to cart</strong> text and <strong>view cart</strong> button but it's not all! If you check shopping cart after above code change, product will not be added in and you will find empty cart.

<h2>WooCommerce Core File Changes</h2>

Now it's time when you need to make change in WooCommerce's file which handles AJAX request.

Go to <strong>WordPress - WooCommerce plugin directory</strong> -&gt; <strong>Includes</strong> and open file named <span class="lang:default decode:true crayon-inline">class-wc-ajax.php</span>. Open the file in some code-editor. Go to <strong>line no 29</strong>. it's having code below code.

<pre>
'add_to_cart' =&gt; true,
'checkout'    =&gt; true,
</pre>

Add below code in between this 2 line. so it will be below code

<pre>
'add_to_cart' =&gt; true,
'add_to_cart_variable_rc' =&gt; true,
'checkout'     =&gt; true,
</pre>

Basically we declare new ajax function for variable product. Now we need to add code of that function in same file. To do so <strong>go to line no - 273</strong>. At this line Add to Cart AJAX function is being completed. We will add - add to cart AJAX code for variable product now.

Please start adding below code from <strong>line no 274</strong>.

<pre>
public function add_to_cart_variable_rc() {
    $product_id = apply_filters( 'woocommerce_add_to_cart_product_id', absint( $_POST['product_id'] ) );
    $quantity = empty( $_POST['quantity'] ) ? 1 : apply_filters( 'woocommerce_stock_amount', $_POST['quantity'] );
    $variation_id = $_POST['variation_id'];
    $variation  = $_POST['variation'];
    $passed_validation = apply_filters( 'woocommerce_add_to_cart_validation', true, $product_id, $quantity );

    if ( $passed_validation &amp;&amp; WC()-&gt;cart-&gt;add_to_cart( $product_id, $quantity, $variation_id, $variation  ) ) {
        do_action( 'woocommerce_ajax_added_to_cart', $product_id );
        if ( get_option( 'woocommerce_cart_redirect_after_add' ) == 'yes' ) {
        wc_add_to_cart_message( $product_id );
    }

        // Return fragments
    $this-&gt;get_refreshed_fragments();
    } else {
        $this-&gt;json_headers();

        // If there was an error adding to the cart, redirect to the product page to show any errors
    $data = array(
        'error' =&gt; true,
        'product_url' =&gt; apply_filters( 'woocommerce_cart_redirect_after_error', get_permalink( $product_id ), $product_id )
        );
    echo json_encode( $data );
    }
    die();
}
</pre>

Above code will take request of our jQuery <code>add_to_cart_variable.js</code> and post it to <strong><em>default add to cart function</em></strong> of WooCommerce. Now we have to see that how our custom JavaScript will send data to our function. So if you look into our JS, the action is declared in <strong>Data array</strong>. It is a function name which we declare in our <code>class-wc-ajax.php</code> file.

I am done with everything. Please try to implement this code in your WooCommerce project and tel me your experience. If you have something in addition to - you can put a comment.