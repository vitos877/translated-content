---
title: WeakMap.prototype.delete()
slug: Web/JavaScript/Reference/Global_Objects/WeakMap/delete
translation_of: Web/JavaScript/Reference/Global_Objects/WeakMap/delete
---
<div>{{JSRef("Global_Objects", "WeakMap")}}</div>

<h2 id="Summary">概述</h2>

<p><code><strong>delete()</strong></code> 方法可以从一个 <code>WeakMap</code> 对象中删除指定的元素。</p>

<h2 id="Syntax">语法</h2>

<pre class="syntaxbox"><code><em>wm</em>.delete(key);</code></pre>

<h3 id="Parameters参数">Parameters 参数</h3>

<dl>
 <dt>key</dt>
 <dd>需要删除的元素的键</dd>
</dl>

<h3 id="返回值">返回值</h3>

<p>如果成功删除，返回 <code>true</code>，否则返回 <code>false</code>。</p>

<h2 id="Examples">示例</h2>

<pre class="brush: js;">var wm = new WeakMap();
wm.set(window, "foo");

wm.delete(window); // 返回 true，表示删除成功。

wm.has(window);    // 返回 false，因为 window 对象已经被删除了。
</pre>

<h2 id="规范">规范</h2>

{{Specifications}}

<h2 id="浏览器兼容性">浏览器兼容性</h2>

{{Compat}}

<h2 id="相关链接">相关链接</h2>

<ul>
 <li>{{jsxref("WeakMap")}}</li>
</ul>