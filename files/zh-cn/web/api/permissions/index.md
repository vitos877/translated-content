---
title: Permissions
slug: Web/API/Permissions
translation_of: Web/API/Permissions
---
<p>{{APIRef("Permissions API")}}{{SeeCompatTable}}</p>

<p><a href="Permissions_API">Permissions API</a>的 Permissions 接口提供核心 PermissionAPI 功能，例如查询和撤消权限的方法。</p>

<h2 id="方法">方法</h2>

<dl>
 <dt>{{domxref("Permissions.query","Permissions.query()")}}</dt>
 <dd>返回给定 API 的用户权限状态。</dd>
 <dt>{{domxref("Permissions.request","Permissions.request()")}}</dt>
 <dd>
 <p>请求使用给定 API 的权限，目前此功能尚未在任何浏览器中被支持。</p>
 </dd>
 <dt>{{domxref("Permissions.requestAll","Permissions.requestAll()")}}</dt>
 <dd>请求使用一组给定 API 的权限。目前此功能尚未在任何浏览器中被支持。</dd>
 <dt>{{domxref("Permissions.revoke","Permissions.revoke()")}}</dt>
 <dd>返回撤消当前在给定 API 上设置的权限。</dd>
</dl>

<h2 id="Example">Example</h2>

<pre class="brush: js">navigator.permissions.query({name:'geolocation'}).then(function(result) {
  if (result.state === 'granted') {
    showLocalNewsWithGeolocation();
  } else if (result.state === 'prompt') {
    showButtonToEnableLocalNews();
  }
  // 如果没有此权限则不什么也做
});</pre>

<h2 id="Specification">Specification</h2>

{{Specifications}}

<h2 id="Browser_Support">Browser Support</h2>

<div>


<p>{{Compat("api.Permissions")}}</p>
</div>