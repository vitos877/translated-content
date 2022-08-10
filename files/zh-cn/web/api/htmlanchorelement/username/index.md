---
title: HTMLHyperlinkElementUtils.username
slug: Web/API/HTMLAnchorElement/username
tags:
  - HTMLHyperlinkElementUtils.username
translation_of: Web/API/HTMLHyperlinkElementUtils/username
original_slug: Web/API/HTMLHyperlinkElementUtils/username
---
<p>{{ApiRef("URL API")}}</p>

<p><strong><code>HTMLHyperlinkElementUtils.username</code></strong> 属性是一个 {{domxref("USVString")}}包含域名前面指定的用户名。</p>

<h2 id="Syntax">Syntax</h2>

<pre class="syntaxbox"><em>string</em> = <em>object</em>.username;
<em>object</em>.username = <em>string</em>;
</pre>

<h2 id="Examples">Examples</h2>

<pre class="brush: js">// Let's &lt;a id="myAnchor" href="https://anonymous:flabada@developer.mozilla.org/en-US/docs/HTMLHyperlinkElementUtils.username"&gt; be in the document
var anchor = document.getElementByID("myAnchor");
var result = anchor.username; // Returns:'anonymous'
</pre>

<h2 id="Specifications">Specifications</h2>

{{Specifications}}

<h2 id="Browser_compatibility">Browser compatibility</h2>

{{Compat("api.HTMLAnchorElement.username")}}

<h2 id="See_also">See also</h2>

<ul>
 <li>The {{domxref("HTMLHyperlinkElementUtils")}} interface it belongs to.</li>
</ul>