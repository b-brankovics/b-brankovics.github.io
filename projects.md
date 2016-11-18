---
layout: page
title: Projects
permalink: /projects/
---

<h2 style="color: darkred"> Comming soon!</h2>
<ul class="page-list">
  {% for my_page in site.pages %}
    {% if my_page.title and my_page.title != "About" ||
        my_page.title and my_page.title != "Projects" ||
        my_page.title and my_page.title != "Blog posts" %}
      <li>

        <h2>
          <a class="page-link" href="{{ my_page.url | prepend: site.baseurl }}">{{ my_page.title }}</a>
        </h2>
      </li>
    {% endif %}
  {% endfor %}
</ul>
