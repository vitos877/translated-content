---
title: stop
slug: Web/SVG/Element/stop
tags:
  - SVG
  - SVG 渐变
  - 元素
  - 参考
  - 需要示例
translation_of: Web/SVG/Element/stop
---
<div>{{SVGRef}}</div>

<p>一个渐变上的颜色坡度，是用<code>stop</code>元素定义的。<code>stop</code>元素可以是{{SVGElement("linearGradient")}}元素或者{{SVGElement("radialGradient")}}元素的子元素。</p>

<h2 id="用法">用法</h2>

<p>{{svginfo}}</p>

<h2 id="示例">示例</h2>

<pre class="brush: html">&lt;svg width="100%" height="100%" viewBox="0 0 80 40"
     xmlns="http://www.w3.org/2000/svg"&gt;

  &lt;defs&gt;
    &lt;linearGradient id="MyGradient"&gt;
      &lt;stop offset="5%" stop-color="#F60" /&gt;
      &lt;stop offset="95%" stop-color="#FF6" /&gt;
    &lt;/linearGradient&gt;
  &lt;/defs&gt;

  &lt;!-- Outline the drawing area in black --&gt;
  &lt;rect fill="none" stroke="black"
        x="0.5" y="0.5" width="79" height="39"/&gt;

  &lt;!-- The rectangle is filled using a linear gradient --&gt;
  &lt;rect fill="url(#MyGradient)" stroke="black" stroke-width="1"
        x="10" y="10" width="60" height="20"/&gt;
&lt;/svg&gt;
</pre>

<p>示例输出：</p>

<p>{{EmbedLiveSample("Example",160,95)}}</p>

<h2 id="属性">属性</h2>

<h3 id="全局属性">全局属性</h3>

<ul>
 <li><a href="/en-US/docs/Web/SVG/Attribute#Core">核心属性</a> »</li>
 <li><a href="/en-US/docs/Web/SVG/Attribute#Presentation">外观属性</a> »</li>
 <li>{{SVGAttr("class")}}</li>
 <li>{{SVGAttr("style")}}</li>
</ul>

<h3 id="专有属性">专有属性</h3>

<ul>
 <li>{{SVGAttr("offset")}}</li>
 <li>{{SVGAttr("stop-color")}}</li>
 <li>{{SVGAttr("stop-opacity")}}</li>
</ul>

<h2 id="DOM_接口">DOM 接口</h2>

<p>该元素实现了<code><a href="/en-US/docs/Web/API/SVGStopElement">SVGStopElement</a></code>接口。</p>

<h2 id="浏览器兼容性">浏览器兼容性</h2>

{{Compat("svg.elements.stop")}}

<h2 id="参见">参见</h2>

<ul>
 <li>{{SVGElement("linearGradient")}}</li>
 <li>{{SVGElement("radialGradient")}}</li>
</ul>