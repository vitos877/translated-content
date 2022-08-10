---
title: 故：在 CORS 头 Access-Control-Allow-Credentials 中预期为 true
slug: Web/HTTP/CORS/Errors/CORSMIssingAllowCredentials
translation_of: Web/HTTP/CORS/Errors/CORSMIssingAllowCredentials
original_slug: Web/HTTP/CORS/Errors/CORS 错误允许凭证
---


<h2 id="理由">理由</h2>

<pre class="syntaxbox notranslate">故：在 CORS 头 Access-Control-Allow-Credentials 中预期设为 true</pre>

<h2 id="错在了哪儿？">错在了哪儿？</h2>

<p>     CORS 请求要求服务器允许使用凭据，但是服务器的 HTTPHeader：Access-Control-Allow-Credentials 标头的值并没有设置为 true 。</p>

<p>想要在客户端解决此问题，请修改代码以不请求使用凭据：</p>

<ul>
 <li>如果要使用 {{domxref("XMLHttpRequest")}} 发出请求，请确保没有将 {{domxref("XMLHttpRequest.withCredentials", "withCredentials")}} 设置为 true。</li>
 <li>如果使用 <a href="/zh-CN/docs/Web/API/Server-sent_events">Server-sent events</a>，请确保{{domxref("EventSource.withCredentials")}}为 false（default）。</li>
 <li>如果使用 <a href="/zh-CN/docs/Web/API/Fetch_API">Fetch API</a>，请确保{{domxref("Request.credentials")}}为“omit”。</li>
</ul>

<p>想要通过更改服务器的配置来消除此错误，请调整服务器的配置以将 Access-Control-Allow-Credentials 标头的值设置为 true。</p>

<h2 id="更多">更多</h2>

<ul>
 <li><a href="/en-US/docs/Web/HTTP/CORS/Errors">CORS errors</a></li>
 <li>Glossary: {{Glossary("CORS")}}</li>
 <li><a href="/en-US/docs/Web/HTTP/CORS">CORS introduction</a></li>
</ul>