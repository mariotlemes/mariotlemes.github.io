---
layout: page
permalink: /alunos/
title: Orientações
years: [Estágio, TCC, Especialização, PIBIT]
description: Lista de alunos orientados pelo professor <mark>Mario Lemes</mark>.
nav: true
nav_order: 3
heading: Alunos
---

<div class="publications">


 
 <!-- <!-- <br> -->
 <hr>
<!-- <span style="font-size:15px"> -->

<h4>Em andamento</h4>
 
 {%- for y in page.years %}
  <!-- <h2 class="year">{{y}}</h2> -->
  {% bibliography -f atuais -q @*[year={{y}}]* %}
{% endfor %}

  <br>

 <hr>
<span style="font-size:15px">

<h4>Concluídas</h4>



<div class="publications">

{%- for y in page.years %}
  <!-- <h2 class="year">{{y}}</h2> -->
  {% bibliography -f anteriores -q @*[year={{y}}]* %}
{% endfor %}