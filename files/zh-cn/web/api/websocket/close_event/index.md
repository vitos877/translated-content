---
title: WebSocket.onclose
slug: Web/API/WebSocket/close_event
translation_of: Web/API/WebSocket/onclose
original_slug: Web/API/WebSocket/onclose
---
<p>{{APIRef("Web Sockets API")}}</p>

<p><strong><code>WebSocket.onclose</code></strong> 属性返回一个事件监听器，这个事件监听器将在 WebSocket 连接的{{domxref("WebSocket.readyState","readyState")}} 变为 <code>CLOSED</code>时被调用，它接收一个名字为“close”的 {{domxref("CloseEvent")}} 事件。</p>

<h2 id="语法">语法</h2>

<pre class="syntaxbox"><em>WebSocket</em>.onclose = function(event) {
  console.log("WebSocket is closed now.");
};</pre>

<h2 id="值">值</h2>

<p>一个{{domxref("EventListener")}}.</p>

<h2 id="规范">规范</h2>

{{Specifications}}