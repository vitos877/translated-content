---
title: Date.prototype.setUTCSeconds()
slug: Web/JavaScript/Reference/Global_Objects/Date/setUTCSeconds
tags:
  - 日期
translation_of: Web/JavaScript/Reference/Global_Objects/Date/setUTCSeconds
---
<div>{{JSRef}}</div>

<p><code>此 <strong>setUTCSeconds()</strong></code> 方法为一个依据国际通用时间的特定日期设置秒数。</p>

<div>{{EmbedInteractiveExample("pages/js/date-setutcseconds.html")}}</div>



<h2 id="语法">语法</h2>

<pre class="syntaxbox"><code><var>dateObj</var>.setUTCSeconds(<var>secondsValue</var>[, <var>msValue</var>])</code></pre>

<h3 id="参数">参数</h3>

<dl>
 <dt><code>secondsValue</code></dt>
 <dd>一个在 0 到 59 之间的整数，表示秒数。</dd>
 <dt><code>msValue</code></dt>
 <dd>可选参数。一个 0 到 999 之间的数字，代表毫秒数。</dd>
</dl>

<h3 id="返回值">返回值</h3>

<p>一个毫秒数，表示从国际通用时间 1970 年 00:00:00 到设置的时间值之间的时间跨度。</p>

<h2 id="描述">描述</h2>

<p>如果你没有设置 msValue 参数的值， 那么返回的值来自{{jsxref("Date.prototype.getUTCMilliseconds()", "getUTCMilliseconds()")}} 方法。</p>

<p>如果你指定的值超出了范围，<code>setUTCSeconds()</code> 因此会更新{{jsxref("Date")}} 对象中 date 的相关信息 . 举个例子，如果你设置 secondsValue 为 100, {{jsxref("Date")}} 对象中的分钟数会增加 1， 并且秒数会变成 40.</p>

<h2 id="示例">示例</h2>

<h3 id="使用_setUTCSeconds()">使用 <code>setUTCSeconds()</code></h3>

<pre class="brush: js">var theBigDay = new Date();
theBigDay.setUTCSeconds(20);
</pre>

<h2 id="规范">规范</h2>

{{Specifications}}

<h2 id="浏览器兼容性">浏览器兼容性</h2>

<p>{{Compat}}</p>

<h2 id="另见">另见</h2>

<ul>
 <li>{{jsxref("Date.prototype.getUTCSeconds()")}}</li>
 <li>{{jsxref("Date.prototype.setSeconds()")}}</li>
</ul>