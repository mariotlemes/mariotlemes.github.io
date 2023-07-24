---
layout: page
permalink: /alunos/
title: Alunos
years: [Estágio, TCC]
description: Lista de alunos orientados pelo professor Mario Lemes
nav: true
nav_order: 1
heading: Alunos
---

<div class="publications">


 
 <!-- <!-- <br> -->
 <hr>
<!-- <span style="font-size:15px"> -->

<h4><mark>Atuais</mark></h4>
 
 {%- for y in page.years %}
  <!-- <h2 class="year">{{y}}</h2> -->
  {% bibliography -f atuais -q @*[year={{y}}]* %}
{% endfor %}

  <br>

 <hr>
<span style="font-size:15px">

<h4><mark>Formados</mark></h4>



<div class="publications">

{%- for y in page.years %}
  <!-- <h2 class="year">{{y}}</h2> -->
  {% bibliography -f anteriores -q @*[year={{y}}]* %}
{% endfor %}