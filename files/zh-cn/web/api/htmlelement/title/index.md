---
title: HTMLElement.title
slug: Web/API/HTMLElement/title
translation_of: Web/API/HTMLElement/title
---
<p>{{ APIRef() }}</p>

<p><strong><code>HTMLElement.title</code></strong> 属性表示元素的 title。当鼠标移到节点上时，会以“工具提示”（tool tip）的弹出形式显示该属性的属性值文本。</p>

<p>如果一个节点没有 <code>title</code> 属性（attribute），默认继承其父节点的相应属性，父节点可能是从父节点的父节点继承，依此类推。</p>

<h2 id="Syntax">语法</h2>

<pre class="eval">var string = element.title;<em>
element.title</em> = <em>string</em>;
</pre>

<h2 id="Example">例子</h2>

<pre><code>const link = document.createElement('a');
link.innerText = '葡萄';
link.href = 'https://en.wikipedia.org/wiki/Grape';
link.title = '维基百科上对葡萄的描述';</code></pre>

<h2 id="浏览器兼容性">浏览器兼容性</h2>

{{Compat("api.HTMLElement.title")}}