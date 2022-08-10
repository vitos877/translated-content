---
title: CSS 分页规则
slug: Web/API/CSSPageRule
translation_of: Web/API/CSSPageRule
original_slug: Web/API/CSS 分页规则
---
<div>{{APIRef("CSSOM")}}</div>

<p><strong><code>CSSPageRule</code></strong>  是代表一个 css 接口 {{cssxref("@page")}} 规则。它实现了 {{domxref("CSSRule")}} 类型值为 6 的接口 (<code>CSSRule.PAGE_RULE</code>).</p>

<h2 id="语法">语法</h2>

<p>这个语法是使用 <a href="https://dev.w3.org/2006/webapi/WebIDL/">WebIDL</a> 格式。</p>

<pre class="syntaxbox">interface CSSPageRule : CSSRule {
  attribute DOMString selectorText;
  readonly attribute CSSStyleDeclaration style;
};
</pre>

<h2 id="Properties">Properties</h2>

<p> {{domxref("CSSRule")}}, <code>CSSPageRule</code> 也实现了此接口的属性。 它具有以下特定属性：</p>

<dl>
 <dt>{{domxref("CSSPageRule.selectorText")}}</dt>
 <dd>表示与规则关联的页面选择器的文本。</dd>
 <dt>{{domxref("CSSPageRule.style")}} {{readonlyinline}}</dt>
 <dd>返回与规则关联的声明块。</dd>
</dl>

<h2 id="Methods">Methods</h2>

<p>作为 {{domxref("CSSRule")}}, <code>CSSPageRule</code> 的 CSSPageRule 还实现了该接口的方法。 它没有具体方法。</p>

<h2 id="Specifications">Specifications</h2>

{{Specifications}}

<h2 id="Browser_compatibility">Browser compatibility</h2>



<p>{{Compat("api.CSSPageRule")}}</p>