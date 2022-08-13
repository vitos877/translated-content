---
title: ':enabled'
slug: 'Web/CSS/:enabled'
translation_of: 'Web/CSS/:enabled'
---
<div>{{CSSRef}}</div>

<h2 id="Описание">Описание</h2>

<p>CSS <a href="/ru/docs/Web/CSS/Псевдо-классы" title="Pseudo-classes">псевдокласс</a> <code>:enabled</code> находит любой включённый элемент. Элемент включён, если его можно активировать (например, выбрать, нажать на него или ввести текст) или поставить фокус. У элемента также есть отключённое состояние, когда его нельзя активировать или сфокусировать.</p>

<h2 id="Пример">Пример</h2>

<p>Следующий пример делает цвет текста средне-зелёного оттенка, когда поле включено, и серым, когда отключено. Это позволяет понимать пользователю какие элементы интерактивны, а какие нет.</p>

<div id="Enabled_Disabled_Inputs_Example">
<p>Следующий HTML...</p>

<pre class="brush:html">    &lt;form action="url_of_form"&gt;
      &lt;label for="FirstField"&gt;Первое поле (включено):&lt;/label&gt; &lt;input type="text" id="FirstField" value="Lorem"&gt;&lt;br /&gt;
      &lt;label for="SecondField"&gt;Второе поле (отключено):&lt;/label&gt; &lt;input type="text" id="SecondField" value="Ipsum" disabled="disabled"&gt;&lt;br /&gt;
      &lt;input type="button" value="Submit" /&gt;
    &lt;/form&gt;
  </pre>

<p>...используем со следующим CSS...</p>

<pre class="brush:css; highlight:[1,4]">input:enabled {
  color: #22AA22;
}
input:disabled {
  color: #D9D9D9;
}
  </pre>

<p>...результат:</p>

<div>{{EmbedLiveSample("Enabled_Disabled_Inputs_Example",550,95)}}</div>

<div>Заметьте, цвет текста кнопки также зелёный, так как она тоже включена.</div>
</div>

<h2 id="Спецификации">Спецификации</h2>

{{Specifications}}

<h2 id="Поддержка_браузерами">Поддержка браузерами</h2>

<p>{{Compat}}</p>

<h2 id="Смотрите_также">Смотрите также</h2>

<ul>
 <li>{{Cssxref(":disabled")}}</li>
</ul>