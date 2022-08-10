---
title: StorageManager
slug: Web/API/StorageManager
translation_of: Web/API/StorageManager
---
<p>{{securecontext_header}}{{SeeCompatTable}}{{APIRef("Storage")}}</p>

<p><a href="https://developer.mozilla.org/zh-CN/docs/Web/API/Storage_API">Storage API</a>的<strong><code>StorageManager</code></strong>接口提供了用于管理数据本地存储权限和估算可用存储空间的接口。 您可以使用{{domxref("navigator.storage")}}或{{domxref("WorkerNavigator.storage")}}对此接口进行引用。</p>

<h2 id="方法">方法</h2>

<dl>
 <dt>{{domxref("StorageManager.estimate()")}} {{securecontext_inline}}</dt>
 <dd>返回一个{{domxref("StorageEstimate")}}对象，此对象包含为你的域名预留的存储空间总大小和你已经使用的存储空间大小。</dd>
 <dt>{{domxref("StorageManager.persist()")}} {{securecontext_inline}}</dt>
 <dd>如果您的 user agent 能够将你域名下的数据持久保存，那么将返回一个状态为 resolve 的{{jsxref('Promise')}}</dd>
 <dt>{{domxref("StorageManager.persisted()")}} {{securecontext_inline}}</dt>
 <dd>如果您的站点已经被授予可使用数据本地存储的权限，则返回一个状态为 resolve 的{{jsxref('Promise')}}</dd>
</dl>

<h2 id="规范">规范</h2>

{{Specifications}}

<h2 id="浏览器兼容性">浏览器兼容性</h2>



<p>{{Compat("api.StorageManager")}}</p>