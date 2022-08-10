---
title: Array.length
slug: Web/JavaScript/Reference/Global_Objects/Array/length
tags:
  - JavaScript
  - 参考
  - 属性
  - 数组
translation_of: Web/JavaScript/Reference/Global_Objects/Array/length
---
<p>{{JSRef}}</p>

<p><code><strong>length</strong></code> 是 <code>Array</code> 的实例属性。返回或设置一个数组中的元素个数。该值是一个无符号 32-bit 整数，并且总是大于数组最高项的下标。</p>

<div>{{EmbedInteractiveExample("pages/js/array-length.html")}}</div>

<h2 id="Description">描述</h2>

<p><code>length</code> 属性的值是一个 0 到 2^32 - 1 的整数。</p>

<pre class="brush: js">const listA = [1, 2, 3];
const listB = new Array(6);

console.log(listA.length);
// 3

console.log(listB.length);
// 6

listB.length = 4294967296; // 2 的 32 次方 = 4294967296
// RangeError: Invalid array length

const listC = new Array(-100) // 负数
// RangeError: Invalid array length
</pre>

<p>你可以设置 <code>length</code> 属性的值来截断任何数组。当通过改变 <code>length</code> 属性值来扩展数组时，实际元素的数目将会增加。例如：将一个拥有 2 个元素的数组的 <code>length</code> 属性值设为 3 时，那么这个数组将会包含 3 个元素，并且，第三个元素是不可迭代的空槽。</p>

<pre class="brush: js">const arr = [1, 2];
console.log(arr);
// [ 1, 2 ]

arr.length = 5; // set array length to 5 while currently 2.
console.log(arr);
// [ 1, 2, <3 empty items> ]
    
arr.forEach(element => console.log(element));
// 1
// 2
</pre>

<p>但是，<code>length</code> 属性不一定表示数组中定义值的个数。了解更多：<a href="/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array#Relationship_between_length_and_numerical_properties">长度与数值下标属性之间的关系</a>。</p>

<p>{{js_property_attributes(1, 0, 0)}}</p>

<ul>
 <li><code>Writable</code>：如果设置为 <code>false</code>，该属性值将不能被修改。</li>
 <li><code>Configurable</code>：如果设置为 <code>false</code>，删除或更改任何属性都将会失败。</li>
 <li><code>Enumerable</code>：如果设置为 <code>true</code>，属性可以通过迭代器<a href="zh-CN/docs/Web/JavaScript/Reference/Statements/for">for</a>或<a href="/zh-CN/docs/Web/JavaScript/Reference/Statements/for...in">for...in</a>进行迭代。</li>
</ul>

<h2 id="Examples">示例 </h2>

<h3 id="Example:_Iterating_over_an_array">遍历数组</h3>

<p>下面的例子中，通过数组下标遍历数组元素，并把每个元素的值修改为原值的 2 倍。</p>

<pre class="brush: js">const numbers = [1, 2, 3, 4, 5];
const length = numbers.length;
for (var i = 0; i &lt; length; i++) {
  numbers[i] *= 2;
}
// 遍历后的结果 [2, 4, 6, 8, 10]</pre>

<h3 id="Example:_Shortening_an_array">截断数组</h3>

<p>下面的例子中，如果数组长度大于 3，则把该数组的长度截断为 3。</p>

<pre class="brush: js">const numbers = [1, 2, 3, 4, 5];

if (numbers.length &gt; 3) {
  numbers.length = 3;
}

console.log(numbers); // [1, 2, 3]
console.log(numbers.length); // 3</pre>

<h2 id="规范">规范</h2>

{{Specifications}}

<h2 id="浏览器兼容性">浏览器兼容性</h2>

<p>{{Compat}}</p>

<h2 id="相关链接">相关链接</h2>

<ul>
 <li>{{jsxref("Array")}}</li>
</ul>