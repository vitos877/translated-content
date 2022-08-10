---
title: FileReader.abort()
slug: Web/API/FileReader/abort
translation_of: Web/API/FileReader/abort
---
<p>{{APIRef("File API")}}</p>

<p>该方法可以取消 FileReader 的读取操作，触发之后 {{domxref("FileReader.readyState","readyState")}} 为已完成（DONE）。</p>

<h2 id="语法">语法</h2>

<pre class="syntaxbox"><em>instanceOfFileReader</em>.abort();</pre>

<h3 id="例外情况">例外情况</h3>

<dl>
 <dt><code>DOM_FILE_ABORT_ERR</code></dt>
 <dd>对一个没有正在进行读取操作（{{domxref("FileReader.readyState","readyState")}} 不是<code>LOADING</code>）的 FileReader 进行 abort 操作，会抛出 <code>DOM_FILE_ABORT_ERR 错误。</code></dd>
</dl>

<h2 id="规范">规范</h2>

{{Specifications}}

<h2 id="浏览器兼容性">浏览器兼容性</h2>

{{Compat("api.FileReader.abort")}}

<h2 id="相关链接">相关链接</h2>

<ul>
 <li>{{domxref("FileReader")}}</li>
</ul>