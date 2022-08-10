---
title: Position
slug: Web/API/GeolocationPosition
tags:
  - API
  - 位置
  - 地理位置 API
translation_of: Web/API/GeolocationPosition
---
<div>{{APIRef("Geolocation API")}}</div>

<p><strong><code>Position</code></strong>  接口表示在给定的时间的相关设备的位置。这个位置，用一个{{domxref("Coordinates")}}对象表示，包括设备在地球上的二维位置， 但也可以包括设备的海拔和速度。      </p>

<h2 id="属性">属性</h2>

<p><em><code>Position</code>接口没有继承任何属性。</em></p>

<dl>
 <dt>{{domxref("Position.coords")}} {{readonlyInline}}</dt>
 <dd>返回一个定义了当前位置的{{domxref("Coordinates")}} 对象。</dd>
 <dt>{{domxref("Position.timestamp")}} {{readonlyInline}}</dt>
 <dd>返回一个时间戳{{domxref("DOMTimeStamp")}}， 这个时间戳表示获取到的位置的时间。</dd>
</dl>

<h2 id="方法">方法</h2>

<p><em><em><code>Position</code> 接口没有实现也没有<em>继承任何方法。</em></em></em></p>

<h2 id="规范">规范</h2>

{{Specifications}}

<h2 id="浏览器兼容性">浏览器兼容性</h2>

{{Compat("api.GeolocationPosition")}}

<h2 id="参阅">参阅</h2>

<ul>
 <li><a href="/zh-CN/docs/Web/API/Geolocation/Using_geolocation">使用地理位置定位</a></li>
 <li>使用它的{{domxref("Geolocation")}}接口。</li>
</ul>