---
title: SpeechGrammar.SpeechGrammar()
slug: Web/API/SpeechGrammar/SpeechGrammar
tags:
  - API
  - SpeechGrammar
  - Web
  - Web Speech API
  - 实验性
  - 引用
  - 构造函数
  - 语音识别
translation_of: Web/API/SpeechGrammar/SpeechGrammar
---
<p>{{APIRef("Web Speech API")}}{{SeeCompatTable}}</p>

<p><code><strong>SpeechGrammar</strong></code> 是 {{domxref("SpeechGrammar")}} 接口的构造函数，创建一个新的 <code>SpeechGrammar</code> 对象实例。</p>

<h2 id="语法">语法</h2>

<pre class="syntaxbox">var mySpeechGrammar = new SpeechGrammar();</pre>

<h3 id="Parameters">Parameters</h3>

<p>无。</p>

<h2 id="样例">样例</h2>

<pre class="brush: js">var grammar = '#JSGF V1.0; grammar colors; public &lt;color&gt; = aqua | azure | beige | bisque | black | blue | brown | chocolate | coral | crimson | cyan | fuchsia | ghostwhite | gold | goldenrod | gray | green | indigo | ivory | khaki | lavender | lime | linen | magenta | maroon | moccasin | navy | olive | orange | orchid | peru | pink | plum | purple | red | salmon | sienna | silver | snow | tan | teal | thistle | tomato | turquoise | violet | white | yellow ;'
var recognition = new SpeechRecognition();
var speechRecognitionList = new SpeechGrammarList();
speechRecognitionList.addFromString(grammar, 1);
recognition.grammars = speechRecognitionList;

var newGrammar = new SpeechGrammar();
newGrammar.src = '#JSGF V1.0; grammar names; public &lt;name&gt; = chris | kirsty | mike;'
speechRecognitionList[1] = newGrammar; // 将 SpeechGrammar 对象添加到列表中
</pre>

<h2 id="规格">规格</h2>

<p>此 API 没有官方的 W3C 或 WHATWG 规范。</p>

<h2 id="浏览器兼容性">浏览器兼容性</h2>

{{Compat}}

<h2 id="相关链接">相关链接</h2>

<ul>
 <li><a href="/en-US/docs/Web/API/Web_Speech_API">Web Speech API</a></li>
</ul>