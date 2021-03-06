---
layout: default
title: Крестики-нолики на CSS
type: post

tags: [experiments]

image: http://img-fotki.yandex.ru/get/9104/5091629.9a/0_7ec6c_5867b098_orig
desc: Довольно странный вариант игры, мне хотелось понять как ещё можно сымитировать игровую логику.

links:
- url: /go-and-css-next-attempt
  name: Игра Го на CSS∶ ещё одна попытка
---

Довольно странный вариант игры. <!--more-->
Мне хотелось понять как ещё можно сымитировать игровую логику.

Правда, без капельки JS всё-же не обошлось: я не обнаружила способ сбрасывать игру и возложила это на JS. Если попытаться обойтись совсем без него, можно было бы просто перегружать страницу.

Результат игры обрабатывается с помощью CSS.
Игра заканчивается при однозначном выигрыше либо при ничьей и полностью заполненном поле.

<p data-height="450" data-theme-id="0" data-slug-hash="lnAuh" data-default-tab="result" class='codepen'>See the Pen <a href='http://codepen.io/yoksel/pen/lnAuh'>lnAuh</a> by yoksel (<a href='http://codepen.io/yoksel'>@yoksel</a>) on <a href='http://codepen.io'>CodePen</a>.</p>
<script async src="//codepen.io/assets/embed/ei.js"></script>

Теоретически можно было бы учитывать ничью до заполнения поля, это возможно, но код будет совсем длинным, так что я отказалась от этой затеи.

Ещё следовало бы сделать плавным появление панели с результатом, но у меня не получилось совладать с поведением псевдоэлементов. Анимировались некоторые свойства, которые точно об этом никто не просил, например <code>text-indent</code>. Для более аккуратной анимации проишлось бы увеличить код на две трети, или я просто не сообразила как это можно решить изящнее.

Я думаю, этот способ можно использовать и для полей побольше, хотя в этом случае селекторы будут километровыми, и без препроцессоров уже точно не обойтись не получится.