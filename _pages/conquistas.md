---
layout: page
permalink: /conquistas/
title: Conquistas
description: Lista de conquistas do professor Mario Lemes.
nav: true
nav_order: 6
years: [2023-2, 2023-1, 2022-2, 2022-1, 2021-2, 2021-1, 2020-2, 2020-1,2019-2, 2019-1, 2018-2, 2018-1, 2017-2, 2017-1, 2016-2, 2016-1, 2015-2, 2015-1, 2014-2, 2014-1, 2013-2]
---

<hr>

<span style="font-size:15px">

<h4>Homenagens</h4>


<div class="publications">

{% for y in page.years  %}
  {% bibliography -f homenagens -q @*[year={{y}}]* %}
{% endfor %}

</div>

<span style="font-size:15px">

<hr>

<h4>Aprovação em concurso público</h4>


<div class="publications">

{% for y in page.years  %}
  {% bibliography -f aprovacao_concurso -q @*[year={{y}}]* %}
{% endfor %}

</div>


