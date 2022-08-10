---
title: WebSocket()
slug: Web/API/WebSocket/WebSocket
translation_of: Web/API/WebSocket/WebSocket
---
<p>{{APIRef("Web Sockets API")}}<br>
 <code><strong>WebSocket()</strong></code>构造函器会返回一个 {{domxref("WebSocket")}} 对象。</p>

<h2 id="语法">语法</h2>

<pre class="syntaxbox">var <em>aWebSocket</em> = new WebSocket(<em>url</em> [, protocols]);</pre>

<h3 id="参数">参数</h3>

<dl>
 <dt><code>url</code></dt>
 <dd>要连接的 URL；这应该是 WebSocket 服务器将响应的 URL。</dd>
 <dt><code>protocols</code> {{optional_inline}}</dt>
 <dd>一个协议字符串或者一个包含协议字符串的数组。这些字符串用于指定子协议，这样单个服务器可以实现多个 WebSocket 子协议（例如，您可能希望一台服务器能够根据指定的协议（<code>protocol</code>）处理不同类型的交互）。如果不指定协议字符串，则假定为空字符串。</dd>
</dl>

<h3 id="抛出异常">抛出异常</h3>

<dl>
 <dt><code>SECURITY_ERR</code></dt>
 <dd>正在尝试连接的端口被阻止。</dd>
</dl>

<h2 id="规范">规范</h2>

{{Specifications}}

<h2 id="浏览器兼容性">浏览器兼容性</h2>



<p>{{Compat("api.WebSocket.WebSocket")}}</p>