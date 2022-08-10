---
title: Window.window
slug: Web/API/Window/window
translation_of: Web/API/Window/window
---
<div>{{APIRef}}</div>

<h2 id="摘要">摘要</h2>

<p>window 对象的 <code>window</code> 属性指向这个 window 对象本身。因此以下表达式所返回的 window 对象都是同一个。</p>

<pre class="syntaxbox">window.window
window.window.window
window.window.window.window
  ...

</pre>

<p>在网页中，window 对象也是一个全局对象。这意味着：</p>

<ol>
 <li>脚本中的全局变量实际上是 window 对象的属性：
  <pre class="brush:js">var global = {data: 0};
alert(global === window.global); // displays "true"
</pre>
 </li>
 <li>不用写 <code>window. </code>前缀就可以访问 window 对象的内置属性：
  <pre class="brush:js">setTimeout("alert('Hi!')", 50); // equivalent to using window.setTimeout.
alert(window === window.window); // displays "true"
</pre>
 </li>
</ol>

<p>将 <code>window</code> 属性指向该 window 对象本身的目的，是为了更容易引用全局对象。不然，就得在最开始写代码的时候进行手动赋值：<code>var window = this;</code> 。</p>

<p>另外一个原因是如果没有这个属性，就不能像这样方便的写：  {{domxref("window.open","window.open('http://google.com/')")}}，而只能这样： open('http://google.com/')</p>

<p>使用该属性还有一个原因，有些库，特别是 JavaScript 模块希望能够提供 OOP 版本和非 OOP 版本。例如，如果引用了 <code>this.window.location.href</code> ，<a href="https://developer.mozilla.org/en-US/docs/Mozilla/JavaScript_code_modules">JavaScript 模块</a>就可以在它定义的类里面定义一个 <code>window </code>属性（因为默认没有全局性的 <code>window</code> 变量存在），这个属性可以在将 window 对象传进这个模块的类的构造器之后被创建。这样，这个类的方法中的 <code>this.window</code> 就指向了 window 对象。在没有命名空间的版本中，<code>this.window</code> 会重新指向 window 对象，从而很容易获取到文档的位置。还有一个优点，这个类（即使这个类定义在模块外面）的对象可以随意地改变对 window 的引用，而如果有一个写死了的 window 的引用就做不到这样。类内部的默认值仍然可以设置成当前的 window 对象。</p>

<h2 id="规范">规范</h2>

{{Specifications}}