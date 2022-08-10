---
title: Document.head
slug: Web/API/Document/head
translation_of: Web/API/Document/head
---
<p>{{APIRef}}</p>
<h2 id="Summary">概述</h2>
<p>返回当前文档中的 {{ HTMLElement("head") }} 元素。如果有多个 <code>&lt;head&gt;</code> 元素，则返回第一个。</p>
<h2 id="Syntax">语法</h2>
<pre class="syntaxbox"><em>var objRef</em> = document.head;
</pre>
<h2 id="Example">示例</h2>
<pre class="brush: js">// HTML 部分源码为: &lt;head id="my-document-head"&gt;
var aHead = document.head;

alert(aHead.id); // "my-document-head";

alert( document.head === document.querySelector("head") ); // true
</pre>
<h2 id="Example">附注</h2>
<p><code>document.head</code> 是个只读属性，为该属性赋值只会静默失败，如果在严格模式中，则会抛出<code>TypeError</code>异常。</p>
<h2 id="浏览器兼容性">浏览器兼容性</h2>
<div>
{{Compat("api.Document.head")}}

<h2 id="Specification">规范</h2>
<ul>
 <li><a href="http://www.w3.org/TR/html5/dom.html#dom-tree-accessors">HTML5: DOM Tree Accessors</a></li>
</ul>