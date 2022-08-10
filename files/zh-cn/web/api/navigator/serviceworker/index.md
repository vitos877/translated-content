---
title: Navigator.serviceWorker
slug: Web/API/Navigator/serviceWorker
translation_of: Web/API/Navigator/serviceWorker
---
<p>{{APIRef("Service Workers API")}}</p>

<p><code><strong>Navigator.serviceWorker</strong></code> 只读属性，返回 <a href="https://html.spec.whatwg.org/multipage/browsers.html#concept-document-window">关联文件</a> 的 {{domxref("ServiceWorkerContainer")}} 对象，它提供对{{domxref("ServiceWorker")}} 的注册，删除，升级和通信的访问。。</p>

<h2 id="语法">语法</h2>

<pre class="syntaxbox">let workerContainerInstance = navigator.serviceWorker;
</pre>

<h3 id="值">值</h3>

<p>{{domxref("ServiceWorkerContainer")}}.</p>

<h2 id="规范">规范</h2>

{{Specifications}}

<h2 id="浏览器兼容性">浏览器兼容性</h2>

{{Compat("api.Navigator.serviceWorker")}}

<h2 id="也可以看看">也可以看看</h2>

<ul>
 <li><a href="/en-US/docs/Web/API/ServiceWorker_API">ServiceWorker API</a></li>
 <li><a href="/en-US/docs/Web/API/ServiceWorker_API/Using_Service_Workers">Using Service Workers</a></li>
</ul>