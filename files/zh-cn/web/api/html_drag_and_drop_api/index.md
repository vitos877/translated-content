---
title: HTML 拖放 API
slug: Web/API/HTML_Drag_and_Drop_API
tags:
  - HTML5
  - XUL
  - drag and drop
  - 事件
  - 总览
  - 拖放
  - 指南
  - 进阶
translation_of: Web/API/HTML_Drag_and_Drop_API
---
<p>{{DefaultAPISidebar("HTML Drag and Drop API")}}</p>

<p><strong>HTML 拖放（</strong><strong>Drag and Drop）</strong>接口使应用程序能够在浏览器中使用拖放功能。例如，用户可使用鼠标选择可拖拽（<em>draggable</em>）元素，将元素拖拽到可放置（<em>droppable</em>）元素，并释放鼠标按钮以放置这些元素。拖拽操作期间，会有一个可拖拽元素的半透明快照跟随着鼠标指针。</p>

<p>对于网站、扩展以及 XUL 应用程序，你可以自定义什么元素是可拖拽的、可拖拽元素产生的反馈类型，以及可放置的元素。</p>

<p>此文档为 HTML 拖放的概述，包含了相关接口的说明、在应用程序中加入拖放支持的基本步骤，以及相关接口的使用简介。</p>

<h2 id="拖拽事件">拖拽事件</h2>

<p>HTML 的 drag &amp; drop 使用了 {{domxref("Event","DOM event model")}} 以及从 {{domxref("MouseEvent","mouse events")}} 继承而来的 <em>{{domxref("DragEvent","drag events")}}</em> 。一个典型的拖拽操作是这样的：用户选中一个<em>可拖拽的（draggable）</em>元素，并将其拖拽（鼠标不放开）到一个<em>可放置的（droppable）</em>元素，然后释放鼠标。</p>

<p>在操作期间，会触发一些事件类型，有一些事件类型可能会被多次触发（比如{{event("drag")}} 和 {{event("dragover")}} 事件类型）。</p>

<p>所有的 <a href="/zh-CN/docs/Web/API/DragEvent#Event_types">拖拽事件类型</a> 有一个对应的 <a href="/zh-CN/docs/Web/API/DragEvent#GlobalEventHandlers">拖拽全局属性</a>。每个拖拽事件类型和拖拽全局属性都有对应的描述文档。下面的表格提供了一个简短的事件类型描述，以及一个相关文档的链接。</p>

<table>
 <tbody>
  <tr>
   <th scope="col">事件</th>
   <th scope="col">On 型事件处理程序</th>
   <th scope="col">触发时刻</th>
  </tr>
  <tr>
   <td>{{event('drag')}}</td>
   <td>{{domxref('GlobalEventHandlers.ondrag','ondrag')}}</td>
   <td>当拖拽元素或选中的文本时触发。</td>
  </tr>
  <tr>
   <td>{{event('dragend')}}</td>
   <td>{{domxref('GlobalEventHandlers.ondragend','ondragend')}}</td>
   <td>当拖拽操作结束时触发 (比如松开鼠标按键或敲“Esc”键). (见<a href="/zh-CN/docs/DragDrop/Drag_Operations#dragend">结束拖拽</a>)</td>
  </tr>
  <tr>
   <td>{{event('dragenter')}}</td>
   <td>{{domxref('GlobalEventHandlers.ondragenter','ondragenter')}}</td>
   <td>当拖拽元素或选中的文本到一个可释放目标时触发（见 <a href="/zh-CN/docs/DragDrop/Drag_Operations#droptargets">指定释放目标</a>）。</td>
  </tr>
  <tr>
   <td>{{event('dragexit')}}</td>
   <td>{{domxref('GlobalEventHandlers.ondragexit','ondragexit')}}</td>
   <td>当元素变得不再是拖拽操作的选中目标时触发。</td>
  </tr>
  <tr>
   <td>{{event('dragleave')}}</td>
   <td>{{domxref('GlobalEventHandlers.ondragleave','ondragleave')}}</td>
   <td>当拖拽元素或选中的文本离开一个可释放目标时触发。</td>
  </tr>
  <tr>
   <td>{{event('dragover')}}</td>
   <td>{{domxref('GlobalEventHandlers.ondragover','ondragover')}}</td>
   <td>当元素或选中的文本被拖到一个可释放目标上时触发（每 100 毫秒触发一次）。</td>
  </tr>
  <tr>
   <td>{{event('dragstart')}}</td>
   <td>{{domxref('GlobalEventHandlers.ondragstart','ondragstart')}}</td>
   <td>当用户开始拖拽一个元素或选中的文本时触发（见<a href="/zh-CN/docs/DragDrop/Drag_Operations#dragstart">开始拖拽操作</a>）。</td>
  </tr>
  <tr>
   <td>{{event('drop')}}</td>
   <td>{{domxref('GlobalEventHandlers.ondrop','ondrop')}}</td>
   <td>当元素或选中的文本在可释放目标上被释放时触发（见<a href="/zh-CN/docs/DragDrop/Drag_Operations#drop">执行释放</a>）。</td>
  </tr>
 </tbody>
