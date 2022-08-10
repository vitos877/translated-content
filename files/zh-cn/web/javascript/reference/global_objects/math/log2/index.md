---
title: Math.log2()
slug: Web/JavaScript/Reference/Global_Objects/Math/log2
translation_of: Web/JavaScript/Reference/Global_Objects/Math/log2
---
<div>
<div>{{JSRef("Global_Objects", "Math")}}</div>
</div>

<h2 id="Summary">概述</h2>

<p><code><strong>Math.log2()</strong></code> 函数返回一个数字以 2 为底的对数。</p>

<h2 id="Syntax">语法</h2>

<pre class="syntaxbox"><code>Math.log2(<em>x</em>)</code></pre>

<h3 id="Parameters">参数</h3>

<dl>
 <dt><code>x</code></dt>
 <dd>任意数字。</dd>
</dl>

<h2 id="Description">描述</h2>

<p>如果传入的参数小于 0，则返回 <code>NaN</code>.</p>

<h2 id="Examples">示例</h2>

<pre class="brush:js">Math.log2(2)     // 1
Math.log2(1024)  // 10
Math.log2(1)     // 0
Math.log2(0)     // -Infinity
Math.log2(-2)    // NaN
Math.log2("1024")// 10
Math.log2("foo") // NaN
</pre>

<h2 id="规范">规范</h2>

{{Specifications}}

<h2 id="浏览器兼容性">浏览器兼容性</h2>

{{Compat}}

<h2 id="See_also">相关链接</h2>

<ul>
 <li>{{jsxref("Global_Objects/Math", "Math")}} 对象。</li>
</ul>