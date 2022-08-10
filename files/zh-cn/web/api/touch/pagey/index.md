---
title: Touch.pageY
slug: Web/API/Touch/pageY
tags:
  - touch
translation_of: Web/API/Touch/pageY
---
<p>{{ ApiRef() }}</p>
<h3 id="Summary">概述</h3>
<p>触点相对于 HTML 文档上边沿的的 Y 坐标。和 <code>clientY</code> 属性不同，这个值是相对于整个 html 文档的坐标，和用户滚动位置无关。因此当存在垂直滚动的偏移时，这个值包含了垂直滚动的偏移。</p>
<h3 id="Syntax">语法</h3>
<pre class="eval">var <em>y</em> = <em>touchItem</em>.pageY;
</pre>
<h3 id="Return_Value">返回值</h3>
<dl>
 <dt>
  <code>y</code></dt>
 <dd>
  触点相对于 HTML 文档上边沿的的 Y 坐标。当存在垂直滚动的偏移时，这个值包含了垂直滚动的偏移。</dd>
</dl>
<h3 id="Specification">标准定义</h3>
<p><a href="http://www.w3.org/TR/touch-events/">Touch Events Specification</a></p>
<h3 id="相关链接">相关链接</h3>
<ul>
 <li>{{ domxref("Touch.pageX") }}</li>
 <li>{{ domxref("Touch.screenY") }}</li>
 <li>{{ domxref("Touch.clientY") }}</li>
</ul>