</table>

<p><strong>注意：</strong>当从操作系统向浏览器中拖拽文件时，不会触发 <code>dragstart</code> 和<code>dragend</code> 事件。</p>

<h2 id="接口">接口</h2>

<p>HTML 的拖拽接口有 {{domxref("DragEvent")}}, {{domxref("DataTransfer")}}, {{domxref("DataTransferItem")}} 和{{domxref("DataTransferItemList")}}。</p>

<p>{{domxref("DragEvent")}} 接口有一个构造函数和一个 {{domxref("DragEvent.dataTransfer","dataTransfer")}} 属性，dataTransfer 属性是一个 {{domxref("DataTransfer")}} 对象。</p>

<p>{{domxref("DataTransfer")}} 对象包含了拖拽事件的状态，例如拖拽事件的类型（如拷贝 <code>copy</code> 或者移动 <code>move</code>），拖拽的数据（一个或者多个项）和每个拖拽项的类型（MIME 类型）。 {{domxref("DataTransfer")}} 对象也有向拖拽数据中添加或删除项目的方法。</p>

<p>给应用程序添加 HTML 拖放功能，{{domxref("DragEvent")}} 和 {{domxref("DataTransfer")}} 接口应该是唯二需要的接口（Firefox 给 {{domxref("DataTransfer")}} 添加了一些 Gecko 专有的扩展功能，但这些扩展只在 Firefox 上可用）。</p>

<p>每个 {{domxref("DataTransfer")}} 都包含一个  {{domxref("DataTransfer.items","items")}} 属性，这个属性是 {{domxref("DataTransferItem")}} 对象的 {{domxref("DataTransferItemList","list")}}。一个 {{domxref("DataTransferItem")}} 代表一个拖拽项目，每个项目都有一个 {{domxref("DataTransferItem.kind","kind")}} 属性（<code>string</code> 或 <code>file</code>）和一个表示数据项目 MIME 类型的 {{domxref("DataTransferItem.type","type")}} 属性。{{domxref("DataTransferItem")}} 对象也有获取拖拽项目数据的方法。</p>

<p>{{domxref("DataTransferItemList")}} 对象是 {{domxref("DataTransferItem")}} 对象的列表。这个列表对象包含以下方法：向列表中添加拖拽项，从列表中移除拖拽项和清空列表中所有的拖拽项。</p>

<p>{{domxref("DataTransfer")}} 和 {{domxref("DataTransferItem")}} 接口的一个主要的不同是前者使用同步的 {{domxref("DataTransfer.getData","getData()")}} 方法去得到拖拽项的数据，而后者使用异步的 {{domxref("DataTransferItem.getAsString","getAsString()")}} 方法得到拖拽项的数据。</p>

