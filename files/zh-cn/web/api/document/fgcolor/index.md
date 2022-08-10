---
title: document.fgColor
slug: Web/API/Document/fgColor
translation_of: Web/API/Document/fgColor
---
<p>{{ ApiRef() }}</p>

<h3 id="Summary">概述</h3>

<p>{{ Deprecated_header() }} <code>fgColor</code> 属性用来获取或设置当前文档的前景色或者文本颜色。</p>

<h3 id="Syntax">语法</h3>

<pre class="eval">  var <em>color</em> = document.fgColor;
  document.fgColor = <em>color;</em>
</pre>

<h3 id="Parameters">参数</h3>

<ul>
 <li><code>color</code> 是一个颜色值，可以为一个颜色类型，比如"red",或者一个 16 进制 RGB 值，比如 "<code>#ff0000</code>".</li>
</ul>

<h3 id="Example">例子</h3>

<pre class="eval">document.fgColor = "white";
document.bgColor = "darkblue";
</pre>

<h3 id="Notes">备注</h3>

<p>在 Mozilla Firefox 中，该属性的默认值是黑色.(<code>black 或者#000000</code>).</p>

<p><code>document.fgColor</code> 属性已经在<a href="http://www.w3.org/TR/DOM-Level-2-HTML/html.html#ID-26809268">DOM Level 2</a>中被废弃。推荐使用的<code>css</code>属性为{{ Cssxref("color") }} (用法为 <code>document.body.style.color = "red"</code>).</p>

<p>另外一个类似的属性是 <code>document.body.text</code>, 该属性也在 <a href="http://www.w3.org/TR/html401/struct/global.html#adef-text">HTML 4.01</a> 中被废弃，推荐使用 CSS 属性。</p>

<h3 id="Specification">规范</h3>

<p>{{Compat("api.Document.fgColor")}}</p>