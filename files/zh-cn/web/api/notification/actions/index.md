---
title: Notification.actions
slug: Web/API/notification/actions
tags:
  - Notification actions
  - Notifications
  - Web API
  - Web Notifications API
translation_of: Web/API/Notification/actions
---
<p>{{APIRef("Web Notifications")}}</p>

<p>{{domxref("Notification")}}接口的只读属性<strong><code>actions</code></strong>返回使用{{domxref("Notification.Notification","Notification()")}}构造函数创建通知时使用 actions 选项设置的{{domxref("NotificationAction")}}对象列表。这是用户可以在通知上下文中选择立即执行的应用定义的操作列表。</p>

<p>{{AvailableInWorkers}}</p>

<h2 id="Syntax">语法</h2>

<pre class="syntaxbox">var <em>actions</em>[] = <em>Notification</em>.actions;</pre>

<h3 id="Return_Value">值</h3>

<p>{{domxref("NotificationAction")}}对象的只读数组。用户在通知中选择每项的单一的功能。</p>

<h2 id="规范">规范</h2>

{{Specifications}}

<h2 id="浏览器兼容性">浏览器兼容性</h2>

{{Compat("api.Notification.actions")}}

<h2 id="更多">更多</h2>

<ul>
 <li><a href="/en-US/docs/Web/API/Notifications_API/Using_the_Notifications_API">Using the Notifications API</a></li>
</ul>