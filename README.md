<h2>
	<span style="font-family:Microsoft YaHei;">2019/09/09 网站维护记录</span> 
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
<h2>
	<span style="font-family:Microsoft YaHei;">2019/09/04 网站维护记录</span>
</h2>
<p>
	<span style="color:#5A5A5A;font-family:&quot;font-size:14px;background-color:#FFFFFF;">1、已修复注册时收不到验证邮件，导致无法注册的问题。重新开放了自由注册。</span><br />
<span style="color:#5A5A5A;font-family:&quot;font-size:14px;background-color:#FFFFFF;">2、评论框的'未登录提示'错位的问题。</span><br />
<span style="color:#5A5A5A;font-family:&quot;font-size:14px;background-color:#FFFFFF;">3、新增了 找游戏 功能。</span><br />
<span style="color:#5A5A5A;font-family:&quot;font-size:14px;background-color:#FFFFFF;">4、新增了 FAQ 和 关于本站 页面。</span><br />
<span style="color:#5A5A5A;font-family:&quot;font-size:14px;background-color:#FFFFFF;">5、对文章的阅读体验进行了一系列不可描述的优化。</span><span style="font-family:Microsoft YaHei;"></span>
</p>

