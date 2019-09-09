<h2>
	<span style="font-family:Microsoft YaHei;">2019/09/09 网站维护记录</span>
</h2>
<p>
	替换了右上角的注册/登陆图标，之前无论登陆与否都一直显示登出标识，现在直接显示会员图标。具体：
</p>
<p>
	将
</p>
<pre class="prettyprint lang-php">    &lt;?php if ( !(clean_gallery_get_option('hide_login_button')) ) { ?&gt;&lt;?php if (is_user_logged_in()) : ?&gt;&lt;a href="&lt;?php echo esc_url( wp_logout_url( get_permalink() ) ); ?&gt;" class="clean-gallery-social-icon-login" title="&lt;?php esc_attr_e( 'Logout', 'clean-gallery' ); ?&gt;" aria-label="&lt;?php esc_attr_e( 'Logout Button', 'clean-gallery' ); ?&gt;"&gt;&lt;i class="fa fa-sign-out" aria-hidden="true"&gt;&lt;/i&gt;&lt;/a&gt;&lt;?php else : ?&gt;&lt;a href="&lt;?php echo esc_url( wp_login_url( get_permalink() ) ); ?&gt;" class="clean-gallery-social-icon-login" title="&lt;?php esc_attr_e( 'Login / Register', 'clean-gallery' ); ?&gt;" aria-label="&lt;?php esc_attr_e( 'Login / Register Button', 'clean-gallery' ); ?&gt;"&gt;&lt;i class="fa fa-sign-in" aria-hidden="true"&gt;&lt;/i&gt;&lt;/a&gt;&lt;?php endif;?&gt;&lt;?php } ?&gt;</pre>
<p>
	替换成
</p>
<pre class="prettyprint lang-php">    &lt;?php if ( !(clean_gallery_get_option('hide_login_button')) ) { ?&gt;&lt;?php if (is_user_logged_in()) : ?&gt;&lt;a href="&lt;?php echo esc_url( wp_logout_url( get_permalink() ) ); ?&gt;" class="clean-gallery-social-icon-login" title="&lt;?php esc_attr_e( 'Logout', 'clean-gallery' ); ?&gt;" aria-label="&lt;?php esc_attr_e( 'Logout Button', 'clean-gallery' ); ?&gt;"&gt;&lt;i class="fa fa-user" aria-hidden="true"&gt;&lt;/i&gt;&lt;/a&gt;&lt;?php else : ?&gt;&lt;a href="&lt;?php echo esc_url( wp_login_url( get_permalink() ) ); ?&gt;" class="clean-gallery-social-icon-login" title="&lt;?php esc_attr_e( 'Login / Register', 'clean-gallery' ); ?&gt;" aria-label="&lt;?php esc_attr_e( 'Login / Register Button', 'clean-gallery' ); ?&gt;"&gt;&lt;i class="fa fa-user" aria-hidden="true"&gt;&lt;/i&gt;&lt;/a&gt;&lt;?php endif;?&gt;&lt;?php } ?&gt;</pre>
</pre>
<p>
	<span style="font-size:10px;">相关文件：</span><span style="font-size:10px;">social-buttons.php</span>
</p>
<p>
	<br />
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

