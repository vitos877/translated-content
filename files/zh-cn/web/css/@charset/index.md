---
title: '@charset'
slug: Web/CSS/@charset
tags:
  - At-rule
  - CSS
  - Layout
  - Reference
  - Web
translation_of: Web/CSS/@charset
---
<div>{{ CSSRef }}</div>

<div> </div>

<h2 id="概述">概述</h2>

<p><strong><code>@charset</code></strong> <a href="/zh-CN/docs/Web/CSS">CSS</a> <a href="/zh-CN/docs/CSS/At-rule">@规则</a>指定样式表中使用的字符编码。它必须是样式表中的第一个元素，而前面不得有任何字符。因为它不是一个<a href="/zh-CN/docs/Web/CSS/Syntax#css_语句">嵌套语句</a>，所以不能在<a href="/zh-CN/docs/CSS/At-rule">@规则</a><a href="/zh-CN/docs/Web/CSS/At-rule#条件规则组">条件组</a>中使用。如果有多个 <strong><code>@charset</code></strong> <a href="/zh-CN/docs/CSS/At-rule">@规则</a>被声明，只有第一个会被使用，而且不能在 HTML 元素或 HTML 页面的字符集相关 {{ HTMLElement("style") }} 元素内的样式属性内使用。</p>

<p>此 <a href="/zh-CN/docs/CSS/At-rule">@规则</a>在某些 CSS 属性中使用非 ASCII 字符时非常有用，例如 {{ cssxref("content") }}。</p>

<p>在样式表中有多种方法去声明字符编码，浏览器会按照以下顺序尝试下边的方法（一旦找到就停止并得出结果）：</p>

<ol>
 <li>文件的开头的 <a href="https://zh.wikipedia.org/wiki/字节顺序标记">Unicode byte-order</a> 字符值。</li>
 <li>由 Content-Type：HTTP header 中的 charset 属性给出的值或用于提供样式表的协议中的等效值。</li>
 <li><code>CSS </code><a href="https://developer.mozilla.org/zh-CN/docs/CSS/At-rule">@规则</a>  <code>@charset。</code></li>
 <li>使用参考文档定义的字符编码：{{ HTMLElement("link") }} 元素的 charset 属性。该方法在 HTML5 标准中已废除，无法使用。</li>
 <li>假设文档是 UTF-8。</li>
</ol>

<h2 id="语法">语法</h2>

<pre class="brush: css">@charset "UTF-8";
@charset "iso-8859-15";
</pre>

<h3 id="语法格式">语法格式</h3>

<pre class="brush: css">
@charset "&lt;charset&gt;";
</pre>

<dl>
 <dt><em>charset</em></dt>
 <dd>它是一个<em> </em>{{cssxref("&lt;string&gt;")}} 表示字符编码被使用。它必须是在被 <a href="http://www.iana.org/assignments/character-sets">IANA-registry</a> 声明过的 web-safe 字符编码中的一个，还必须被双引号包围，遵循一个空格字符 (U+0020)，并且立即以分号结束。 如果有多个相关的编码名字，只有被标记为 <em>preferred  </em>的那个才会被使用。</dd>
</dl>

<h2 id="例子">例子</h2>

<pre class="brush: css">@charset "UTF-8";
@charset "utf-8"; /*大小写不敏感*/
/* 设置 css 的编码格式为 Unicode UTF-8 */
@charset 'iso-8859-15'; /* 无效的，使用了错误的引号 */
@charset  "UTF-8";      /* 无效的，多于一个空格 */
 @charset "UTF-8";      /* 无效的，在 at-rule 之前多了一个空格 */
@charset UTF-8;         /* 无效的，缺少单引号 ' 或双引号 "，charset 不是一个有效的 CSS {{cssxref("&lt;string&gt;")}} */
</pre>

<h2 id="规范">规范</h2>

{{Specifications}}

<h2 id="Browser_compatibility">浏览器兼容性</h2>

<p>{{Compat}}</p>

<h2 id="参见">参见</h2>

<ul>
<li><a href="/zh-CN/docs/Glossary/character_set">字符集</a>术语条目</li>
<li><a href="/zh-CN/docs/Glossary/Unicode">Unicode</a> 术语条目</li>
</ul>