---
title: AbortSignal.onabort
slug: Web/API/AbortSignal/abort_event
tags:
  - API
  - Fetch
  - onabort
  - 事件处理
  - 属性
  - 测试
  - 终止属性
translation_of: Web/API/AbortSignal/onabort
original_slug: Web/API/AbortSignal/onabort
---
<div>{{APIRef("DOM")}}{{SeeCompatTable}}</div>

<div>当事件被{{event("abort_(cancellable_fetch)", "终止")}}，{{domxref("FetchSignal")}}接口的<strong><code>onabort</code></strong> 只读属性就会被调用。例子。当 fetch 的请求信号被终止。</div>

<h2 id="语法">语法</h2>

<pre class="brush: js">abortSignal.onabort = function() { ... };</pre>

<h2 id="示例">示例</h2>

<p>在下面例子中，我们将创建一个新的 <code>AbortController</code> 对象，并获取它的{{domxref("AbortSignal")}} (在 <code>signal</code> 属性中可用)。然后我们查看 <code>onabort</code> 属性是否被终止，并将相应的日志输出到控制台。</p>

<pre class="brush: js">var controller = new AbortController();
var signal = controller.signal;

signal.onabort = function() {
  console.log('Request aborted');
};
</pre>

<h2 id="规格">规格</h2>

{{Specifications}}

<h2 id="浏览器兼容性">浏览器兼容性</h2>



<p>{{Compat("api.AbortSignal.onabort")}}</p>

<h2 id="参考文档">参考文档</h2>

<ul>
 <li><a href="/en-US/docs/Web/API/Fetch_API">Fetch API</a></li>
</ul>