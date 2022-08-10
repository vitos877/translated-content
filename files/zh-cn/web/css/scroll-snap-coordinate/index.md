---
title: scroll-snap-coordinate
slug: Web/CSS/scroll-snap-coordinate
tags:
  - CSS
  - css snap
translation_of: Web/CSS/scroll-snap-coordinate
---
<div>{{CSSRef}}{{SeeCompatTable}}</div>

<h2 id="摘要">摘要</h2>

<p><strong><code>scroll-snap-coordinate</code></strong> <a href="/en-US/docs/Web/CSS">CSS</a>属性结合元素的最近的祖先元素滚动容器的{{cssxref("scroll-snap-destination")}} 定义的轴，定义了元素中 x 和 y 坐标偏移的位置。</p>

<p>如果元素已经变型，snap 坐标也以相同的方式进行变型，为了使元素的 snap 点向元素一样被显示。</p>

<div>{{cssinfo}}</div>

<h2 id="语法">语法</h2>

<pre class="brush: css">/* 关键值 */
scroll-snap-coordinate: none;

/* &lt;位置&gt;值 */
scroll-snap-coordinate: 50px 50px;                   /* 单坐标 */
scroll-snap-coordinate: 100px 100px, 100px bottom;   /* 多坐标 */

/* 全局值 */
scroll-snap-coordinate: inherit;
scroll-snap-coordinate: initial;
scroll-snap-coordinate: unset;
</pre>

<h3 id="赋值">赋值</h3>

<dl>
 <dt><code>none</code></dt>
 <dd>定义元素不提供一个 snap 点。</dd>
 <dt><code>&lt;position&gt;</code></dt>
 <dd>定义从元素核模型边框边缘开始偏移的 snap 坐标。每一对值中，第一个值给定了 snap 坐标的 x 坐标，第二个值为它的 y 坐标。</dd>
</dl>

<h3 id="正式语法">正式语法</h3>

{{csssyntax}}

<h2 id="示例">示例</h2>

<h3 id="HTML内容">HTML 内容</h3>

<pre class="brush: html">&lt;div id="container"&gt;
  &lt;div&gt;
    &lt;p&gt;At coordinate (0, 0)&lt;/p&gt;
    &lt;div class="scrollContainer coordinate0"&gt;
      &lt;div&gt;1&lt;/div&gt;
      &lt;div&gt;2&lt;/div&gt;
      &lt;div&gt;3&lt;/div&gt;
    &lt;/div&gt;
  &lt;/div&gt;

  &lt;div&gt;
    &lt;p&gt;At coordinate (25, 0)&lt;/p&gt;
    &lt;div class="scrollContainer coordinate25"&gt;
      &lt;div&gt;1&lt;/div&gt;
      &lt;div&gt;2&lt;/div&gt;
      &lt;div&gt;3&lt;/div&gt;
    &lt;/div&gt;
  &lt;/div&gt;

  &lt;div&gt;
    &lt;p&gt;At coordinate (50, 0)&lt;/p&gt;
    &lt;div class="scrollContainer coordinate50"&gt;
      &lt;div&gt;1&lt;/div&gt;
      &lt;div&gt;2&lt;/div&gt;
      &lt;div&gt;3&lt;/div&gt;
    &lt;/div&gt;
  &lt;/div&gt;
&lt;/div&gt;
</pre>

<h3 id="CSS内容">CSS 内容</h3>

<pre class="brush: css">#container {
  display: flex;
}

#container &gt; div:nth-child(-n+2) {
  margin-right: 20px;
}

.scrollContainer {
  width: 100px;
  overflow: auto;
  white-space: nowrap;
  scroll-snap-type: mandatory;
  font-size: 0;
}

.scrollContainer &gt; div {
  width: 100px;
  height: 100px;
  display: inline-block;
  line-height: 100px;
  text-align: center;
  font-size: 50px;
}

.coordinate0 &gt; div {
  scroll-snap-coordinate: 0 0;
}

.coordinate25 &gt; div {
  scroll-snap-coordinate: 25px 0;
}

.coordinate50 &gt; div {
  scroll-snap-coordinate: 50px 0;
}

.scrollContainer &gt; div:nth-child(even) {
  background-color: #87ea87;
}

.scrollContainer &gt; div:nth-child(odd) {
  background-color: #87ccea;
}</pre>

<p>{{EmbedLiveSample("Example", "100%", "170")}}</p>

<h2 id="规范">规范</h2>

<p>不属于任何规范。</p>

<h2 id="浏览器兼容性">浏览器兼容性</h2>

{{Compat}}