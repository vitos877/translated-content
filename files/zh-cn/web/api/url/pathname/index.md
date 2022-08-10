---
title: URL.pathname
slug: Web/API/URL/pathname
tags:
  - API
  - URL
  - pathname
translation_of: Web/API/URL/pathname
---
<div>{{ApiRef("URL API")}}</div>

<p>{{domxref("URL")}}接口的<strong><code>pathname</code></strong>属性是一个{{domxref("USVString")}}，包含一个初始 <code>'/'</code> 和 URL 的路径 (如果没有路径，则为空字符串)</p>

<p>{{AvailableInWorkers}}</p>

<h2 id="语法">语法</h2>

<pre class="syntaxbox"><em>string</em> = <em>object</em>.pathname;
<em>object</em>.pathname = <em>string</em>;
</pre>

<h3 id="值">值</h3>

<p>一个{{domxref("USVString")}}.</p>

<h2 id="例子">例子</h2>

<pre class="brush: js">var url = new URL('https://developer.mozilla.org/en-US/docs/Web/API/URL/pathname');
var result = url.pathname; // Returns:"/en-US/docs/Web/API/URL/pathname"
</pre>

<h2 id="规范">规范</h2>

{{Specifications}}

<h2 id="浏览器兼容性">浏览器兼容性</h2>



<p>{{Compat("api.URL.pathname")}}</p>

<h2 id="参考">参考</h2>

<ul>
 <li>它所属的{{domxref("URL")}}接口。</li>
</ul>