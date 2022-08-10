---
title: Date.prototype.getUTCDate()
slug: Web/JavaScript/Reference/Global_Objects/Date/getUTCDate
translation_of: Web/JavaScript/Reference/Global_Objects/Date/getUTCDate
---
<div>{{JSRef("Global_Objects", "Date")}}</div>

<p><strong><code>getUTCDate()</code></strong> 方法以世界时为标准，返回一个指定的日期对象为一个月中的第几天</p>

<div>{{EmbedInteractiveExample("pages/js/date-getutcdate.html")}}</div>

<h2 id="Syntax">语法</h2>

<pre class="syntaxbox"><code><var>dateObj</var>.getUTCDate()</code></pre>

<h3 id="Parameters">参数</h3>

<p>无</p>

<h3 id="Returns">返回值</h3>

<p><code>getUTCDate()</code> 返回一个 1 到 31 的整数值</p>

<h2 id="Examples">例子</h2>

<h3 id="Example:_Using_getUTCDate">例子：使用 <code>getUTCDate()</code> 方法</h3>

<p>下面的例子是把当前日期的天数部分赋值给变量 <code>day</code>.</p>

<pre class="brush: js">var today = new Date();
var day = today.getUTCDate();
</pre>

<h2 id="规范">规范</h2>

{{Specifications}}

<h2 id="浏览器兼容性">浏览器兼容性</h2>

<div>
<p>{{Compat}}</p>
</div>

<h2 id="See_also">相关链接</h2>

<ul>
 <li>{{jsxref("Date.prototype.getDate()")}}</li>
 <li>{{jsxref("Date.prototype.getUTCDay()")}}</li>
 <li>{{jsxref("Date.prototype.setUTCDate()")}}</li>
</ul>