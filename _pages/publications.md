---
layout: page
permalink: /publications/
title: publications
description:
years: [2025, 2024, 2023, 2022, 2019, 2016, 2015]
nav: true
nav_order: 2
---
<!-- _pages/publications.md -->
<div class="publications">
In reversed chronological order
{%- for y in page.years %}
  <h2 class="year">{{y}}</h2>
  {% bibliography -f papers -q @*[year={{y}}]* %}
{% endfor %}

</div>
