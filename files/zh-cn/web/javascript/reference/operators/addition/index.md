---
title: 相加运算符 (+)
slug: Web/JavaScript/Reference/Operators/Addition
translation_of: Web/JavaScript/Reference/Operators/Addition
original_slug: Web/JavaScript/Reference/Operators/相加
---
<div>{{jsSidebar("相加运算符")}}</div>

<p>相加运算符 (<code>+</code>) 用于对两个操作数进行相加运算，如果操作数中有一方为字符串，则该运算符将两个操作数连接成一个字符串。</p>

<div>{{EmbedInteractiveExample("pages/js/expressions-addition.html")}}</div>

<h2 id="语法">语法</h2>

<pre class="brush: js">x + y
</pre>

<h2 id="示例">示例</h2>

<h3 id="数字的相加运算">数字的相加运算</h3>

<pre class="brush: js">// Number + Number -&gt; addition
1 + 2 // 3

// Boolean + Number -&gt; addition
true + 1 // 2

// Boolean + Boolean -&gt; addition
false + false // 0
</pre>

<h3 id="字符串相加运算">字符串相加运算</h3>

<pre class="brush: js">// String + String -&gt; concatenation
'foo' + 'bar' // "foobar"

// Number + String -&gt; concatenation
5 + 'foo' // "5foo"

// String + Boolean -&gt; concatenation
'foo' + false // "foofalse"</pre>

<h2 id="规范">规范</h2>

{{Specifications}}

<h2 id="浏览器兼容性">浏览器兼容性</h2>

<p>{{Compat}}</p>

<h2 id="参考">参考</h2>

<ul>
 <li><a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/Subtraction">Subtraction operator</a></li>
 <li><a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/Division">Division operator</a></li>
 <li><a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/Multiplication">Multiplication operator</a></li>
 <li><a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/Remainder">Remainder operator</a></li>
 <li><a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/Exponentiation">Exponentiation operator</a></li>
 <li><a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/Increment">Increment operator</a></li>
 <li><a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/Decrement">Decrement operator</a></li>
 <li><a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/Unary_negation">Unary negation operator</a></li>
 <li><a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/Unary_plus">Unary plus operator</a></li>
</ul>