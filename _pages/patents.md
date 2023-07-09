---
layout: page
permalink: /patents/
title: patents
description: A full list of my patents - both issued and pending.
issued_years: [2023, 2022, 2020]
pending_years: [2022]
nav: false
nav_order: 3
---
<!-- _pages/publications.md -->
<div class="publications">

{%- for y in page.issued_years %}
  <h2 class="year">{{y}}</h2>
  {% bibliography -f patents -q @*[year={{y}} && issued={{true}}]* %}
{% endfor %}

<h2>Pending</h2>
{%- for y in page.pending_years %}
  <h2 class="year">{{y}}</h2>
  {% bibliography -f patents -q @*[year={{y}} && issued!={{true}}]* %}
{% endfor %}
</div>





