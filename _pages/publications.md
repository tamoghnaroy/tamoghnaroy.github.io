---
layout: page
permalink: /publications/
title: publications
description: A full list of my peer-reviewed articles. 
years: [2021, 2020, 2019, 2018, 2017, 2015, 2014, 2013]
# years: [1967, 1956, 1950, 1935, 1905]
nav: false
nav_order: 2
---
<!-- _pages/publications.md -->
<div class="publications">

{%- for y in page.years %}
  <h2 class="year">{{y}}</h2>
  {% bibliography -f papers -q @*[year={{y}}]* %}
{% endfor %}

</div>
