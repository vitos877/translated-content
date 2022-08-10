---
title: document.contentType
slug: Web/API/Document/contentType
translation_of: Web/API/Document/contentType
---
<p>{{ ApiRef() }}</p>
<h3 id="Summary">概述</h3>
<p>返回当前文档的 Content-Type(MIME) 类型。</p>
<h3 id="Syntax">语法</h3>
<pre class="eval"><var>contentType</var> = <var>document</var>.contentType;
</pre>
<p><code>该属性为只读。</code></p>
<h3 id="Notes">备注</h3>
<p>该属性的返回值是浏览器检测到的，不一定是直接读取 HTTP 响应头中的或者 HTML 中 meta 标签指定的值。</p>
<h3 id="Specification">规范</h3>
<p>非标准属性，仅<a href="/zh-cn/Gecko">Gecko</a>支持。</p>