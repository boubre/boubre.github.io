---
layout: page
permalink: /publications/
title: publications
description: 
paper_years: [2023, 2022, 2021, 2020, 2019]
conf_years: [2022, 2020]
abs_years: [2024, 2021, 2020, 2019]
nav: true
---

<div class="publications">

<h1>journal publications</h1>
<h2 class="year">&nbsp;</h2>
{% bibliography -f papers -q @*[status=review]* %}
{% bibliography -f papers -q @*[status=maj-revision]* %}
{% bibliography -f papers -q @*[status=min-revision]* %}

{% for y in page.paper_years %}
  <h2 class="year">{{y}}</h2>
  {% bibliography -f papers -q @*[year={{y}}]* %}
{% endfor %}

<h1>conference proceedings</h1>
{% for y in page.conf_years %}
  <h2 class="year">{{y}}</h2>
  {% bibliography -f conf -q @*[year={{y}}]* %}
{% endfor %}

<h1>posters and abstracts</h1>
{% for y in page.abs_years %}
  <h2 class="year">{{y}}</h2>
  {% bibliography -f abstracts -q @*[year={{y}}]* %}
{% endfor %}

</div>
