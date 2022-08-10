---
title: Worker.terminate()
slug: Web/API/Worker/terminate
translation_of: Web/API/Worker/terminate
---
<p>{{APIRef("Web Workers API")}}</p>

<p>{{domxref("Worker")}} 接口中的 <code><strong>terminate()</strong></code>  方法用于立即终止 {{domxref("Worker")}} 的行为。本方法并不会等待 worker 去完成它剩余的操作；worker 将会被立刻停止</p>

<h2 id="Syntax">Syntax</h2>

<pre class="brush: js">myWorker.terminate();</pre>

<h3 id="参数">参数</h3>

<p>没有。</p>

<h3 id="返回值">返回值</h3>

<p>Void.</p>

<h2 id="Example">Example</h2>

<p>以下代码示例表明，通过使用 {{domxref("Worker.Worker", "Worker()")}} 构造器创建出的{{domxref("Worker")}} 对象，在下一步操作之后会被立即终止。</p>

<pre class="brush: js">var myWorker = new Worker('worker.js');

myWorker.terminate();
</pre>

<h2 id="Specifications">Specifications</h2>

{{Specifications}}

<h2 id="Browser_compatibility">Browser compatibility</h2>

{{Compat("api.Worker.terminate")}}

<h2 id="See_also">See also</h2>

<p>{{domxref("Worker")}} 接口。</p>