<p>注意: {{domxref("DragEvent")}} 和 {{domxref("DataTransfer")}} 接口是所有桌面浏览器都支持的。但是， {{domxref("DataTransferItem")}} 和{{domxref("DataTransferItemList")}} 接口并不被所有浏览器支持。请移步 <a href="#互操作性">互操作性</a> 了解更多关于拖拽行为的信息。</p>

<h3 id="Gecko_专用接口">Gecko 专用接口</h3>

<p>Mozilla 和 Firefox 支持一些不在标准拖放模型中的特性。 它们是一些帮助实现拖拽多个项目和拖拽非文本内容（如文件）的便捷函数。想要了解更多信息，请参见 <a href="/zh-CN/docs/DragDrop/Dragging_and_Dropping_Multiple_Items">拖放多个项目</a>。另外，请查看 {{domxref("DataTransfer")}} 参考页以获取所有 <a href="/zh-CN/docs/Web/API/DataTransfer#Gecko_properties">Gecko 专有属性</a> 和 <a href="/zh-CN/docs/Web/API/DataTransfer#Gecko_methods">Gecko 专有方法</a>。</p>

<h2 id="基础">基础</h2>

<p>这一部分总结了给应用程序加入拖放功能的基本步骤。</p>

<h3 id="确定什么是可拖拽的">确定什么是可拖拽的</h3>

<p>让一个元素被拖拽需要添加 {{htmlattrxref("draggable")}} 属性，再加上全局事件处理函数{{domxref("GlobalEventHandlers.ondragstart","ondragstart")}}，如下面的示例代码所示：</p>

<pre class="brush: html notranslate">&lt;script&gt;
  function dragstart_handler(ev) {
    // Add the target element's id to the data transfer object
    ev.dataTransfer.setData("text/plain", ev.target.id);
  }

  window.addEventListener('DOMContentLoaded', () =&gt; {
    // Get the element by id
    const element = document.getElementById("p1");
    // Add the ondragstart event listener
    element.addEventListener("dragstart", dragstart_handler);
  });
&lt;/script&gt;

&lt;p id="p1" draggable="true"&gt;This element is draggable.&lt;/p&gt;</pre>

<p>查看更多 <a href="/zh-CN/docs/Web/HTML/Global_attributes/draggable">draggable 属性</a> 和 <a href="/zh-CN/docs/Web/Guide/HTML/Drag_operations#draggableattribute">拖拽操作指南</a>。</p>

<h3 id="定义拖拽数据">定义拖拽数据</h3>

<p>应用程序可以在拖拽操作中包含任意数量的数据项。每个数据项都是一个 {{domxref("DOMString","string")}} 类型，典型的 MIME 类型，如：<code>text/html</code>。</p>

<p>每个 {{domxref("DragEvent","drag event")}} 都有一个{{domxref("DragEvent.dataTransfer","dataTransfer")}} 属性，其中保存着事件的数据。这个属性（{{domxref("DataTransfer")}} 对象）也有管理拖拽数据的方法。{{domxref("DataTransfer.setData","setData()")}} 方法为拖拽数据添加一个项，如下面的示例代码所示：</p>

<pre class="brush: js notranslate">function dragstart_handler(ev) {
  // 添加拖拽数据
  ev.dataTransfer.setData("text/plain", ev.target.innerText);
  ev.dataTransfer.setData("text/html", ev.target.outerHTML);
  ev.dataTransfer.setData("text/uri-list", ev.target.ownerDocument.location.href);
}
</pre>

<p>查看 <a href="/zh-CN/docs/DragDrop/Recommended_Drag_Types">推荐拖拽类型</a> 了解可拖拽的常见数据类型（如文本、HTML、链接和文件），移步 <a href="/zh-CN/docs/Web/Guide/HTML/Drag_operations#dragdata">拖拽数据</a> 获取更多有关拖拽数据的信息。</p>

<h3 id="定义拖拽图像">定义拖拽图像</h3>

<p>拖拽过程中，浏览器会在鼠标旁显示一张默认图片。当然，应用程序也可以通过 {{domxref("DataTransfer.setDragImage","setDragImage()")}} 方法自定义一张图片，如下面的例子所示。</p>

