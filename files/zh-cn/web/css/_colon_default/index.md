---
title: ':default'
slug: 'Web/CSS/:default'
translation_of: 'Web/CSS/:default'
---
<div>{{CSSRef}}</div>

<p> <strong><code>:default</code></strong> <a href="/zh-CN/docs/Web/CSS">CSS</a> <a href="/zh-CN/docs/Web/CSS/Pseudo-classes">pseudo-class</a> 表示一组相关元素中的默认表单元素。</p>

<p>该选择器可以在 {{htmlelement("button")}}, <code><a href="/zh-CN/docs/Web/HTML/Element/input/checkbox">&lt;input type="checkbox"&gt;</a></code>, <code><a href="/zh-CN/docs/Web/HTML/Element/input/radio">&lt;input type="radio"&gt;</a></code>, 以及 {{htmlelement("option")}} 上使用。</p>

<pre class="brush: css no-line-numbers  language-css"><code class="language-css">/* Selects any default &lt;input&gt; */
input:default {
  background-color: lime;
}</code></pre>

<p>允许多个选择的分组元素也可以具有多个默认值，即，它们可以具有最初选择的多个项目。在这种情况下，所有默认值都使用 <code>:default</code> 伪类表示。例如，您可以在一组复选框之间设置默认复选框。</p>

<h2 id="语法">语法</h2>

{{csssyntax}}

<h2 id="示例">示例</h2>

<h3 id="HTML">HTML</h3>

<pre class="brush: html">&lt;input type="radio" name="season" id="spring"&gt;
&lt;label for="spring"&gt;Spring&lt;/label&gt;

&lt;input type="radio" name="season" id="summer" checked&gt;
&lt;label for="summer"&gt;Summer&lt;/label&gt;

&lt;input type="radio" name="season" id="fall"&gt;
&lt;label for="fall"&gt;Fall&lt;/label&gt;

&lt;input type="radio" name="season" id="winter"&gt;
&lt;label for="winter"&gt;Winter&lt;/label&gt;</pre>

<h3 id="CSS">CSS</h3>

<pre class="brush: css">input:default {
  box-shadow: 0 0 2px 1px coral;
}

input:default + label {
  color: coral;
}</pre>

<h3 id="结果">结果</h3>

<p>{{EmbedLiveSample('示例')}}</p>

<h2 id="规范">规范</h2>

{{Specifications}}

<h2 id="浏览器兼容性">浏览器兼容性</h2>

{{Compat("css.selectors.default")}}