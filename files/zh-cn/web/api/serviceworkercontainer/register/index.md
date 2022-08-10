---
title: ServiceWorkerContainer.register()
slug: Web/API/ServiceWorkerContainer/register
tags:
  - ServiceWorkerContainer.register()
translation_of: Web/API/ServiceWorkerContainer/register
---
<p>{{SeeCompatTable}}{{APIRef("Service Workers API")}}</p>

<p>{{domxref("ServiceWorkerContainer")}} 接口的 <strong><code>register()</code></strong>方法创建或更新一个给定 scriptURL 的<code><a href="/zh-CN/docs/Web/API/ServiceWorkerRegistration">ServiceWorkerRegistration</a></code>。</p>

<p>如果成功，一个服务工作者注册将提供的脚本 URL 与一个范围进行关联，后者用于导航匹配。如果该方法无法返回一个 <code>ServiceWorkerRegistration</code>，则返回一个 <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Promise"><code>Promise</code></a>。</p>

<p>您可以从受控页无条件调用此方法， 即，您不需要首先检查是否有一个有效的注册。</p>

<h2 id="语法">语法</h2>

<pre class="brush: js">ServiceWorkerContainer.register(scriptURL, options)
    .then(
        function(ServiceWorkerRegistration) {
            // do something
        }
);</pre>

<h3 id="参数">参数</h3>

<dl>
 <dt><code>scriptURL</code></dt>
 <dd>service worker 脚本的 URL.</dd>
 <dt><code>options</code> <code>{{optional_inline}}</code></dt>
 <dd>注册时提供选项的配置对象。 目前可用的选项包括：
 <ul>
  <li><code>scope</code>: 一个 {{domxref("USVString")}}，表示定义 service worker 注册范围的 URL ；service worker 可以控制的 URL 范围。通常是相对 URL。默认值是基于当前的 location，并以此来解析传入的路径。</li>
 </ul>
 </dd>
</dl>

<h3 id="返回">返回</h3>

<p>返回一个 {{domxref("Promise")}} 对象， 值是 {{domxref("ServiceWorkerRegistration")}} .</p>

<h2 id="示例">示例</h2>

<pre class="brush: js">if ('serviceWorker' in navigator) {
  navigator.serviceWorker.register('service-worker.js', {scope: './'})
  .then(function(registration) {
    document.querySelector('#status').textContent = 'succeeded';
  }).catch(function(error) {
    document.querySelector('#status').textContent = error;
  });
} else {
  // The current browser doesn't support service workers.
  let aElement = document.createElement('a');
  aElement.href = `
     http://www.chromium.org/blink/serviceworker/service-worker-faq
  `;
  aElement.textContent = 'unavailable';
  document.querySelector('#status').appendChild(aElement);
}</pre>

<h2 id="规范">规范</h2>

{{Specifications}}

<h2 id="浏览器兼容性">浏览器兼容性</h2>

{{Compat("api.ServiceWorkerContainer.register")}}