---
title: IntersectionObserver.IntersectionObserver()
slug: Web/API/IntersectionObserver/IntersectionObserver
translation_of: Web/API/IntersectionObserver/IntersectionObserver
---
<div>{{APIRef("Intersection Observer API")}}</div>

<p><strong><code>IntersectionObserver()</code></strong>构造器创建并返回一个{{domxref("IntersectionObserver")}}对象。 如果指定<code>rootMargin</code>则会检查其是否符合语法规定，检查阈值以确保全部在 0.0 到 1.0 之间，并且阈值列表会按升序排列。如果阈值列表为空，则默认为一个 [0.0] 的数组。</p>

<h2 id="语法">语法</h2>

<pre class="syntaxbox">var <em>observer</em> = new IntersectionObserver(<em>callback</em>[, <em>options</em>]);</pre>

<h3 id="参数">参数</h3>

<dl>
 <dt><code>callback</code></dt>
 <dd>当元素可见比例超过指定阈值后，会调用一个回调函数，此回调函数接受两个参数：
 <dl>
  <dt><code>entries</code></dt>
  <dd>一个{{domxref("IntersectionObserverEntry")}}对象的数组，每个被触发的阈值，都或多或少与指定阈值有偏差。</dd>
  <dt><code>observer</code></dt>
  <dd>被调用的{{domxref("IntersectionObserver")}}实例。</dd>
 </dl>
 </dd>
 <dt><code>options</code> {{optional_inline}}</dt>
 <dd>一个可以用来配置 observer 实例的对象。如果<code>options</code>未指定，observer 实例默认使用文档视口作为 root，并且没有 margin，阈值为 0%（意味着即使一像素的改变都会触发回调函数）。你可以指定以下配置：
 <dl>
  <dt><code>root</code></dt>
  <dd>监听元素的祖先元素{{domxref("Element")}}对象，其边界盒将被视作视口。目标在根的可见区域的的任何不可见部分都会被视为不可见。</dd>
  <dt><code>rootMargin</code></dt>
  <dd>一个在计算交叉值时添加至根的边界盒 ({{Glossary('bounding_box')}}) 中的一组偏移量，类型为字符串 (string) ，可以有效的缩小或扩大根的判定范围从而满足计算需要。语法大致和 CSS 中的{{cssxref("margin")}} 属性等同; 可以参考 {{SectionOnPage("/en-US/docs/Web/API/Intersection_Observer_API", "The root element and root margin")}}来深入了解 margin 的工作原理及其语法。默认值是"0px 0px 0px 0px"。</dd>
  <dt><code>threshold</code></dt>
  <dd>规定了一个监听目标与边界盒交叉区域的比例值，可以是一个具体的数值或是一组 0.0 到 1.0 之间的数组。若指定值为 0.0，则意味着监听元素即使与根有 1 像素交叉，此元素也会被视为可见。若指定值为 1.0，则意味着整个元素都在可见范围内时才算可见。可以参考{{SectionOnPage("/en-US/docs/Web/API/Intersection_Observer_API", "Thresholds")}} 来深入了解阈值是如何使用的。阈值的默认值为 0.0。</dd>
 </dl>
 </dd>
</dl>

<h3 id="返回值">返回值</h3>

<p>一个可以使用规定阈值监听目标元素可见部分与<code>root</code>交叉状况的新的{{domxref("IntersectionObserver")}} 实例。调用自身的{{domxref("IntersectionObserver.observe", "observe()")}} 方法开始使用规定的阈值监听指定目标。</p>

<h3 id="异常">异常</h3>

<dl>
 <dt><code>SyntaxError</code></dt>
 <dd>指定的<code>rootMargin</code>不存在。</dd>
 <dt>RangeError</dt>
 <dd>一个或多个阈值超出了 0.0 到 1.0 的范围。</dd>
</dl>

<h2 id="规范">规范</h2>

{{Specifications}}

<h2 id="浏览器兼容">浏览器兼容</h2>

<p>{{Compat("api.IntersectionObserver.IntersectionObserver")}}</p>