<pre class="brush: js notranslate">function dragstart_handler(ev) {
  // Create an image and then use it for the drag image.
  // NOTE: change "example.gif" to a real image URL or the image
  // will not be created and the default drag image will be used.
  var img = new Image();
  img.src = 'example.gif';
  ev.dataTransfer.setDragImage(img, 10, 10);
}
</pre>

<p>欲了解更多关于拖拽图像的信息，见 <a href="/zh-CN/docs/DragDrop/Drag_Operations#dragfeedback">设置拖拽图像</a>。</p>

<h3 id="定义拖拽效果">定义拖拽效果</h3>

<p>{{domxref("DataTransfer.dropEffect","dropEffect")}} 属性用来控制拖放操作中用户给予的反馈。它会影响到拖拽过程中浏览器显示的鼠标样式。比如，当用户悬停在目标元素上的时候，浏览器鼠标也许要反映拖放操作的类型。</p>

<p>有 3 个效果可以定义：</p>

<ol>
 <li><strong><code>copy</code></strong> 表明被拖拽的数据将从它原本的位置拷贝到目标的位置。</li>
 <li><strong><code>move</code></strong> 表明被拖拽的数据将被移动。</li>
 <li><strong><code>link</code></strong> 表明在拖拽源位置和目标位置之间将会创建一些关系表格或是连接。</li>
</ol>

<p>在拖拽过程中，拖拽效果也许会被修改以用于表明在具体位置上具体效果是否被允许，如果允许，在该位置则被允许放置。</p>

<p>以下例子表明如何使用该属性。</p>

<pre class="brush: js notranslate">function dragstart_handler(ev) {
  ev.dataTransfer.dropEffect = "copy";
}
</pre>

<p>查看 <a href="/zh-CN/docs/Web/Guide/HTML/Drag_operations#drageffects">拖拽效果</a> 更多细节。</p>

<h3 id="定义一个放置区">定义一个放置区</h3>

<p>当拖拽一个项目到 HTML 元素中时，浏览器默认不会有任何响应。想要让一个元素变成可释放区域，该元素必须设置 {{domxref("GlobalEventHandlers.ondragover","ondragover")}} 和 {{domxref("GlobalEventHandlers.ondrop","ondrop")}} 事件处理程序属性，下面的例子通过简单的事件处理展示了如何使用这些属性：</p>

<pre class="brush: html notranslate">&lt;script&gt;
function dragover_handler(ev) {
 ev.preventDefault();
 ev.dataTransfer.dropEffect = "move";
}
function drop_handler(ev) {
 ev.preventDefault();
 // Get the id of the target and add the moved element to the target's DOM
 var data = ev.dataTransfer.getData("text/plain");
 ev.target.appendChild(document.getElementById(data));
}
&lt;/script&gt;

&lt;p id="target" ondrop="drop_handler(event)" ondragover="dragover_handler(event)"&gt;Drop Zone&lt;/p&gt;
</pre>

<p>注意每个处理程序调用 {{domxref("Event.preventDefault","preventDefault()")}} 来阻止对这个事件的其它处理过程（如触点事件或指针事件）。</p>

<p>欲了解更多信息，参见 <a href="/zh-CN/docs/Web/Guide/HTML/Drag_operations#droptargets">指定释放目标</a>。</p>

<h3 id="处理放置效果">处理放置效果</h3>

<p>{{event("drop")}} 事件的处理程序是以程序指定的方法处理拖拽数据。一般，程序调用 {{domxref("DataTransfer.getData","getData()")}} 方法取出拖拽项目并按一定方式处理。程序意义根据 {{domxref("DataTransfer.dropEffect","dropEffect")}} 的值与/或可变更关键字的状态而不同</p>

<p>下面的例子展示了一个处理程序，从拖拽数据中获取事件源元素的 <code>id</code> 然后根据 <code>id</code> 移动源元素到目标元素：</p>

