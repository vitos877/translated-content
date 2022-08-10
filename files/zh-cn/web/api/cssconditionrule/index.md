---
title: CSSConditionRule
slug: Web/API/CSSConditionRule
translation_of: Web/API/CSSConditionRule
---
<p>{{ APIRef("CSSOM") }}</p>

<p> </p>

<p> </p>

<p><strong>CSSConditionRule</strong> 对象表示单个条件 CSS 规则，由条件和语句块组成。继承至 {{domxref("CSSGroupingRule")}}.</p>

<p>从它派生的两个对象 : {{domxref("CSSMediaRule")}} and {{domxref("CSSSupportsRule")}}.</p>

<h2 id="Syntax">Syntax</h2>

<p>The syntax is described using the <a href="http://dev.w3.org/2006/webapi/WebIDL/">WebIDL</a> format.</p>

<pre>interface CSSConditionRule : CSSGroupingRule {
    attribute DOMString conditionText;
}
</pre>

<h2 id="Properties">Properties</h2>

<p>The <code>CSSConditionRule</code> derives from {{domxref("CSSRule")}}, {{domxref("CSSGroupingRule")}} and inherits all properties of these classes. It has one specific property:</p>

<dl>
 <dt>{{domxref("CSSConditionRule.conditionText")}}</dt>
 <dd>Represents the text of the condition of the rule.</dd>
</dl>

<h2 id="Methods">Methods</h2>

<p>The <code>CSSConditionRule</code> derives from {{domxref("CSSRule")}}, {{domxref("CSSGroupingRule")}} and inherits all methods of these classes. It has no specific property of its own.</p>

<h2 id="Specification">Specifications</h2>

{{Specifications}}

<h2 id="Browser_compatibility">Browser compatibility</h2>



<p>{{Compat("api.CSSConditionRule")}}</p>

<h2 id="See_also">See also</h2>

<ul>
 <li><a href="/en/DOM/Using_dynamic_styling_information">Using dynamic styling information</a></li>
</ul>