---
title: GlobalEventHandlers.oncuechange
slug: Web/API/TextTrack/cuechange_event
tags:
  - API
  - Event Handler
  - GlobalEventHandlers
  - 事件处理函数
translation_of: Web/API/GlobalEventHandlers/oncuechange
original_slug: Web/API/GlobalEventHandlers/oncuechange
---
<div>{{ ApiRef("HTML DOM") }}</div>

<div><strong><code>oncuechange</code></strong> 属性属于{{domxref("GlobalEventHandlers")}}，是一个处理{{event("cuechange")}}事件的{{event("Event_handlers", "event handler")}}。</div>

<div>当{{domxref("TextTrack")}}更改了当前显示的提示时，<code>cuechange</code> 事件将会触发。</div>

<h2 id="语法">语法</h2>

<pre class="syntaxbox"><em><var>element</var></em>.oncuechange = <em>handlerFunction</em>;
var <em>handlerFunction</em> = <em><var>element</var></em>.oncuechange;
</pre>

<p><code>handlerFunction</code> 可以为 <code>null</code>，也可以是一个处理指定事件的<a href="/zh-CN/docs/Web/JavaScript/Reference/Functions">JavaScript函数</a>。</p>

<h2 id="规范">规范</h2>

{{Specifications}}

<h2 id="浏览器兼容性">浏览器兼容性</h2>

<p>{{Compat}}</p>

<h2 id="查看更多">查看更多</h2>

<ul>
 <li>{{event("cuechange")}}</li>
 <li><a href="/zh-CN/docs/Web/Guide/Events/Event_handlers">DOM事件处理函数</a></li>
</ul>