<pre class="brush: html notranslate">&lt;script&gt;
function dragstart_handler(ev) {
 // Add the target element's id to the data transfer object
 ev.dataTransfer.setData("application/my-app", ev.target.id);
 ev.dataTransfer.dropEffect = "move";
}
function dragover_handler(ev) {
 ev.preventDefault();
 ev.dataTransfer.dropEffect = "move"
}
function drop_handler(ev) {
 ev.preventDefault();
 // Get the id of the target and add the moved element to the target's DOM
 var data = ev.dataTransfer.getData("application/my-app");
 ev.target.appendChild(document.getElementById(data));
}
&lt;/script&gt;

&lt;p id="p1" draggable="true" ondragstart="dragstart_handler(event)"&gt;This element is draggable.&lt;/p&gt;
&lt;div id="target" ondrop="drop_handler(event)" ondragover="dragover_handler(event)"&gt;Drop Zone&lt;/div&gt;
</pre>

<p>更多信息请参见 <a href="/zh-CN/docs/Web/Guide/HTML/Drag_operations#drop">执行释放</a>。</p>

<h3 id="拖拽结束">拖拽结束</h3>

<p>拖拽操作结束时，在源元素（开始拖拽时的目标元素）上触发 {{event("dragend")}} 事件。不管拖拽是完成还是被取消这个事件都会被触发。{{event("dragend")}} 事件处理程序可以检查{{domxref("DataTransfer.dropEffect","dropEffect")}} 属性的值来确认拖拽成功与否。</p>

<p>更多关于处理拖拽结束的信息请参见 <a href="/zh-CN/docs/DragDrop/Drag_Operations#dragend">结束拖拽</a>。</p>

<h2 id="互操作性">互操作性</h2>

<p>在 <a href="/zh-CN/docs/Web/API/DataTransferItem#Browser_compatibility">数据交换对象接口的浏览器兼容性表</a> 中可以看到拖放在桌面浏览器中相对支持得比较完整（除了 {{domxref("DataTransferItem")}} 和 {{domxref("DataTransferItemList")}} 接口支持得较少）。这个数据也显示出拖放操作在移动浏览器中支持得非常弱。</p>

<h2 id="示例和演示">示例和演示</h2>

<ul>
 <li><a href="https://mdn.github.io/dom-examples/drag-and-drop/copy-move-DataTransfer.html">使用 <code>DataTransfer</code> 接口拷贝和移动元素</a></li>
 <li><a href="http://mdn.github.io/dom-examples/drag-and-drop/copy-move-DataTransferItemList.html">使用 <code>DataTransferListItem</code> 接口拷贝和移动元素</a></li>
 <li>拖放文件；仅 Firefox 支持：<a href="http://jsfiddle.net/9C2EF/">http://jsfiddle.net/9C2EF/</a></li>
 <li>拖放文件；所有浏览器支持：<a href="https://jsbin.com/hiqasek/edit?html,js,output">https://jsbin.com/hiqasek/</a></li>
 <li>使用了拖放 API 的停车小页面：<a href="https://park.glitch.me/">https://park.glitch.me/</a> （在 <a href="https://glitch.com/edit/#!/park">这里</a> 编辑）</li>
</ul>

<h2 id="规范">规范</h2>

{{Specifications}}

<h2 id="参见">参见</h2>

<ul>
 <li><a href="/zh-CN/docs/Web/API/HTML_Drag_and_Drop_API/Drag_operations">拖拽操作</a></li>
 <li><a href="/zh-CN/docs/Web/API/HTML_Drag_and_Drop_API/Multiple_items">拖放多个项目</a></li>
 <li><a href="/zh-CN/docs/Web/API/HTML_Drag_and_Drop_API/Recommended_drag_types">推荐拖拽元素类型</a></li>
 <li><a href="https://html.spec.whatwg.org/multipage/interaction.html#dnd">HTML5 Living Standard：HTML5 拖放操作</a></li>
 <li><a href="http://caniuse.com/#search=draganddrop">来自 CanIUse 的拖放兼容数据</a></li>
</ul>