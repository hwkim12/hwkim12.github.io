---
layout: page
permalink: /publications/
title: publications
description:
years: [2026, 2025, 2024, 2023, 2022, 2019, 2016, 2015]
nav: true
nav_order: 2
---

<div class="publications">

<h2 class="category">Under Review / Revision</h2>
{%- for y in page.years %}
  {%- capture bib_output %}{% bibliography -f papers -q @*[year={{y}},pubstate=submitted]* %}{% endcapture -%}
  {%- if bib_output != "" %}
  <h3 class="year">{{y}}</h3>
  {{ bib_output }}
  {%- endif %}
{% endfor %}

<h2 class="category">Published & Accepted</h2>
{%- for y in page.years %}
  {%- capture bib_output %}{% bibliography -f papers -q @*[year={{y}},pubstate=accepted]* %}{% endcapture -%}
  {%- if bib_output != "" %}
  <h3 class="year">{{y}}</h3>
  {{ bib_output }}
  {%- endif %}
{% endfor %}

</div>
