---
title: document.linkColor
slug: Web/API/Document/linkColor
translation_of: Web/API/Document/linkColor
---
<p>{{ ApiRef() }}</p>

<h3 id="Summary">概述</h3>

<p>{{ Deprecated_header() }} <code>linkColor</code> 用来获取和设置文档内链接元素 (&lt;a&gt;) 的颜色。</p>

<h3 id="Syntax">语法</h3>

<pre class="eval"><em>color</em> = document.linkColor
document.linkColor = <em>color</em>
</pre>

<h3 id="Parameters">参数</h3>

<ul>
 <li><code>color</code> 是一个代表颜色的字符串 (比如"red","blue"等),或者是一个 16 进制 rgb 颜色值 (比如"<code>#ff0000</code>").</li>
</ul>

<h3 id="Notes">备注</h3>

<p>在 Mozilla Firefox 中，该属性的默认值是 blue(<code>或者说是#0000ee</code> ).</p>

<p><code>document.linkColor</code>在 <a href="http://www.w3.org/TR/DOM-Level-2-HTML/html.html#ID-26809268">DOM Level 2 HTML 中已被废弃</a>.</p>

<p>替代方案是在链接元素上 <a href="/zh-cn/HTML/Element/a">HTML anchor (&lt;a&gt;) </a> 使用 css {{ Cssxref("color") }} 属性，(比如<code>a {color:red;}</code>) 或者 <code><a href="http://www.w3.org/TR/CSS21/selector.html#link-pseudo-classes">:link</a></code> 伪类 ,(比如<code>:link {color:red;}</code>).</p>

<p>另一种方法是使用 <code>document.body.link</code>, 该属也在<a href="http://www.w3.org/TR/html401/struct/global.html#adef-link">HTML 4.01</a>中被废弃。</p>

<h3 id="Example">例子</h3>

<pre class="eval">document.linkColor = "blue";
</pre>

<h3 id="Specification">规范</h3>

<p> </p>

<ul>
 <li>{{domxref("document.vlinkColor")}}</li>
 <li>{{domxref("document.alinkColor")}}</li>
</ul>