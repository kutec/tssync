---
ID: 3942
post_title: How to Duplicate Content in WordPress
author: Guest Author
post_date: 2015-08-03 20:47:43
post_excerpt: >
  Not all the content on your WordPress
  website may be unique, as there will be
  a few posts and pages in the site with a
  repetitive pattern. This article will
  focus on how you can manage duplicate
  content in WordPress.
layout: post
permalink: >
  http://teckstack.com/duplicate-wordpress-content
published: true
dsq_thread_id:
  - "4000244534"
feedweb_post_sort_value:
  - "-2"
ac_is_copyprotect:
  - "1"
ac_is_advanced_tracking:
  - "1"
ac_postid:
  - 7Yz3xn5RnZf.text
ac_is_process:
  - "1"
ac_embedid:
  - 1sRqXtr9l3W
vortex_system_likes:
  - "0"
vortex_system_dislikes:
  - "0"
---
<blockquote>Not all the content on your WordPress website may be unique, as there will be a few posts and pages in the site with a repetitive pattern. In such a case, you'll likely have to make a lot of coping and pasting. Besides, having a copy of page and/or post makes the process of creating multiple posts and pages with similar content (except for titles and a part of content) much easier. This saves you from recreating the same content for each post/page.</blockquote>

What's more? When you're running a <a href="http://teckstack.com/wordpress">WordPress</a> powered online store, you'll probably want to use the same information to be displayed for your long list of products. And so, duplicating the data on the posts/pages will make the task of presenting similar content less difficult for you. Fortunately, there are a few WordPress plugins that makes the task of duplicating posts and/or posts easier for editors; and thus, spare them from copying and pasting the text manually from one post/page to another.

In this post, we'll be discussing about two of the most popular WordPress plugins that enables to copy and paste a page or post without much hassle, namely: Clone Posts and Duplicate Post.

<h2>Clone Posts <small>Plugin</small></h2>

The <a href="https://wordpress.org/plugins/clone-posts/" target="_blank" rel="nofollow">Clone Posts WordPress</a> plugin is an ideal choice for website owners who just want to have a clone of their page or post, without any fluff. In simple words, this plugin lets you create a clone of a WordPress website page and posts, but it doesn't come with an options page. You just need to install this plugin, and you're good to go.When using this plugin, a "Clone" link will be added to all your website post, page, and custom post on the index pages. Whenever that link is clicked, the items on the page/post will be copied and saved as a draft.

<em>Note: Since the copy of the content is kept as a part of drafts in the back-end, you don't have to worry about displaying duplicate data on the front end.</em>

<h2>Duplicate Post <small>Plugin</small></h2>

In case, you want to have more options other than the simple copy and paste operation, then you can opt for the <a href="https://wordpress.org/plugins/duplicate-post/other_notes/" target="_blank" rel="nofollow">Duplicate Post plugin</a>. This plugin provides a complete solution to meet your needs of duplicating the posts or pages compared to the “Clone Posts” plugin. Simply put, it's not just clone your pages and posts on the index pages, but also while displaying them in the editing page or post screen respectively. The Duplicate Post plugin can be used in two different ways to duplicate a post/post:
<img class=" size-full wp-image-3948 alignright" src="http://teckstack.com/tsdir/wp-content/uploads/2015/08/Pic-2.png" alt="Duplicate Content in WordPress 1" width="248" height="221" />You can choose to click the link named “Copy to a new draft” on the post/page editing screen (as shown in the image below). Doing so, a duplicate copy of the post/page will be opened in a new edit screen.

Note: The "Copy to a new draft" link can be added to the "Publish" section when you're editing a page. Also, it can be added directly to the front end in the admin bar, while you're viewing a page/post on the site.

Simply duplicate any page or post, by navigating to Pages → All Pages (or Posts → All Posts) and hover over the page or post title that needs to be duplicated, and you'll be able to see 2 links “Clone” and “New Draft”, as follows:
<img class=" wp-image-3949 size-full alignleft" src="http://teckstack.com/tsdir/wp-content/uploads/2015/08/Pic-3.png" alt="Duplicate Content in WordPress 2" width="1024" height="139" />

When you'll click on the “Clone” button, it will simply copy your page or post but won't open it. On the other hand, clicking on the “New Draft” option will not just copy your page/post, but will also open it on the edit screen.Once you've chosen any one of the above discussed options to duplicate your pages/post, you can even fine-tune the Duplicate Post plugin's behavior – from the settings page in your WordPress site admin dashboard screen. For instance, instead of merely copying the post/page, you can use the settings to copy the blog post's editorial status, attachments and many other things.

