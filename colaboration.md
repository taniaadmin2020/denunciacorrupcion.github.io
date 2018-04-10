---
layout: colaboradores
title: Colaboradores
permalink: /colaboradores/
---

<h2 class="titulo">{{page.title}}</h2>

{% for c in site.data.colaboradores %}
<div class="colaborador">
  <div class="row">
    <div class="col-md-4 logo">
      <img src="{{c.image}}" alt="{{c.name}}" class="img-fluid">
    </div>
    <div class="col-md-8">
      <h3>{{c.name}}</h3>
      <p>{{c.description}}</p>
    </div>
  </div>
</div>
{% endfor %}