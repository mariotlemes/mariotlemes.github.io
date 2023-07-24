---
layout: page
permalink: /ensino/
title: Ensino
description: Lista de Projetos de Ensino realizados pelo professor Mario Lemes categorizados em ordem cronológica reversa.
nav: false
nav_order: 1
---


<div class="publications">


{% for y in page.years  %}
	{% bibliography -f ensino -q @*[year={{y}}]* %}
{% endfor %}

<!-- {% for x in page.publisher  %}
	{%if x == 'UFG' %}
		<h4><mark>UFG</mark></h4>
	{% endif %}
{% endfor %} -->

</div>