---
title: Window.scrollByLines()
slug: Web/API/Window/scrollByLines
tags:
  - API
  - DOM
  - Method
  - Non-standard
  - Window
  - 方法
  - 非标准
translation_of: Web/API/Window/scrollByLines
---
<p> </p>

<div>{{ ApiRef() }}</div>

<div>
<p>{{Non-standard_header}}</p>
</div>

<h2 id="Summary">概要</h2>

<p>按给定的行数滚动文档。</p>

<h2 id="Syntax">语法</h2>

<pre class="syntaxbox">window.scrollByLines(<var>lines</var>)
</pre>

<h2 id="Parameters">参数</h2>

<ul>
 <li><code>lines</code> 要滚动的行数。</li>
 <li><code>lines</code> 可以是正整数，也可以是负整数。</li>
</ul>

<h2 id="Example">例子</h2>

<pre class="brush:html">&lt;!-- 向下滚动 5 行。 --&gt;
&lt;button onclick="scrollByLines(5);"&gt;down 5 lines&lt;/button&gt;
</pre>

<pre class="brush:html">&lt;!-- 向上滚动 5 行。 --&gt;
&lt;button onclick="scrollByLines(-5);"&gt;up 5 lines&lt;/button&gt;
</pre>

<h2 id="Specification">规范</h2>

<p>这不是任何规范的一部分。</p>

<h2 id="See_also">参考</h2>

<ul>
 <li>{{domxref("window.scrollBy")}}, {{domxref("window.scrollByPages")}}</li>
</ul>