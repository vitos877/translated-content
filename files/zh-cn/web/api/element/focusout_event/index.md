---
title: focusout
slug: Web/API/Element/focusout_event
translation_of: Web/API/Element/focusout_event
original_slug: Web/Events/focusout
---
<p>当元素即将失去焦点时，focusout 事件被触发。focusout 事件和 <a href="/zh-CN/docs/Web/Events/blur">blur</a> 事件之间的主要区别在于后者不会冒泡。</p>

<h2 id="基本信息">基本信息</h2>

<dl>
 <dt>Specification</dt>
 <dd><a href="http://www.w3.org/TR/DOM-Level-3-Events/#event-type-focusout">DOM L3</a></dd>
 <dt>Interface</dt>
 <dd>{{domxref("FocusEvent")}}</dd>
 <dt>Bubbles</dt>
 <dd>Yes</dd>
 <dt>Cancelable</dt>
 <dd>No</dd>
 <dt>Target</dt>
 <dd>Element</dd>
 <dt>Default Action</dt>
 <dd>None.</dd>
</dl>

<h2 id="属性">属性</h2>

<table>
 <thead>
  <tr>
   <th scope="col">Property</th>
   <th scope="col">Type</th>
   <th scope="col">Description</th>
  </tr>
 </thead>
 <tbody>
  <tr>
   <td><code>target</code> {{readonlyInline}}</td>
   <td>{{domxref("EventTarget")}}</td>
   <td>Event target losing focus.</td>
  </tr>
  <tr>
   <td><code>type</code> {{readonlyInline}}</td>
   <td>{{domxref("DOMString")}}</td>
   <td>The type of event.</td>
  </tr>
  <tr>
   <td><code>bubbles</code> {{readonlyInline}}</td>
   <td>{{jsxref("Boolean")}}</td>
   <td>Whether the event normally bubbles or not.</td>
  </tr>
  <tr>
   <td><code>cancelable</code> {{readonlyInline}}</td>
   <td>{{jsxref("Boolean")}}</td>
   <td>Whether the event is cancellable or not.</td>
  </tr>
  <tr>
   <td><code>relatedTarget</code> {{readonlyInline}}</td>
   <td>{{domxref("EventTarget")}} (DOM element)</td>
   <td>Event target receiving focus.</td>
  </tr>
 </tbody>
</table>

<h2 id="规范">规范</h2>

{{Specifications}}

<h2 id="浏览器兼容性">浏览器兼容性</h2>

{{Compat("api.Element.focusout_event")}}

<h2 id="相关事件">相关事件</h2>

<ul>
 <li>{{event("focus")}}</li>
 <li>{{event("blur")}}</li>
 <li>{{event("focusin")}}</li>
 <li>{{event("focusout")}}</li>
</ul>