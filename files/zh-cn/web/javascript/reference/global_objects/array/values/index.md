---
title: Array.prototype.values()
slug: Web/JavaScript/Reference/Global_Objects/Array/values
tags:
  - Array
  - ECMAScript 2015
  - Iterator
  - JavaScript
  - Prototype
  - 数组
  - 方法
  - 迭代
translation_of: Web/JavaScript/Reference/Global_Objects/Array/values
---
<div>{{JSRef}}</div>

<p><strong><code>values()</code></strong> 方法返回一个新的 <strong><code>Array Iterator</code></strong> 对象，该对象包含数组每个索引的值。</p>

<div>{{EmbedInteractiveExample("pages/js/array-values.html")}}</div>

<h2 id="语法">语法</h2>

<pre class="syntaxbox"><var>arr</var>.values()</pre>

<h3 id="返回值">返回值</h3>

<p>一个新的 {{jsxref("Array")}} 迭代对象。</p>

<h2 id="示例">示例</h2>

<h3 id="使用_for...of_循环进行迭代">使用 <code>for...of</code> 循环进行迭代</h3>

<pre class="brush: js">const arr = ['a', 'b', 'c', 'd', 'e'];
const iterator = arr.values();

for (let letter of iterator) {
  console.log(letter);
}  //"a" "b" "c" "d" "e"</pre>

<p><strong>Array.prototype.values</strong> 是 <strong>Array.prototype[Symbol.iterator] </strong>的默认实现。</p>

<pre class="brush: js">Array.prototype.values === Array.prototype[Symbol.iterator]  // true </pre>

<h3 id="使用_.next_迭代">使用 <code>.next()</code> 迭代</h3>

<pre class="brush: js">const arr = ['a', 'b', 'c', 'd', 'e'];
const iterator = arr.values();
iterator.next();               // Object { value: "a", done: false }
iterator.next().value;         // "b"
iterator.next()["value"];      // "c"
iterator.next();               // Object { value: "d", done: false }
iterator.next();               // Object { value: "e", done: false }
iterator.next();               // Object { value: undefined, done: true }
iterator.next().value;         // undefined</pre>

<div class="warning">
<p><strong>警告：</strong>数组迭代器是一次性的，或者说临时对象</p>
</div>

<p>例子：</p>

<pre class="brush: js">const arr = ['a', 'b', 'c', 'd', 'e'];
const iterator = arr.values();
for (let letter of iterator) {
  console.log(letter);
} //"a" "b" "c" "d" "e"
for (let letter of iterator) {
  console.log(letter);
} // undefined</pre>

<p><strong>解释：</strong>当 <code>next().done=true</code> 或 <code>currentIndex&gt;length</code> 时， <code>for..of</code> 循环结束。参见 <a href="/en-US/docs/Web/JavaScript/Reference/Iteration_protocols">Iteration protocols</a> 。</p>

<p><strong>值：</strong>数组迭代器中存储的是原数组的地址，而不是数组元素值。</p>

<pre class="brush: js">const arr = ['a', 'b', 'c', 'd', 'e'];
const iterator = arr.values();
console.log(iterator);        // Array Iterator {  }
iterator.next().value;        // "a"
arr[1] = 'n';
iterator.next().value;        // "n"
</pre>

<div class="note">
<p><strong>备注：</strong>如果数组中元素改变，那么迭代器的值也会改变</p>
</div>

<h2 id="规范">规范</h2>

{{Specifications}}

<h2 id="浏览器兼容性">浏览器兼容性</h2>



<p>{{Compat}}</p>

<h2 id="相关链接">相关链接</h2>

<ul>
 <li>{{jsxref("Array.prototype.keys()")}}</li>
 <li>{{jsxref("Array.prototype.entries()")}}</li>
 <li>{{jsxref("Array.prototype.forEach()")}}</li>
 <li>{{jsxref("Array.prototype.every()")}}</li>
 <li>{{jsxref("Array.prototype.some()")}}</li>
</ul>