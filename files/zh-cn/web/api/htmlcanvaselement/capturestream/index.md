---
title: HTMLCanvasElement.captureStream()
slug: Web/API/HTMLCanvasElement/captureStream
translation_of: Web/API/HTMLCanvasElement/captureStream
original_slug: Web/API/HTMLCanvasElement/捕获流
---
<div>{{APIRef("Media Capture and Streams")}}{{SeeCompatTable}}</div>

<p>该 <code><strong>HTMLCanvasElement</strong></code><strong><code>.captureStream()</code></strong> 方法返回的 {{domxref("CanvasCaptureMediaStream")}} 是一个实时视频捕获的画布。</p>

<h2 id="语法">语法</h2>

<pre class="syntaxbox"><var>MediaStream</var> = <var>canvas</var>.captureStream(<var>frameRate</var>);
</pre>

<h3 id="参数">参数</h3>

<dl>
 <dt><code>frameRate</code> 可选</dt>
 <dd>设置双精准度浮点值为每个帧的捕获速率。如果未设置，则每次画布更改时都会捕获一个新帧。如果设置为<code>0</code>，则会捕获单个帧。</dd>
</dl>

<h3 id="返回值">返回值</h3>

<p>对一个 {{domxref("MediaStream")}} 对象的引用。</p>

<h2 id="例子">例子</h2>

<pre class="brush: js"><code>//</code>获取所需要截取媒体流的 canvas element
var canvasElt = document.querySelector('canvas');

//<code>截取到媒体流</code>
var stream = canvasElt.captureStream(25); // 25 FPS

//使用媒体流
// E.g.使用 RTCPeerConnection 来传输给其它的电脑
// 下面的 pc 是其他地方创建的一个 RTCPeerConnection
pc.addStream(stream);
</pre>

<h2 id="规范">规范</h2>

{{Specifications}}

<h2 id="浏览器兼容性">浏览器兼容性</h2>

{{Compat("api.HTMLCanvasElement.captureStream")}}

<h2 id="看看其他">看看其他</h2>

<ul>
 <li>{{domxref("CanvasCaptureMediaStream")}},所属接口。</li>
 <li>{{domxref("HTMLMediaElement.captureStream()")}}, 允许从一个媒体中获取流</li>
 <li>{{domxref("MediaStream")}}</li>
 <li>{{domxref("Media Capture and Streams API")}}</li>
</ul>