<h2>Code Your Own</h2>

If you've good coding skills and don't want to make use of the WordPress plugins to duplicate your site posts, then below is a code snippet that will help you achieve the same objective with ease:

<pre class="lang:default decode:true">/*
 * Function for creating a duplicate post
 */
function duplicate_an_post(){
    global $wpdb;
    if (! isset( $_POST['post']) || ( isset( $_GET['post'])  || ( isset($_REQUEST['action']) &amp;&amp; 'duplicate_an_post' == $_REQUEST['action'] ) ) ) {
        wp_die('nothing action for creating duplicate post!');
    }
 
    /*
     * post id of real post
     */
    $real_post_id = (isset($_POST['post']) ? $_POST['post'] : $_GET['post']);
    /*
     * data of real post
     */
    $real_post = get_post( $real_post_id );
    /*
     * create the post duplicate, if post data exists
     */
    if (isset( $real_post ) &amp;&amp; $real_post != null) {
 
        $args = array(
            'post_title'     =&gt; $real_post-&gt;post_title,
            'post_type'      =&gt; $real_post-&gt;post_type,
            'to_ping'        =&gt; $real_post-&gt;to_ping,
            'menu_order'     =&gt; $real_post-&gt;menu_order,
            'post_content'   =&gt; $real_post-&gt;post_content,
            'post_excerpt'   =&gt; $real_post-&gt;post_excerpt,
            'post_name'      =&gt; $real_post-&gt;post_name,
            'post_parent'    =&gt; $real_post-&gt;post_parent,
            'post_password'  =&gt; $real_post-&gt;post_password,
            'post_status'    =&gt; 'draft',
            'comment_status' =&gt; $real_post-&gt;comment_status,
            'ping_status'    =&gt; $real_post-&gt;ping_status,
            'post_author'    =&gt; $new_post_author
            
        );
 
        $new_id = wp_insert_post( $args );
 
        /*
         * duplicate all post meta
         */
        $real_meta_infos = $wpdb-&gt;get_results("SELECT meta_key, meta_value FROM $wpdb-&gt;postmeta WHERE post_id=$real_post_id");
        if (count($real_meta_infos)!=0) {
            $sql_query = "INSERT INTO $wpdb-&gt;postmeta (post_id, meta_key, meta_value) ";
            foreach ($real_meta_infos as $meta_detail) {
                $meta_key = $meta_detail-&gt;meta_key;
                $meta_value = addslashes($meta_detail-&gt;meta_value);
                $sql_query_sel[]= "SELECT $new_id, '$meta_key', '$meta_value'";
            }
            $meta_query.= implode(" UNION ALL ", $sql_query_sel);
            $wpdb-&gt;query($meta_query);
        }
  
        /*
         * At last, open edit post screen as a new draft
         */
        wp_redirect( admin_url( 'post.php?action=edit&amp;post=' . $new_id ) );
        exit;
    } else {
        wp_die('Process failed, Please try again');
    }
}
add_action( 'admin_action_duplicate_an_post', 'duplicate_an_post' );
 
/*
 * Add link for create the duplicate post
 */
function create_option( $actions, $post ) {
    if (current_user_can('edit_posts')) {
        $actions['duplicate'] = '<a title="Create duplicate post" href="admin.php?action=duplicate_an_post&amp;post=' . $post-&gt;ID . '" rel="permalink">Duplicate</a>';
    }
    return $actions;
}
 
add_filter( 'post_row_actions', 'create_option', 10, 2 );</pre>

Add the above code in your theme <strong>functions.php</strong> file (or any other file). After executing this code, a Duplicate link will get added to your posts. Clicking this link will create a clone of your posts and will them as drafts.

<h4><strong>Conclusion</strong></h4>

If you're an editor of a WordPress site, and would like to duplicate some pages and/or posts of the site, reading this post will provide you understanding of the different ways to meet your needs.

<div class="panel panel-info">
<div class="panel-body">This is a guest post by <a href="mailto:sophiaphill15@gmail.com?subject=teckstack.com">Sophia Phillips</a>. She is an expert frond-end &amp; WordPress developer. Currently, she is employed with WordPrax Ltd.- a leading <a title="PSD to Wordpress" href="http://www.wordprax.com/services/psd-to-wordpress">PSD Design to WordPress theme</a> converter company. Sophia has had written a remarkable number of articles on WordPress tricks and tips.</div>
</div>