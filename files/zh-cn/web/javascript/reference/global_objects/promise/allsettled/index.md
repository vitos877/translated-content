---
title: Promise.allSettled()
slug: Web/JavaScript/Reference/Global_Objects/Promise/allSettled
tags:
  - Promise
  - Promise.allSettled
  - promise.all
translation_of: Web/JavaScript/Reference/Global_Objects/Promise/allSettled
---
<p>{{JSRef}}</p>

<p>该<code><strong>Promise.allSettled()</strong></code>方法返回一个在所有给定的 promise 都已经<code>fulfilled</code>或<code>rejected</code>后的 promise，并带有一个对象数组，每个对象表示对应的 promise 结果。</p>

<p>当您有多个彼此不依赖的异步任务成功完成时，或者您总是想知道每个<code>promise</code>的结果时，通常使用它。</p>

<p>相比之下，<code><a href="https://developer.mozilla.org/zh-CN/docs/Web/JavaScript/Reference/Global_Objects/Promise/all">Promise.all()</a></code> 更适合彼此相互依赖或者在其中任何一个<code>reject</code>时立即结束。</p>

<div>{{EmbedInteractiveExample("pages/js/promise-allsettled.html")}}</div>

<h2 id="句法">句法</h2>

<pre><em>Promise</em>.allSettled(<em>iterable</em>);</pre>

<h3 id="参数">参数</h3>

<dl>
 <dt><code>iterable</code></dt>
 <dd>一个<a href="/zh-CN/docs/Web/JavaScript/Guide/iterable">可迭代的</a>对象，例如{{jsxref("Array")}}，其中每个成员都是<code>Promise</code>。</dd>
</dl>

<h3 id="返回值">返回值</h3>

<p>一旦所指定的 promises 集合中每一个 promise 已经完成，无论是成功的达成或被拒绝，<strong>未决议的</strong> {{jsxref("Promise")}}将被<strong>异步</strong>完成。那时，所返回的 promise 的处理器将传入一个数组作为输入，该数组包含原始 promises 集中每个 promise 的结果。</p>

<p>对于每个结果对象，都有一个 <code>status</code> 字符串。如果它的值为 <code>fulfilled</code>，则结果对象上存在一个 <code>value</code> 。如果值为 <code>rejected</code>，则存在一个 <code>reason</code> 。value（或 reason ）反映了每个 promise 决议（或拒绝）的值。</p>

<h2 id="规范">规范</h2>

{{Specifications}}

<h2 id="浏览器兼容性">浏览器兼容性</h2>

<p>{{Compat}}</p>

<h2 id="参见">参见</h2>

<ul>
 <li>
<a href="/zh-CN/docs/Archive/Add-ons/Techniques/Promises">Promises</a></li>
 <li>
<a href="/zh-CN/docs/Web/JavaScript/Guide/Using_promises">Using promises</a></li>
 <li>
<a href="/zh-CN/docs/Learn/JavaScript/Asynchronous/Promises">Graceful asynchronous programming with promises</a></li>
 <li>{{jsxref("Promise")}}</li>
 <li>{{jsxref("Promise.all()")}}</li>
</ul>