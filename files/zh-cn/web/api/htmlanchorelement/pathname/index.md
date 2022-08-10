---
title: HTMLHyperlinkElementUtils.pathname
slug: Web/API/HTMLAnchorElement/pathname
tags:
  - HTMLHyperlinkElementUtils.pathname
translation_of: Web/API/HTMLHyperlinkElementUtils/pathname
original_slug: Web/API/HTMLHyperlinkElementUtils/pathname
---
<p>{{ApiRef("URL API")}}</p>

<p><strong><code>HTMLHyperlinkElementUtils.pathname</code></strong> 属性是一个 {{domxref("USVString")}} ，其中包含一个初始的'/'后跟URL的路径。</p>

<h2 id="Syntax">Syntax</h2>

<pre class="syntaxbox"><em>string</em> = <em>object</em>.pathname;
<em>object</em>.pathname = <em>string</em>;
</pre>

<h2 id="Examples">Examples</h2>

<pre class="brush: js">// Let's an &lt;a id="myAnchor" href="https://developer.mozilla.org/en-US/docs/HTMLHyperlinkElementUtils.pathname"&gt; element be in the document
var anchor = document.getElementById("myAnchor");
var result = anchor.pathname; // Returns:'/en-US/docs/HTMLHyperlinkElementUtils.pathname'
</pre>

<h2 id="Specifications">Specifications</h2>

{{Specifications}}

<h2 id="Browser_compatibility">Browser compatibility</h2>

{{Compat("api.HTMLAnchorElement.pathname")}}

<h2 id="See_also">See also</h2>

<ul>
 <li>The {{domxref("HTMLHyperlinkElementUtils")}} mixin it belongs to.</li>
</ul>