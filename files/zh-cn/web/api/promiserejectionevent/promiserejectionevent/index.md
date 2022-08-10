---
title: PromiseRejectionEvent.PromiseRejectionEvent()
slug: Web/API/PromiseRejectionEvent/PromiseRejectionEvent
translation_of: Web/API/PromiseRejectionEvent/PromiseRejectionEvent
---
<div>{{APIRef("HTML DOM")}}</div>

<p><code><strong>PromiseRejectionEvent()</strong></code> 构造器返回一个新创建的 {{domxref("PromiseRejectionEvent")}}，代表一个 JavaScript {{jsxref("Promise")}}被 rejected 时触发的事件。</p>

<h2 id="语法">语法</h2>

<pre class="syntaxbox">new PromiseRejectionEvent(<em>type</em>, {
  promise: <em>somePromise</em>,
  reason : <em>someValue</em>
});
</pre>

<h3 id="参数">参数</h3>

<p><em><code>PromiseRejectionEvent()</code> 构造函数继承了 {{domxref("Event.Event", "Event()")}}的参数。</em></p>

<dl>
 <dt><code>type</code></dt>
 <dd>一个代表 PromiseRejectionEvent 的类型名称的字符串。这是区分大小写的同时必须是{{event("rejectionhandled", '"rejectionhandled"')}} 或者 {{event("unhandledrejection", '"unhandledrejection"')}} 其中之一。</dd>
 <dt><code>promise</code></dt>
 <dd>代表被 rejected 的{{jsxref("Promise")}}。</dd>
 <dt><code>reason</code></dt>
 <dd>代表 promise 被 rejected 的原因的值或者对象{{jsxref("Object")}} 。</dd>
</dl>

<h2 id="例子">例子</h2>

<pre class="brush: js">var myRejectionEvent = new PromiseRejectionEvent('unhandledrejection', {
  promise : myPromise,
  reason : 'My house is on fire'
});</pre>

<h2 id="规范">规范</h2>

{{Specifications}}

<h2 id="浏览器兼容性">浏览器兼容性</h2>

{{Compat("api.PromiseRejectionEvent.PromiseRejectionEvent")}}

<h2 id="另请参阅">另请参阅</h2>

<ul>
 <li>{{jsxref("Promise")}}</li>
 <li>{{domxref("PromiseRejectionEvent")}}</li>
</ul>