---
title: Error.prototype.columnNumber
slug: Web/JavaScript/Reference/Global_Objects/Error/columnNumber
translation_of: Web/JavaScript/Reference/Global_Objects/Error/columnNumber
---
<div>{{JSRef}} {{non-standard_header}}</div>

<p><code><strong>columnNumber</strong></code>属性包含引发此错误的文件行中的列号。</p>

<h2 id="例子">例子</h2>

<h3 id="使用_columnNumber">使用 <code>columnNumber</code></h3>

<pre class="brush: js">var e = new Error('Could not parse input');
throw e;
console.log(e.columnNumber) // 0
</pre>

<h2 id="规范">规范</h2>

{{Specifications}}

<h2 id="浏览器兼容性">浏览器兼容性</h2>

{{Compat}}

<h2 id="相关链接">相关链接</h2>

<ul>
 <li>{{jsxref("Error.prototype.stack")}} {{non-standard_inline}}</li>
 <li>{{jsxref("Error.prototype.lineNumber")}} {{non-standard_inline}}</li>
 <li>{{jsxref("Error.prototype.fileName")}} {{non-standard_inline}}</li>
</ul>