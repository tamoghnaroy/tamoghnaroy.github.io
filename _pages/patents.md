---
layout: page
permalink: /patents/
title: patents
description: A full list of my patents - both issued and pending.
years: [2022, 2020]
nav: false
nav_order: 3
---
<!-- _pages/publications.md -->
<div class="publications">

{%- for y in page.years %}
  <h2 class="year">{{y}}</h2>
  {% bibliography -f patents -q @*[year={{y}} && issued={{true}}]* %}
{% endfor %}

<h2>Pending</h2>
{%- for y in page.years %}
  <h2 class="year">{{y}}</h2>
  {% bibliography -f patents -q @*[year={{y}} && issued!={{true}}]* %}
{% endfor %}
</div>





