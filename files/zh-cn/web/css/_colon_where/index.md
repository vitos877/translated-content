---
title: ':where()'
slug: 'Web/CSS/:where'
tags:
  - CSS
  - Web
  - 伪类
  - 参考
  - 选择器
translation_of: 'Web/CSS/:where'
---
<p>{{CSSRef}}{{SeeCompatTable}}</p>

<p><strong><code>:where()</code></strong> <a href="/zh-CN/docs/Web/CSS/Pseudo-classes">CSS 伪类</a>函数接受<a href="/zh-CN/docs/Web/CSS/Selector_list">选择器列表</a>作为它的参数，将会选择所有能被该选择器列表中任何一条规则选中的元素。</p>

<p><code>:where()</code> 和 {{CSSxRef(":is", ":is()")}} 的不同之处在于，<code>:where()</code> 的<a href="/zh-CN/docs/Web/CSS/Specificity">优先级</a>总是为 0 ，但是 <code>:is()</code> 的优先级是由它的选择器列表中优先级最高的<a href="/zh-CN/docs/Glossary/CSS_Selector">选择器</a>决定的。</p>

<h2 id="语法">语法</h2>

{{CSSSyntax}}

<h2 id="规范">规范</h2>

{{Specifications}}

<h2 id="浏览器兼容性">浏览器兼容性</h2>

<div>


<p>{{Compat("css.selectors.where")}}</p>
</div>

<h2 id="参见">参见</h2>

<ul>
 <li>{{CSSxRef(":is", ":is()")}} {{Experimental_Inline}}</li>
 <li><a href="/zh-CN/docs/Web/CSS/Selector_list">选择器列表</a></li>
</ul>