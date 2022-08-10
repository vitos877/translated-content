---
title: HTMLHyperlinkElementUtils.search
slug: Web/API/HTMLAnchorElement/search
tags:
  - HTMLHyperlinkElementUtils.search
translation_of: Web/API/HTMLHyperlinkElementUtils/search
original_slug: Web/API/HTMLHyperlinkElementUtils/search
---
<p>{{ApiRef("URL API")}}</p>

<p><strong><code>HTMLHyperlinkElementUtils.search</code></strong> 属性是一个搜索字符串，也叫做查询字符串， 它是一个 {{domxref("USVString")}} ，包含 <code>'?'</code> 和随后的 URL 参数。</p>

<h2 id="语法">语法</h2>

<pre class="syntaxbox"><em>string</em> = <em>object</em>.search;
<em>object</em>.search = <em>string</em>;
</pre>

<h2 id="示例">示例</h2>

<pre class="brush: js">// 让一个
// &lt;a id="myAnchor" href="https://developer.mozilla.org/en-US/docs/HTMLHyperlinkElementUtils.search?q=123" /&gt;
//  元素在文档里

let anchor = document.getElementById("myAnchor");
let result = anchor.search;
// 返回:'?q=123'
</pre>

<h2 id="规范">规范</h2>

{{Specifications}}

<h2 id="浏览器兼容性">浏览器兼容性</h2>

{{Compat("api.HTMLAnchorElement.search")}}

<h2 id="相关链接">相关链接</h2>

<ul>
 <li>它属于{{domxref("HTMLHyperlinkElementUtils")}} mixin 。</li>
</ul>