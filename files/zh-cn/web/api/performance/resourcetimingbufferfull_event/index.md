---
title: Performance.onresourcetimingbufferfull
slug: Web/API/Performance/resourcetimingbufferfull_event
translation_of: Web/API/Performance/onresourcetimingbufferfull
original_slug: Web/API/Performance/onresourcetimingbufferfull
---
<div>{{APIRef("Resource Timing API")}}</div>

<p><strong><code>onresourcetimingbufferfull</code></strong> 属性是一个在{{event("resourcetimingbufferfull")}}事件触发时会被调用的 {{domxref("EventHandler","event handler")}} 。这个事件当浏览器的资源时间性能缓冲区已满时会触发。</p>

<h2 id="Syntax">语法</h2>

<pre class="syntaxbox">callback = <em>performance</em>.onresourcetimingbufferfull = buffer_full_cb;
</pre>

<h3 id="Return_Value">返回值</h3>

<dl>
 <dt>callback</dt>
 <dd>一个当{{event("resourcetimingbufferfull")}} 事件触发时调用的{{event("Event_handlers", "event handler")}} 。</dd>
</dl>

<h2 id="例子">例子</h2>

<p>下面的示例在 <code>onresourcetimingbufferfull</code> 属性上设置一个回调函数。</p>

<pre class="brush: js">function buffer_full(event) {
  console.log("WARNING: Resource Timing Buffer is FULL!");
  performance.setResourceTimingBufferSize(200);
}
function init() {
  // Set a callback if the resource buffer becomes filled
  performance.onresourcetimingbufferfull = buffer_full;
}
&lt;body onload="init()"&gt;
</pre>

<h2 id="规范">规范</h2>

{{Specifications}}

<h2 id="浏览器兼容性">浏览器兼容性</h2>

{{Compat("api.Performance.onresourcetimingbufferfull")}}

<h2 id="参见">参见</h2>

<ul>
 <li>{{event("resourcetimingbufferfull")}} event</li>
 <li>{{domxref("Performance.clearResourceTimings","Performance.clearResourceTimings()")}}</li>
 <li>{{domxref("Performance.setResourceTimingBufferSize","Performance.setResourceTimingBufferSize()")}}</li>
</ul>