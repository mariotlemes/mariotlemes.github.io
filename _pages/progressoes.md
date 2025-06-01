---
layout: page
title: Progressões
permalink: /progressoes/
years: [2025, 2024, 2024, 2023, 2022, 2021, 2020, 2019, 2018, 2017, 2016, 2015, 2014]
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