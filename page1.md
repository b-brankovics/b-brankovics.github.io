---
layout: page
title: Page1
permalink: /page1/
---

This is the first page created for this site.

List of pages:
{% for my_page in site.pages %}
{{my_page.title}}
{% endfor %}

Second list of pages:
<ul>
  {% for my_page in site.pages %}
    <li>{{my_page.title}}</li>
  {% endfor %}
</ul>
