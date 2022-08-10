---
title: HTMLHyperlinkElementUtils.password
slug: Web/API/HTMLAnchorElement/password
tags:
  - HTMLHyperlinkElementUtils.password
translation_of: Web/API/HTMLHyperlinkElementUtils/password
original_slug: Web/API/HTMLHyperlinkElementUtils/password
---
<p>{{ApiRef("URL API")}}</p>

<p>HTMLHyperlinkElementUtils<strong><code>.password</code></strong> property 属性是一个{{domxref("USVString")}} ，包含域名前面指定的密码。</p>

<p>如果在没有首先设置<code><a href="/en-US/docs/Web/API/HTMLHyperlinkElementUtils/username">用户名</a></code>属性的情况下设置，则会静默失败。</p>

<h2 id="Syntax">Syntax</h2>

<pre class="syntaxbox"><em>string</em> = <em>object</em>.password;
<em>object</em>.password = <em>string</em>;
</pre>

<h2 id="Examples">Examples</h2>

<pre class="brush: js">// Let's &lt;a id="myAnchor" href="https://anonymous:flabada@developer.mozilla.org/en-US/docs/HTMLHyperlinkElementUtils.username"&gt; be in the document
var anchor = document.getElementByID("myAnchor");
var result = anchor.password; // Returns:'flabada'
</pre>

<h2 id="Specifications">Specifications</h2>

{{Specifications}}

<h2 id="Browser_compatibility">Browser compatibility</h2>

{{Compat("api.HTMLAnchorElement.password")}}

<h2 id="See_also">See also</h2>

<ul>
 <li>The {{domxref("HTMLHyperlinkElementUtils")}} mixin it belongs to.</li>
</ul>