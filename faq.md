---
layout: faqs_layout
title: Preguntas frecuentes
permalink: /preguntas-frecuentes/
---

<div class="col-sm-9 col-sm-offset-2">
<div class="panel-group" id="accordion" role="tablist" aria-multiselectable="true">
  {% assign preguntas = site.data.faqs  %}
  {% for p in preguntas %}
    <div class="panel panel-default">
      <div class="panel-heading" role="tab" id="headingOne-{{ p.id }}">
        <h4 class="panel-title">
          <a role="button" data-toggle="collapse" data-parent="#accordion" href="#collapseOne-{{ p.id }}" aria-expanded="true" aria-controls="collapseOne-{{ p.id }}">
            {{ p.pregunta }}
          </a>
        </h4>
      </div>
      <div id="collapseOne-{{ p.id }}" class="panel-collapse collapse" role="tabpanel" aria-labelledby="headingOne">
        <div class="panel-body">
          <p>{{ p.respuesta }}</p>
        </div>
      </div>
    </div>
  {% endfor %}

</div>
</div>
