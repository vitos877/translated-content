---
title: Document.exitPointerLock()
slug: Web/API/Document/exitPointerLock
translation_of: Web/API/Document/exitPointerLock
---
<p>{{ apiref("DOM") }}</p>

<p>{{ seeCompatTable }}</p>

<p><code>exitPointerLock</code> 方法可异步的解锁鼠标（通过{{domxref("Element.requestPointerLock")}}锁定的）。</p>

<p>追踪是否解锁成功，需要监听{{event("pointerlockchange")}} 和{{event("pointerlockerror")}} 事件。</p>

<h2 id="Syntax">语法</h2>

<pre class="eval">document.exitPointerLock();
</pre>

<h2 id="规范">规范</h2>

{{Specifications}}

<h2 id="Browser_compatibility">浏览器兼容性</h2>

{{Compat("api.Document.exitPointerLock")}}

<h2 id="参见">参见</h2>

<ul>
 <li>{{ domxref("Document.pointerLockElement") }}</li>
 <li>{{ domxref("Element.requestPointerLock()") }}</li>
 <li><a href="/en-US/docs/WebAPI/Pointer_Lock">Pointer Lock</a></li>
</ul>