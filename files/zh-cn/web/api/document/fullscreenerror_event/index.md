---
title: Document.onfullscreenerror
slug: Web/API/Document/fullscreenerror_event
translation_of: Web/API/Document/onfullscreenerror
original_slug: Web/API/Document/onfullscreenerror
---
<div>{{ApiRef("Fullscreen API")}}</div>

<p>Document.onfullscreenerror 属性是一个事件处理器用于处理 {{event("fullscreenchange")}} 事件，在当前文档不能进入全屏模式，即使它被请求时触发。</p>

<h2 id="语法">语法</h2>

<pre class="syntaxbox"><var>targetDocument</var>.onfullscreenerror = <var>fullscreenErrorHandler</var>;
</pre>

<h2 id="示例">示例</h2>

<pre class="brush: js">document.onfullscreenerror = function ( event ) {
  console.log("FULL SCREEN DENIED")
};

// requestFullscreen() 将会失败，因为它在事件处理器之外
document.documentElement.requestFullscreen();
</pre>

<h2 id="规范">规范</h2>

{{Specifications}}

<h2 id="浏览器兼容性">浏览器兼容性</h2>

{{Compat("api.Document.fullscreenerror_event")}}

<h2 id="相关文章">相关文章</h2>

<ul>
 <li>{{event("fullscreenerror")}}</li>
 <li>{{domxref("Document.onfullscreenchange")}}</li>
</ul>