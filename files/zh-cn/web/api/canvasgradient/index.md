---
title: CanvasGradient
slug: Web/API/CanvasGradient
translation_of: Web/API/CanvasGradient
---
<div>{{APIRef("Canvas")}}</div>

<p><code><strong>CanvasGradient</strong></code> 接口表示描述渐变的不透明对象。通过 {{domxref("CanvasRenderingContext2D.createLinearGradient()")}} 或 {{domxref("CanvasRenderingContext2D.createRadialGradient()")}} 的返回值得到。</p>

<h2 id="属性">属性</h2>

<p><em>不透明对象，没有暴露的属性。</em></p>

<h2 id="方法">方法</h2>

<p><em>没有继承的方法</em></p>

<dl>
 <dt>{{domxref("CanvasGradient.addColorStop()")}}</dt>
 <dd>添加一个由<code>偏移(offset)</code>和颜色 (<code>color</code>) 定义的断点到渐变中。如果偏移值不在 0 到 1 之间，将抛出<code>INDEX_SIZE_ERR错误，如果颜色值不能被解析为有效的</code>CSS 颜色值 {{cssxref("&lt;color&gt;")}}<code>，将抛出SYNTAX_ERR</code>错误。</dd>
</dl>

<h2 id="Specifications">标准</h2>

{{Specifications}}

<h2 id="浏览器兼容性">浏览器兼容性</h2>

{{Compat("api.CanvasGradient")}}

<h2 id="请参考">请参考</h2>

<ul>
 <li>创建方法在{{domxref("CanvasRenderingContext2D")}}.</li>
 <li>{{HTMLElement("canvas")}} 元素及其有关接口{{domxref("HTMLCanvasElement")}}.</li>
</ul>