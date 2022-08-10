---
title: WebGLRenderingContext.deleteFramebuffer()
slug: Web/API/WebGLRenderingContext/deleteFramebuffer
translation_of: Web/API/WebGLRenderingContext/deleteFramebuffer
---
<div>{{APIRef("WebGL")}}</div>

<p><a href="/en-US/docs/Web/API/WebGL_API">WebGL API</a> 的 <strong><code>WebGLRenderingContext.deleteFramebuffer()</code></strong> 方法用来删除给定的{{domxref("WebGLFramebuffer")}} 对象。如果帧缓冲区已被删除，则此方法无效。.</p>

<h2 id="语法">语法</h2>

<pre class="syntaxbox">void <var>gl</var>.deleteFramebuffer(<var>framebuffer</var>);
</pre>

<h3 id="参数">参数</h3>

<dl>
 <dt>framebuffer</dt>
 <dd> 将要删除的{{domxref("WebGLFramebuffer")}} 对象。</dd>
</dl>

<h3 id="返回值">返回值</h3>

<p>None.</p>

<h2 id="示例">示例</h2>

<h3 id="删除一个帧缓冲区">删除一个帧缓冲区</h3>

<pre class="brush: js">var canvas = document.getElementById('canvas');
var gl = canvas.getContext('webgl');
var framebuffer = gl.createFramebuffer();

// ...

gl.deleteFramebuffer(framebuffer);</pre>

<h2 id="规范">规范</h2>

{{Specifications}}

<h2 id="浏览器兼容性">浏览器兼容性</h2>

<p>{{Compat("api.WebGLRenderingContext.deleteFramebuffer")}}</p>

<h2 id="另见">另见</h2>

<ul>
 <li>{{domxref("WebGLRenderingContext.bindFramebuffer()")}}</li>
 <li>{{domxref("WebGLRenderingContext.createFramebuffer()")}}</li>
 <li>{{domxref("WebGLRenderingContext.isFramebuffer()")}}</li>
 <li>Other buffers: {{domxref("WebGLBuffer")}}, {{domxref("WebGLRenderbuffer")}}</li>
</ul>