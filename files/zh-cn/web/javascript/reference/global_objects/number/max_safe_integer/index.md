---
title: Number.MAX_SAFE_INTEGER
slug: Web/JavaScript/Reference/Global_Objects/Number/MAX_SAFE_INTEGER
translation_of: Web/JavaScript/Reference/Global_Objects/Number/MAX_SAFE_INTEGER
---
<div>{{JSRef}}</div>

<p><strong><code>Number.MAX_SAFE_INTEGER</code></strong> 常量表示在 JavaScript 中最大的安全整数（maxinum safe integer)（<code>2^53 - 1）。</code></p>

<div>{{js_property_attributes(0, 0, 0)}}</div>

<h2 id="描述">描述</h2>

<p><code>MAX_SAFE_INTEGER</code> 是一个值为 9007199254740991 的常量。因为 Javascript 的数字存储使用了 <a href="http://en.wikipedia.org/wiki/IEEE_floating_point">IEEE 754</a> 中规定的<a href="https://zh.wikipedia.org/zh-cn/%E9%9B%99%E7%B2%BE%E5%BA%A6%E6%B5%AE%E9%BB%9E%E6%95%B8">双精度浮点数</a>数据类型，而这一数据类型能够安全存储 <code>-(2^53 - 1)</code> 到 <code>2^53 - 1</code> 之间的数值（包含边界值）。</p>

<p>这里安全存储的意思是指能够准确区分两个不相同的值，例如 <code>Number.MAX_SAFE_INTEGER + 1 === Number.MAX_SAFE_INTEGER + 2</code> 将得到 true 的结果，而这在数学上是错误的，参考{{jsxref("Number.isSafeInteger()")}}获取更多信息。</p>

<p>由于 <code>MAX_SAFE_INTEGER 是</code>{{jsxref("Number")}}的一个<code>静态属性，所以你不用自己动手为</code>{{jsxref("Number")}}对象创建<code>Number.MAX_SAFE_INTEGER</code>这一属性，就可以直接使用它。</p>

<h2 id="示例">示例</h2>

<pre class="brush: js">Number.MAX_SAFE_INTEGER // 9007199254740991
Math.pow(2, 53) - 1     // 9007199254740991
</pre>

<h2 id="规范">规范</h2>

{{Specifications}}

<h2 id="浏览器兼容性">浏览器兼容性</h2>

{{Compat}}

<h2 id="相关链接">相关链接</h2>

<ul>
 <li>{{jsxref("Number.MIN_SAFE_INTEGER")}}</li>
 <li>{{jsxref("Number.isSafeInteger()")}}</li>
</ul>