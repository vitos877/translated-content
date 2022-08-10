---
title: URL.toString()
slug: Web/API/URL/toString
tags:
  - API
  - URL
  - 参考
  - 字符串
  - 方法
translation_of: Web/API/URL/toString
---
<div>{{ApiRef("URL API")}}</div>

<p><strong><code>URL.toString()</code></strong> 字符串化方法返回一个包含完整 URL 的 {{domxref("USVString")}}。它的作用等同于只读的 {{domxref("URL.href")}}。</p>

<p>{{AvailableInWorkers}}</p>

<h2 id="语法">语法</h2>

<pre class="syntaxbox"><em>string</em> = <em>url</em>.toString();</pre>

<h3 id="参数">参数</h3>

<p>无。</p>

<h3 id="返回值">返回值</h3>

<p>一个{{domxref("USVString")}}。</p>

<h2 id="参考">参考</h2>

<pre class="brush: js">const url = new URL("https://developer.mozilla.org/en-US/docs/Web/API/URL/toString");
url.toString() // 应当返回字符串形式的 URL
</pre>

<h2 id="规范">规范</h2>

{{Specifications}}

<h2 id="浏览器兼容性">浏览器兼容性</h2>



<p>{{Compat("api.URL.toString")}}</p>

<h2 id="参见">参见</h2>

<ul>
 <li>父级接口 {{domxref("URL")}}。</li>
</ul>