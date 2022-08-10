---
title: FileReader.readAsArrayBuffer()
slug: Web/API/FileReader/readAsArrayBuffer
translation_of: Web/API/FileReader/readAsArrayBuffer
---
<p>{{APIRef("File API")}}</p>

<p>{{domxref("FileReader")}} 接口提供的 <strong><code>readAsArrayBuffer()</code></strong> 方法用于启动读取指定的 {{domxref("Blob")}} 或 {{domxref("File")}} 内容。当读取操作完成时，{{domxref("FileReader.readyState","readyState")}} 变成 <code>DONE</code>（已完成），并触发 {{event("loadend")}} 事件，同时 {{domxref("FileReader.result","result")}} 属性中将包含一个 {{domxref("ArrayBuffer")}} 对象以表示所读取文件的数据。</p>

<h2 id="语法">语法</h2>

<pre class="syntaxbox"><em>instanceOfFileReader</em>.readAsArrayBuffer(<em>blob</em>);</pre>

<h3 id="参数">参数</h3>

<dl>
 <dt><code>blob</code></dt>
 <dd>即将被读取的 {{domxref("Blob")}} 或 {{domxref("File")}} 对象。</dd>
</dl>

<h2 id="规范">规范</h2>

{{Specifications}}

<h2 id="浏览器兼容性">浏览器兼容性</h2>

{{Compat("api.FileReader.readAsArrayBuffer")}}

<h2 id="相关链接">相关链接</h2>

<ul>
 <li>{{domxref("FileReader")}}</li>
</ul>