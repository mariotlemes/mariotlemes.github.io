---
layout: page
permalink: /disciplinas_ministradas/
title: Disciplinas
description: Relação das disciplinas do Ensino Médio (Técnico Integrado e Educação de Jovens e Adultos - EJA), Ensino Superior e Pós-Graduação ministradas pelo professor Mario Lemes.
years: [2023-2, 2023-1, 2022-2, 2022-1, 2021-2, 2021-1, 2020-2, 2020-1,2019-2, 2019-1, 2018-2, 2018-1, 2017-2, 2017-1, 2016-2, 2016-1, 2015-2, 2015-1, 2014-2]
nav: true
nav_order: 2
heading: Disciplinas
---

<div class="publications">


{% for y in page.years  %}
	{% bibliography -f classes -q @*[year={{y}}]* %}
{% endfor %}

<!-- {% for x in page.publisher  %}
	{%if x == 'UFG' %}
		<h4><mark>UFG</mark></h4>
	{% endif %}
{% endfor %} -->

</div>