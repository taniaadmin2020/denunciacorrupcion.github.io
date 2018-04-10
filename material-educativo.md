---
layout: material-educativo
title: Material Educativo
permalink: /material-educativo/
---

<h2 class="titulo">Material Educativo</h2>

{% assign material_informativo = site.material_informativo | reverse %}
{% for material in material_informativo %}
<div class="item-articulo">
  <span class="tipo">{{material.categories}}</span>
  <a href="{% if material.categories contains 'video' or material.categories contains 'archivo' %}{{material.share_url}}{% else %}{{material.url}}{% endif %}"{% if material.categories contains 'video' or material.categories contains 'archivo' %} target="_blank"{% endif %}><h3 class="titulo">{{material.title}}</h3></a>
  <p>{{material.description}}</p>
  <a class="ver"  href="{% if material.categories contains 'video' or material.categories contains 'archivo' %}{{material.share_url}}{% else %}{{material.url}}{% endif %}"{% if material.categories contains 'video' or material.categories contains 'archivo' %} target="_blank"{% endif %}>ver</a>
</div>
{% endfor %}