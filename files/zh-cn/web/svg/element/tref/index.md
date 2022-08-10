---
title: tref
slug: Web/SVG/Element/tref
tags:
  - SVG
  - SVG 文本内容
  - 元素
  - 参考
  - 需要兼容性表
translation_of: Web/SVG/Element/tref
---
<div>{{SVGRef}}</div>

<p> {{ SVGElement("text") }} 的文本内容既可以是直接嵌入在{{SVGElement("text")}}元素中的的字符数据 ，也可以是引用元素的字符数据内容，<code>tref</code>元素用来指定的包含文本内容的引用元素。</p>

<h2 id="用法">用法</h2>

<p>{{svginfo}}</p>

<h2 id="示例">示例</h2>

<pre class="brush: xml">&lt;svg width="100%" height="100%" viewBox="0 0 1000 300"
     xmlns="http://www.w3.org/2000/svg"
     xmlns:xlink="http://www.w3.org/1999/xlink"&gt;
  &lt;defs&gt;
    &lt;text id="ReferencedText"&gt;
      Referenced character data
    &lt;/text&gt;
  &lt;/defs&gt;

  &lt;text x="100" y="100" font-size="45" &gt;
    Inline character data
  &lt;/text&gt;

  &lt;text x="100" y="200" font-size="45" fill="red" &gt;
    &lt;tref xlink:href="#ReferencedText"/&gt;
  &lt;/text&gt;

  &lt;!-- Show outline of canvas using 'rect' element --&gt;
  &lt;rect x="1" y="1" width="998" height="298"
        fill="none" stroke-width="2" /&gt;
&lt;/svg&gt;
</pre>

<h2 id="属性">属性</h2>

<h3 id="全局属性">全局属性</h3>

<ul>
 <li><a href="/en/SVG/Attribute#ConditionalProccessing">条件处理属性</a> »</li>
 <li><a href="/en/SVG/Attribute#Core">核心属性</a> »</li>
 <li><a href="/en/SVG/Attribute#GraphicalEvent">图形事件属性</a> »</li>
 <li><a href="/en/SVG/Attribute#Presentation">外观属性</a> »</li>
 <li><a href="/en/SVG/Attribute#XLink">Xlink 属性</a> »</li>
 <li>{{ SVGAttr("class") }}</li>
 <li>{{ SVGAttr("style") }}</li>
 <li>{{ SVGAttr("externalResourcesRequired") }}</li>
</ul>

<h3 id="专有属性">专有属性</h3>

<ul>
 <li>{{ SVGAttr("xlink:href") }}</li>
</ul>

<h2 id="DOM_接口">DOM 接口</h2>

<p>该元素实现了<code><a href="/en/DOM/SVGTRefElement">SVGTRefElement</a></code>接口。</p>

<h2 id="浏览器兼容性">浏览器兼容性</h2>

{{Compat("svg.elements.tref")}}

<h2 id="参见">参见</h2>

<ul>
 <li>{{ SVGElement("text") }}</li>
</ul>