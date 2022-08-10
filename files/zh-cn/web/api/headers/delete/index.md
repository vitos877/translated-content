---
title: Headers.delete()
slug: Web/API/Headers/delete
translation_of: Web/API/Headers/delete
---
<p>{{APIRef("Fetch")}}{{ SeeCompatTable() }}</p>

<p><strong><code>delete()</code></strong> 方法可以从 Headers 对象中删除指定 header.</p>

<p>下列原因将会导致该方法抛出一个{{jsxref("TypeError")}}:</p>

<ul>
 <li>header 名在 HTTP header 中是不存在的。</li>
 <li>header 被锁定了.​</li>
</ul>

<div class="note">
<p><strong>Note:</strong>出于安全原因，部分头信息只能被用户代理控制。这些头信息包括 {{Glossary("Forbidden_header_name", "forbidden header names", 1)}}  和 {{Glossary("Forbidden_response_header_name", "forbidden response header names", 1)}}.</p>
</div>

<h2 id="语法">语法</h2>

<pre class="brush: js">myHeaders.delete(name);</pre>

<h3 id="Parameters">Parameters</h3>

<dl>
 <dt><em>name</em></dt>
 <dd>需删除的 HTTP header 名称。</dd>
</dl>

<h3 id="Returns">Returns</h3>

<p>Void.</p>

<h2 id="Example">Example</h2>

<p>创建一个空的 Headers 对象：</p>

<pre class="brush: js">var myHeaders = new Headers(); // Currently empty</pre>

<p>可以通过 append() 方法添加 header:</p>

<pre class="brush: js">myHeaders.append('Content-Type', 'image/jpeg');
myHeaders.get('Content-Type'); // Returns 'image/jpeg'
</pre>

<p>可以通过 delete() 方法删除已有 header:</p>

<pre class="brush: js">myHeaders.delete('Content-Type');
myHeaders.get('Content-Type'); // Returns null, as it has been deleted</pre>

<h2 id="Specifications">Specifications</h2>

{{Specifications}}

<h2 id="Browser_compatibility">Browser compatibility</h2>

{{Compat("api.Headers.delete")}}

<h2 id="See_also">See also</h2>

<ul>
 <li><a href="/en-US/docs/Web/API/ServiceWorker_API">ServiceWorker API</a></li>
 <li><a href="/en-US/docs/Web/HTTP/Access_control_CORS">HTTP access control (CORS)</a></li>
 <li><a href="/en-US/docs/Web/HTTP">HTTP</a></li>
</ul>