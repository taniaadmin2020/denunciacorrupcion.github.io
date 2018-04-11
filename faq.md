---
layout: faqs_layout
title: Preguntas frecuentes
permalink: /preguntas-frecuentes/
---
<main>
  <section id="contenido">
    <div class="container-fluid">
      <div class="row no-gutters">
        <div class="col-lg-6 text-left alac">
          <div class="row no-gutters">
            <div class="col-lg-2 d-none d-lg-block d-xl-block">
              <ul class="redes">
                {% include rrss.html %}
              </ul>
              <div class="col-lg-6">
              </div>
            </div>
          </div>
        </div>
      </div>
      <div class="container">
        <div class="row">
          <div class="col-lg-10 offset-lg-1 preguntas">
            <h2 class="titulo">Preguntas Frecuentes</h2>
            <div id="accordion" class="accordion">
              <div class="card mb-0">
              {% assign preguntas = site.data.faqs  %}
              {% for p in preguntas %}
                <div class="card-header collapsed" data-toggle="collapse" href="#collapse-0{{ p.id }}" aria-expanded="false">
                  <a class="card-title">
                    {{ p.pregunta }}
                  </a>
                </div>
                <div id="collapse-0{{ p.id }}" class="card-body collapse" data-parent="#accordion" >
                  <p>
                    {{ p.respuesta | markdownify}}
                    <ul>
                    {% for i in p.items %}
                    <li> {{ i.item | markdownify }} </li>
                    {% endfor %}
                    </ul>
                  </p>
                </div>
                {% endfor %}
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </section>
  <!-- Bootstrap core JavaScript -->
  <script src="/assets/vendor/jquery/jquery.min.js"></script>
  <script src="/assets/vendor/bootstrap/js/bootstrap.bundle.min.js"></script>

  <script>
    function toggleIcon(e) {
      $(e.target)
          .prev('.panel-heading')
          .find(".more-less")
          .toggleClass('glyphicon-plus glyphicon-minus');
    }
    $('.panel-group').on('hidden.bs.collapse', toggleIcon);
    $('.panel-group').on('shown.bs.collapse', toggleIcon);

  </script>
</main>
