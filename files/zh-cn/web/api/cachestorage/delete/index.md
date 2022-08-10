---
title: CacheStorage.delete()
slug: Web/API/CacheStorage/delete
translation_of: Web/API/CacheStorage/delete
---
<p>{{APIRef("Service Workers API")}}{{SeeCompatTable}}</p>

<p>{{domxref("CacheStorage")}} 接口的 <code><strong>delete</strong></code><strong><code>()</code></strong> 方法查找匹配 <code>cacheName</code> 的 {{domxref("Cache")}} 对象，如果找到，则删除 {{domxref("Cache")}} 对象并返回一个 resolve 为 true 的 {{jsxref("Promise")}} . 如果未找到 {{domxref("Cache")}} 对象，则返回 <code>false</code>.</p>

<h2 id="语法">语法</h2>

<pre class="syntaxbox">caches.delete(<em>cacheName</em>).then(function(true) {
  //your cache is now deleted
});
</pre>

<h3 id="Returns">Returns</h3>

<p>如果找到 {{domxref("Cache")}} 对象，删除它，返回一个 resolve 为 <code>true</code> 的 {{jsxref("Promise")}} ，否则，返回 <code>false</code> .</p>

<h3 id="Parameters">Parameters</h3>

<dl>
 <dt>cacheName</dt>
 <dd>想要删除的 cache 对象的名称。</dd>
</dl>

<h2 id="实例">实例</h2>

<p>在此代码片段中，我们等待一个 activate 事件，然后运行一个 {{domxref("ExtendableEvent.waitUntil","waitUntil()")}} 块，其在一个新的 service worker 被激活前清除所有旧的、未使用的 cache. 这里我们有一个白名单，其中包含我们想要保留的 cache 的 name. 我们使用 {{domxref("CacheStorage.keys")}} 返回 {{domxref("CacheStorage")}} 对象中 cache 的键，然后检查每个键值，以查看它是否在白名单中。如果没有，我们使用 <code>delete()</code> 删除它。</p>

<pre class="brush: js">this.addEventListener('activate', function(event) {
  var cacheWhitelist = ['v2'];

  event.waitUntil(
    caches.keys().then(function(keyList) {
      return Promise.all(keyList.map(function(key) {
        if (cacheWhitelist.indexOf(key) === -1) {
          return caches.delete(key);
        }
      }));
    })
  );
});</pre>

<h2 id="规范">规范</h2>

{{Specifications}}

<h2 id="浏览器兼容性">浏览器兼容性</h2>

{{Compat("api.CacheStorage.delete")}}

<h2 id="See_also">See also</h2>

<ul>
 <li><a href="/en-US/docs/Web/API/ServiceWorker_API/Using_Service_Workers">Using Service Workers</a></li>
 <li>{{domxref("Cache")}}</li>
 <li>{{domxref("WorkerGlobalScope.caches")}}</li>
</ul>