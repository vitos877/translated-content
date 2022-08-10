---
title: Atomics.load()
slug: Web/JavaScript/Reference/Global_Objects/Atomics/load
translation_of: Web/JavaScript/Reference/Global_Objects/Atomics/load
---
<div>{{JSRef}}</div>

<p>静态方法 <code><strong>Atomics</strong></code><strong><code>.load()</code></strong> 返回一个数组当中给定位置的值。</p>

<div>{{EmbedInteractiveExample("pages/js/atomics-load.html")}}</div>



<h2 id="语法">语法</h2>

<pre class="syntaxbox">Atomics.load(typedArray, index)
</pre>

<h3 id="参数">参数</h3>

<dl>
 <dt><code>typedArray</code></dt>
 <dd>一个共享的整型数组。可以是 {{jsxref("Int8Array")}}，{{jsxref("Uint8Array")}}，{{jsxref("Int16Array")}}，{{jsxref("Uint16Array")}}，{{jsxref("Int32Array")}} 或 {{jsxref("Uint32Array")}}.</dd>
 <dt><code>index</code></dt>
 <dd>在 <code>typedArray</code> 中需要加载的位置。</dd>
</dl>

<h3 id="返回值">返回值</h3>

<p>给定位置的值 (<code>typedArray[index]</code>)。</p>

<h3 id="异常">异常</h3>

<ul>
 <li>抛出 {{jsxref("TypeError")}}, 如果 <code>typedArray</code> 不是一个被允许的整型。</li>
 <li>抛出 {{jsxref("TypeError")}}, 如果 <code>typedArray</code> 不是一个共享数组。</li>
 <li>抛出 {{jsxref("RangeError")}}, 如果 <code>index</code> 超出 <code>typedArray</code> 的界限。</li>
</ul>

<h2 id="示例">示例</h2>

<pre class="brush: js">var sab = new SharedArrayBuffer(1024);
var ta = new Uint8Array(sab);

Atomics.add(ta, 0, 12);
Atomics.load(ta, 0); // 12</pre>

<h2 id="规范">规范</h2>

{{Specifications}}

<h2 id="浏览器兼容性">浏览器兼容性</h2>

<p>{{Compat}}</p>

<h2 id="参阅">参阅</h2>

<ul>
 <li>{{jsxref("Atomics")}}</li>
 <li>{{jsxref("Atomics.store()")}}</li>
</ul>