---
title: 303 See Other
slug: Web/HTTP/Status/303
translation_of: Web/HTTP/Status/303
---
<div>{{HTTPSidebar}}</div>

<p>HTTP <strong>303 See Other</strong> 重定向状态码，通常作为 {{HTTPMethod("PUT")}} 或 {{HTTPMethod("POST")}} 操作的返回结果，它表示重定向链接指向的不是新上传的资源，而是另外一个页面，比如消息确认页面或上传进度页面。而请求重定向页面的方法要总是使用 {{HTTPMethod("GET")}}。</p>

<h2 id="状态">状态</h2>

<pre class="syntaxbox">303 See Other</pre>

<h2 id="规范">规范</h2>

{{Specifications}}

<h2 id="浏览器兼容性">浏览器兼容性</h2>

<p>{{Compat}}</p>

<h2 id="更多可见">更多可见</h2>

<ul>
 <li>{{HTTPStatus("302")}} <code>Found</code>, the temporary redirect</li>
</ul>