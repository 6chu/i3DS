<h2>
	2019/09/09 User Icon, Page Navigator, Home Page Layout
</h2>
<p>
	1. Change the membership icon from fa logout to fa user, which makes more sense. Detail:
</p>
<p>
	Change
</p>
<pre class="prettyprint lang-php">    &lt;?php if ( !(clean_gallery_get_option('hide_login_button')) ) { ?&gt;&lt;?php if (is_user_logged_in()) : ?&gt;&lt;a href="&lt;?php echo esc_url( wp_logout_url( get_permalink() ) ); ?&gt;" class="clean-gallery-social-icon-login" title="&lt;?php esc_attr_e( 'Logout', 'clean-gallery' ); ?&gt;" aria-label="&lt;?php esc_attr_e( 'Logout Button', 'clean-gallery' ); ?&gt;"&gt;&lt;i class="fa fa-sign-out" aria-hidden="true"&gt;&lt;/i&gt;&lt;/a&gt;&lt;?php else : ?&gt;&lt;a href="&lt;?php echo esc_url( wp_login_url( get_permalink() ) ); ?&gt;" class="clean-gallery-social-icon-login" title="&lt;?php esc_attr_e( 'Login / Register', 'clean-gallery' ); ?&gt;" aria-label="&lt;?php esc_attr_e( 'Login / Register Button', 'clean-gallery' ); ?&gt;"&gt;&lt;i class="fa fa-sign-in" aria-hidden="true"&gt;&lt;/i&gt;&lt;/a&gt;&lt;?php endif;?&gt;&lt;?php } ?&gt;</pre>
<p>
	into
</p>
<pre class="prettyprint lang-php">    &lt;?php if ( !(clean_gallery_get_option('hide_login_button')) ) { ?&gt;&lt;?php if (is_user_logged_in()) : ?&gt;&lt;a href="&lt;?php echo esc_url( wp_logout_url( get_permalink() ) ); ?&gt;" class="clean-gallery-social-icon-login" title="&lt;?php esc_attr_e( 'Logout', 'clean-gallery' ); ?&gt;" aria-label="&lt;?php esc_attr_e( 'Logout Button', 'clean-gallery' ); ?&gt;"&gt;&lt;i class="fa fa-user" aria-hidden="true"&gt;&lt;/i&gt;&lt;/a&gt;&lt;?php else : ?&gt;&lt;a href="&lt;?php echo esc_url( wp_login_url( get_permalink() ) ); ?&gt;" class="clean-gallery-social-icon-login" title="&lt;?php esc_attr_e( 'Login / Register', 'clean-gallery' ); ?&gt;" aria-label="&lt;?php esc_attr_e( 'Login / Register Button', 'clean-gallery' ); ?&gt;"&gt;&lt;i class="fa fa-user" aria-hidden="true"&gt;&lt;/i&gt;&lt;/a&gt;&lt;?php endif;?&gt;&lt;?php } ?&gt;</pre>
<p>
	<span style="font-size:10px;">Related File：</span><span style="font-size:10px;">social-buttons.php</span> 
</p>
<p>
	<span style="font-size:10px;">2. Cumstomized page navigator's CSS style:</span>
</p>
<p>
<pre class="prettyprint lang-css">/* LCP-PageNavi
-------------------------------------------------------------- */
.lcp_paginator{clear:both;float:center;}
.lcp_paginator a,.lcp_paginatorspan{text-decoration:none;background:#eeeeee !important;border:1px solid #dddddd !important;padding:6px;margin:2px;display:inline-block;color:#444444 !important;line-height:1;border-radius:2px;}
.lcp_paginator a:hover,.lcp_paginator a:focus,.lcp_paginator span.current{background:#dddddd !important;border:1px solid #cccccc !important;color:#000000 !important;}
.lcp_paginator span.current{font-weight:normal;background:#dddddd !important;border:1px solid #cccccc !important;color:#000000 !important;}
.lcp_paginator ul,li{list-style-type:none;}
.lcp_paginator li{float:left;text-align:center;line-height:49px}

/* lcp_catlist
-------------------------------------------------------------- */
.lcp_catlist a,.lcp_paginatorspan{text-decoration:none;font-size:12px;font-family:arial;}
.lcp_catlist a:hover,.lcp_catlist a a:focus,.lcp_catlist a span.current{color:#000000;}
.lcp_catlist ul,li{list-style-type:none;}
.lcp_catlist li{text-align:left;line-height:9px;}</pre>
</p>

<p>
	<span style="font-size:10px;">3. Change Home Post CSS style:</span>
</p>
<p>
	From
</p>
<p>
<pre class="prettyprint lang-css">.clean-gallery-postbox{height:293px;width:250px;margin:6px 25px 19px 3px;padding:0;border:0px solid #dddddd;overflow:hidden;position:relative;float:left;background-color:#ffffff;border-radius:10px;box-shadow:7px 6px 1px #002851;}
.clean-gallery-postbox:nth-of-type(3n+3){margin-right:0;}
.clean-gallery-postbox:nth-of-type(3n+1){clear:both;}
.clean-gallery-postbox .clean-gallery-postbox-title{width:248px;height:43px;color:#222222;font:normal bold 14px Domine,Arial,Helvetica,sans-serif;line-height:1.4;-webkit-transition-duration:2.5s ease-out;-moz-transition-duration:2.5s ease-out;-o-transition-duration:2.5s ease-out;transition-duration:2.5s ease-out;position:absolute;bottom:0;margin:0;padding:5px 5px 0;text-align:center;overflow:hidden;}
.clean-gallery-postbox .clean-gallery-postbox-title a{color:#222222;text-align:center;-webkit-transition:color .3s;-moz-transition:color .3s;-o-transition:color .3s;transition:color .3s;}
.clean-gallery-postbox .clean-gallery-postbox-title a:hover,.clean-gallery-postbox .clean-gallery-postbox-title a:focus{color:#888888;text-decoration:none;}
.clean-gallery-postbox .clean-gallery-single-post-date{margin-right:0;}</pre>
into
</p>
<p>
<pre class="prettyprint lang-css">.clean-gallery-postbox{width:250px;height:243px;margin:6px 25px 19px 3px;padding:0;border:0px solid #dddddd;overflow:hidden;position:relative;float:left;background-color:#ffffff;border-radius:10px;box-shadow:7px 6px 1px #002851;}
.clean-gallery-postbox:nth-of-type(3n+3){margin-right:0;}
.clean-gallery-postbox:nth-of-type(3n+1){clear:both;}
.clean-gallery-postbox .clean-gallery-postbox-title{width:248px;height:43px;color:#222222;font:normal bold 14px Domine,Arial,Helvetica,sans-serif;line-height:1.4;-webkit-transition-duration:2.5s ease-out;-moz-transition-duration:2.5s ease-out;-o-transition-duration:2.5s ease-out;transition-duration:2.5s ease-out;position:absolute;bottom:0;margin:0;padding:4px 5px 0;text-align:center;overflow:hidden;background-color:#FFF;}
.clean-gallery-postbox .clean-gallery-postbox-title a{color:#222222;text-align:center;-webkit-transition:color .3s;-moz-transition:color .3s;-o-transition:color .3s;transition:color .3s;}
.clean-gallery-postbox .clean-gallery-postbox-title a:hover,.clean-gallery-postbox .clean-gallery-postbox-title a:focus{color:#888888;text-decoration:none;}
.clean-gallery-postbox .clean-gallery-single-post-date{margin-right:0;}</pre>
</p>
