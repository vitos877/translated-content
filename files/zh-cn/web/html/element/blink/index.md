---
title: <blink>
slug: Web/HTML/Element/blink
translation_of: Web/HTML/Element/blink
---
<div>{{Deprecated_header}}</div>

<p>HTML Blink Element (<code>&lt;blink&gt;</code>) 不是标准元素，它会使包含其中的文本闪烁。</p>

<div class="warning">
<p><strong>警告：</strong> 不要使用这个元素，它已经被<strong>淘汰</strong>。闪烁字体不符合无障碍标准，CSS 规范允许浏览器忽略闪烁值。</p>
</div>

<h2 id="DOM_接口">DOM 接口</h2>

<p>该元素不被支持，因而实现了{{domxref("HTMLUnknownElement")}} 接口。</p>

<h2 id="示例">示例</h2>

<pre class="brush:html">&lt;blink&gt;Why would somebody use this?&lt;/blink&gt;
</pre>

<h3 id="结果_(淡化!)">结果 (淡化！)</h3>

<p><img alt="Image:HTMLBlinkElement.gif" src="/@api/deki/files/247/=HTMLBlinkElement.gif"></p>

<h2 id="规范">规范</h2>

<p>该元素不是标准元素，不属于规范的一部分。不信的话，<a href="http://www.whatwg.org/specs/web-apps/current-work/multipage/obsolete.html#non-conforming-features"> 你自己来看 HTML 规范文档</a>.</p>

<h2 id="浏览器兼容">浏览器兼容</h2>

{{Compat("html.elements.blink")}}

<h2 id="参见">参见</h2>

<ul>
 <li><a href="http://www.montulli.org/theoriginofthe%3Cblink%3Etag">History of the creation of the HTML <code>&lt;blink&gt;</code> element</a>.</li>
 <li>{{cssxref("text-decoration")}}, where a blink value exists, though browsers are not required to effectively make it blink.</li>
 <li>{{htmlelement("marquee")}}, another similar non-standard element.</li>
 <li><a href="/en-US/docs/Web/Guide/CSS/Using_CSS_animations">CSS animations</a> are the way to go to create such an effect.</li>
</ul>

<p>{{HTMLRef}}</p>