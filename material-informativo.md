---
layout: page
title: Material Informativo
permalink: /material-informativo/
---

<ul class="list-unstyled">
{% for material in site.material_informativo %}
  <li>
    <p>{{material.categories}}</p>
    <p><a href="{% if material.categories contains 'video' or material.categories contains 'archivo' %}{{material.share_url}}{% else %}{{material.url}}{% endif %}"{% if material.categories contains 'video' or material.categories contains 'archivo' %} target="_blank"{% endif %}>{{material.title}}</a></p>
    <p>{{material.description}}</p>
  </li>
{% endfor %}
</ul>