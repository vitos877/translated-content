---
title: SameSite cookies
slug: Web/HTTP/Headers/Set-Cookie/SameSite
translation_of: Web/HTTP/Headers/Set-Cookie/SameSite
---


<p><strong><code>SameSite</code></strong> 是 HTTP 响应头 {{HTTPHeader("Set-Cookie")}} 的属性之一。它允许您声明该 Cookie 是否仅限于第一方或者同一站点上下文。</p>

<h2 id="值">值</h2>

<p> <code>SameSite</code> 接受下面三个值：</p>

<h3 id="Lax"><code>Lax</code></h3>

<p>Cookies 允许与顶级导航一起发送，并将与第三方网站发起的 GET 请求一起发送。这是浏览器中的默认值。</p>

<h3 id="Strict"><code>Strict</code></h3>

<p>Cookies 只会在第一方上下文中发送，不会与第三方网站发起的请求一起发送。</p>

<h3 id="None"><code>None</code></h3>

<p>Cookie 将在所有上下文中发送，即允许跨站发送。</p>

<p>以前 <code>None</code> 是默认值，但最近的浏览器版本将 <code>Lax</code> 作为默认值，以便对某些类型的跨站请求伪造（{{Glossary("CSRF")}}）攻击具有相当强的防御能力。</p>

<p>使用 <code>None</code> 时，需在最新的浏览器版本中使用 <a href="/zh-CN/docs/Web/HTTP/Headers/Set-Cookie"><code>Secure</code></a> 属性。更多信息见下文。</p>

<h2 id="针对常见警告信息的解决办法">针对常见警告信息的解决办法</h2>

<h3 id="SameSiteNone_需要_Secure"><code>SameSite=None</code> 需要 <code>Secure</code></h3>

<p>如果没有设置 <code>Secure</code> 属性，控制台中可能会出现以下警告：</p>

<blockquote>
<p>Some cookies are misusing the “sameSite“ attribute, so it won’t work as expected.<br>
 Cookie “<em>myCookie</em>” rejected because it has the “sameSite=none” attribute but is missing the “secure” attribute.</p>
</blockquote>

<p>出现此警告是因为需要 <code>SameSite=None</code> 但未标记 <code>Secure</code> 的任何 cookie 都将被拒绝。</p>

<pre class="example-bad notranslate">Set-Cookie: flavor=choco; SameSite=None</pre>

<p>要解决此问题，必须将 <code>Secure</code> 属性添加到 <code>SameSite=None</code> cookies 中。</p>

<pre class="example-good notranslate">Set-Cookie: flavor=choco; SameSite=None; <strong>Secure</strong></pre>

<p><a href="/zh-CN/docs/Web/HTTP/Headers/Set-Cookie"><code>Secure</code></a> cookie 仅通过 HTTPS 协议加密发送到服务器。请注意，不安全站点（<code>http:</code>）无法使用 <code>Secure</code> 指令设置 cookies。</p>

<h3 id="没有_SameSite_属性的Cookies默认为_SameSiteLax">没有 <code>SameSite</code> 属性的 Cookies 默认为 <code>SameSite=Lax</code></h3>

<p>最新版本的现代浏览器为 cookies 的 <code>SameSite</code> 提供了更安全的默认值，因此控制台中可能会显示以下消息：</p>

<blockquote>
<p>Some cookies are misusing the “sameSite“ attribute, so it won’t work as expected.<br>
 Cookie “<em>myCookie</em>” has “sameSite” policy set to “lax” because it is missing a “sameSite” attribute, and “sameSite=lax” is the default value for this attribute.</p>
</blockquote>

<p>出现警告是因为未显式指定 cookie 的 <code>SameSite</code> 属性：</p>

<pre class="example-bad notranslate">Set-Cookie: flavor=choco</pre>

<p>虽然您可以依赖现代浏览器自动应用 <code>SameSite=Lax</code>，但您应该显式地指定它，以便清楚地传达您的意图，即要如何将 <code>SameSite</code> 属性应用到您的 cookie。这也将改善跨浏览器的体验，因为并不是所有浏览器都默认为 <code>Lax</code>。</p>

<pre class="example-good notranslate">Set-Cookie: flavor=choco; <strong>SameSite=Lax</strong></pre>

<h2 id="示例"><strong>示例</strong></h2>

<pre class="notranslate">RewriteEngine on
RewriteBase "/"
RewriteCond "%{HTTP_HOST}"       "^example\.org$" [NC]
RewriteRule "^(.*)"              "https://www.example.org/index.html" [R=301,L,QSA]
RewriteRule "^(.*)\.ht$"         "index.php?nav=$1 [NC,L,QSA,CO=RewriteRule;01;https://www.example.org;30/;SameSite=None;Secure]
RewriteRule "^(.*)\.htm$"        "index.php?nav=$1 [NC,L,QSA,CO=RewriteRule;02;https://www.example.org;30/;SameSite=None;Secure]
RewriteRule "^(.*)\.html$"       "index.php?nav=$1 [NC,L,QSA,CO=RewriteRule;03;https://www.example.org;30/;SameSite=None;Secure]
[...]
RewriteRule "^admin/(.*)\.html$" "admin/index.php?nav=$1 [NC,L,QSA,CO=RewriteRule;09;https://www.example.org:30/;SameSite=Strict;Secure]
</pre>

<h2 id="规范">规范</h2>

{{Specifications}}

<h2 id="浏览器兼容性">浏览器兼容性</h2>

<p>{{Compat}}</p>

<h2 id="另请参阅">另请参阅</h2>

<ul>
 <li><a href="/en-US/docs/Web/HTTP/Cookies">HTTP cookies</a></li>
 <li>{{HTTPHeader("Cookie")}}</li>
 <li>{{domxref("Document.cookie")}}</li>
</ul>