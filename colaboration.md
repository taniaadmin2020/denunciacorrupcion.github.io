---
layout: page
title: Colaboradores
permalink: /colaboradores/
---

<table class="table">
  <thead>
    <tr>
      <th>Logo</th>
      <th>Nombre</th>
      <th>Descripcion</th>
    </tr>
  </thead>
  <tbody>
    {% for c in site.data.colaboradores %}
    <tr>
      <td><img src="{{c.image}}" alt="{{c.name}}" class="img-responsive"></td>
      <td>{{c.name}}</td>
      <td>{{c.description}}</td>
    </tr>
    {% endfor %}
  </tbody>
</table>