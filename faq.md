---
layout: page
title: Preguntas frecuentes
permalink: /preguntas-frecuentes/
---

<div class="panel-group" id="accordion" role="tablist" aria-multiselectable="true">
  {% assign preguntas = site.data.faqs  %}
  {% for p in preguntas %}
    <div class="panel panel-default">
      <div class="panel-heading" role="tab" id="headingOne">
        <h4 class="panel-title">
          <a role="button" data-toggle="collapse" data-parent="#accordion" href="#collapseOne" aria-expanded="true" aria-controls="collapseOne">
            {{ p.pregunta }}
          </a>
        </h4>
      </div>
      <div id="collapseOne" class="panel-collapse collapse" role="tabpanel" aria-labelledby="headingOne">
        <div class="panel-body">
          <p>{{ p.respuesta }}</p>
        </div>
      </div>
    </div>
  {% endfor %}

</div>
