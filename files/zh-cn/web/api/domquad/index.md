---
title: DOMQuad
slug: Web/API/DOMQuad
translation_of: Web/API/DOMQuad
---
<p>{{SeeCompatTable}}{{APIRef("Geometry Interfaces")}}</p>

<p>DOMQuad 是四 DOMPoints 的集合，用于定义任意四边形的角。返回 DOMQuads 允许 getBoxQuads () 即使存在任意 2D 或 3D 转换，也可以返回准确的信息。它有一个方便的边界属性返回 DOMRectReadOnly 的那些情况下，你只需要一个轴对齐的边框。</p>

<dl>
 <dt>{{domxref("DOMQuad.DOMQuad()")}}</dt>
 <dd>Creates a new <code>DOMQuad</code> object.</dd>
</dl>

<h2 id="Properties">Properties</h2>

<dl>
 <dt>p1,p2,p3,p4 {{readonlyinline}}</dt>
 <dd>are {{domxref("DOMPoint")}} objects for each of the <code>DOMQuad</code> object's four corners.</dd>
</dl>

<h2 id="Methods">Methods</h2>

<dl>
 <dt>{{domxref("DOMQuad.fromRect()")}}</dt>
 <dd>Returns a new <code>DOMQuad</code> object based on the passed set of coordinates.</dd>
 <dt>{{domxref("DOMQuad.fromQuad()")}}</dt>
 <dd>Returns a new <code>DOMQuad</code> object based on the passed set of coordinates.</dd>
 <dt>{{domxref("DOMQuad.getBounds()")}}</dt>
 <dd>Returns a {{domxref("DOMRect")}} object with the coordinates and dimensions of the <code>DOMQuad</code> object.</dd>
 <dt>{{domxref("DOMQuad.toJSON()")}}</dt>
 <dd>Returns a JSON representation of the <code>DOMQuad</code> object.</dd>
</dl>

<h2 id="Specifications">Specifications</h2>

{{Specifications}}

<h2 id="Browser_compatibility">Browser compatibility</h2>

<div>


<p>{{Compat("api.DOMQuad")}}</p>
</div>