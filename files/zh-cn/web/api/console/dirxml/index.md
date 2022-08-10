---
title: Console.dirxml()
slug: Web/API/Console/dirxml
translation_of: Web/API/Console/dirxml
---
<div>{{APIRef("Console API")}}{{Non-standard_header}}</div>

<p>显示一个明确的 XML/HTML 元素的包括所有后代元素的交互树。如果无法作为一个 element 被显示，那么会以 JavaScript 对象的形式作为替代。它的输出是一个继承的扩展的节点列表，可以让你看到子节点的内容。</p>

<h2 id="语法">语法</h2>

<pre class="syntaxbox">console.dirxml(<em>object</em>);
</pre>

<h2 id="参数">参数</h2>

<dl>
 <dt><code>object</code></dt>
 <dd>一个属性将被输出的 JavaScript 对象。</dd>
</dl>

<h2 id="浏览器兼容性">浏览器兼容性</h2>

{{Compat("api.console.dirxml")}}

<h2 id="相关链接">相关链接</h2>

<ul>
 <li><a href="http://www.opera.com/dragonfly/documentation/console/">Opera Dragonfly documentation: Console</a></li>
</ul>