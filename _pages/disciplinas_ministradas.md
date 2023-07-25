---
layout: page
permalink: /disciplinas_ministradas/
title: Disciplinas
description: Abaixo estão as disciplinas do Ensino Médio do Técnico Integrado e Educação de Jovens e Adultos - EJA, Ensino Superior e Pós-graduação) ministradas pelo professor <mark>Mario Lemes</mark>.
# years: [Fall 2023, Spring 2023, Fall 2022, Spring 2022, Fall 2021, Spring 2021, Fall 2020, Spring 2020, Fall 2019, Spring 2019,  Fall 2018, Spring 2018, Fall 2017, Spring 2017, Fall 2016, Spring 2016, Fall 2015, Spring 2015, Fall 2014, Spring 2014, Fall 2013]
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