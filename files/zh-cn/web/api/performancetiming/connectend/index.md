---
title: PerformanceTiming.connectEnd
slug: Web/API/PerformanceTiming/connectEnd
translation_of: Web/API/PerformanceTiming/connectEnd
---
<p>{{APIRef("Navigation Timing")}}</p>

<h2 id="Summary">Summary</h2>

<p><strong><code>PerformanceTiming.connectEnd</code></strong> 这个只读属性返回一个无符号长整型，它以毫秒为单位，代表了网络链接建立的时间节点。如果传输层报告了错误或者链接又被重新建立，则采用最后一次链接建立的时间。如果链接是长久的，那么这个值等同于{{domxref("PerformanceTiming.fetchStart")}}。链接被认为打开以所有的链接握手，SOCKS 认证结束为标志。</p>

<h2 id="Syntax">Syntax</h2>

<pre class="syntaxbox"><em>time</em> = <em>performanceTiming</em>.connectEnd;</pre>

<h2 id="规范">规范</h2>

<p>因为 <a href="https://w3c.github.io/navigation-timing/#obsolete">Navigation Timing 规范</a>已被弃用，此特性不再有望成为标准。请使用 {{domxref("PerformanceNavigationTiming")}} 接口代替。</p>

<h2 id="浏览器兼容性">浏览器兼容性</h2>

{{Compat}}

<h2 id="See_also">See also</h2>

<ul>
 <li>参见 {{domxref("PerformanceTiming")}} 接口。</li>
</ul>