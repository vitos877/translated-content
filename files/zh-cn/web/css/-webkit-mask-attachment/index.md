---
title: '-webkit-mask-attachment'
slug: Web/CSS/-webkit-mask-attachment
translation_of: Web/CSS/-webkit-mask-attachment
---
<div>{{CSSRef}}{{Non-standard_header}}</div>

<p>如果使用了 {{Cssxref("-webkit-mask-image")}}, <code>-webkit-mask-attachment</code> 将指定蒙版在视口的位置是固定的，还是同包含块一起滚动的。</p>

<pre class="brush: css no-line-numbers">/* 关键字 */
-webkit-mask-attachment: scroll;
-webkit-mask-attachment: fixed;
-webkit-mask-attachment: local;

/* 多个值 */
-webkit-mask-attachment: scroll, local;
-webkit-mask-attachment: fixed, local, scroll;

/* 全局值 */
-webkit-mask-attachment: inherit;
-webkit-mask-attachment: initial;
-webkit-mask-attachment: unset;
</pre>

<p>{{cssinfo}}</p>

<h2 id="语法">语法</h2>

<h3 id="可用的值">可用的值</h3>

<dl>
 <dt>scroll</dt>
 <dd>使用 <code>scroll</code> 时，蒙版在视口中同包含它的块一起滚动。</dd>
 <dt>fixed</dt>
 <dd>使用 <code>fixed</code> 时，蒙版不会同包含它的元素一起滚动，而是在视口中固定不动。</dd>
</dl>

<h3 id="使用语法">使用语法</h3>

{{csssyntax}}

<h2 id="示例">示例</h2>

<pre class="brush: css">body {
  -webkit-mask-image: url('images/mask.png');
  -webkit-mask-attachment: fixed;
}
</pre>

<h2 id="浏览器兼容性">浏览器兼容性</h2>

{{Compat("css.properties.-webkit-mask-attachment")}}

<h2 id="另见">另见</h2>

<p>{{cssxref("-webkit-mask")}}, {{cssxref("-webkit-mask-clip")}}, {{cssxref("-webkit-mask-box-image")}}, {{cssxref("-webkit-mask-origin")}}, {{cssxref("-webkit-mask-image")}}, {{cssxref("-webkit-mask-composite")}}, {{cssxref("-webkit-mask-repeat")}}</p>