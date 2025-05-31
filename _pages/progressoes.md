---
layout: page
title: Progressões
permalink: /progressoes/
years: [2025-1, 2024-2, 2024-1, 2023-2, 2023-1, 2022-2, 2022-1, 2021-2, 2021-1, 2020-2, 2020-1,2019-2, 2019-1, 2018-2, 2018-1, 2017-2, 2017-1, 2016-2, 2016-1, 2015-2, 2015-1, 2014-2]
description: Progressões do professor Mario Lemes.
nav: true
nav_order: 6
heading: Alunos
---
 <hr>

<span style="font-size:15px">

<h4>Em andamento</h4>

<div class="publications">

{% for y in page.years  %}
  {% bibliography -f progressao_atual -q @*[year={{y}}]* %}
{% endfor %}

</div>

  <br>

 <hr>
<span style="font-size:15px">

<h4>Concluídas</h4>


<div class="publications">

{%- for y in page.years %}
  <!-- <h2 class="year">{{y}}</h2> -->
  {% bibliography -f progressao_anterior -q @*[year={{y}}]* %}
{% endfor %}