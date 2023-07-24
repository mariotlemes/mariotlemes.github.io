---
layout: page
title: Projetos
permalink: /projetos/
nav: true
nav_order: 4
dropdown: false
years: [2023-2, 2023-1, 2022-2, 2022-1, 2021-2, 2021-1, 2020-2, 2020-1,2019-2, 2019-1, 2018-2, 2018-1, 2017-2, 2017-1, 2016-2, 2016-1, 2015-2, 2015-1, 2014-2]
# children: 
#   - title: Ensino
#     permalink: /ensino/
#   - title: divider
#   - title: Pesquisa
#     permalink: /pesquisa/
#   - title: divider
#   - title: Extensão
#     permalink: /extensao/
---

Abaixo estão os projetos de ensino, pesquisa e extensão realizados pelo professor <mark>Mario Lemes</mark> ao longo de sua carreira acadêmica.

<div class="publications">


{% for y in page.years  %}
  {% bibliography -f projetos -q @*[year={{y}}]* %}
{% endfor %}

<!-- {% for x in page.publisher  %}
  {%if x == 'UFG' %}
    <h4><mark>UFG</mark></h4>
  {% endif %}
{% endfor %} -->

</div>