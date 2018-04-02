---
layout: page
title: Material Informativo
permalink: /material-informativo/
---

<ul id="material-informativo" class="list-unstyled">
{% for material in site.material_informativo %}
  <li>
    <p class="category">{{material.categories}}</p>

    <h3><a href="{% if material.categories contains 'video' or material.categories contains 'archivo' %}{{material.share_url}}{% else %}{{material.url}}{% endif %}"{% if material.categories contains 'video' or material.categories contains 'archivo' %} target="_blank"{% endif %}>{{material.title}}</a></h3>
    <i class="fas fa-chevron-circle-right fa-2x"></i>
    <p class="description">{{material.description}}</p>
  </li>
{% endfor %}
</ul>