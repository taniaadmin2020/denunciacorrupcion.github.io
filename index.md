---
# You don't need to edit this file, it's empty on purpose.
# Edit theme's home layout instead if you wanna make some changes
# See: https://jekyllrb.com/docs/themes/#overriding-theme-defaults
layout: home
---
<div id="main-section" class="container-fluid">
  <div class="row">
    <div class="col-md-6">
      <h1>Qué es un ALAC?</h1>
      <p>ALAC es una oficina de Chile Transparente, Capítulo Chileno de Transparencia Internacional, que brinda asistencia legal gratuita a víctimas, testigos y/o denunciantes de corrupción de hechos que involucren a autoridades y/o funcionarios públicos.</p>
      <p>ALAC te permite denunciar cualquier hecho irregular o sospecha de acto corrupto que involucre a autoridades o funcionarios de alguna institución pública de la Administración del Estado.</p>
      <a href="#" class="btn btn-main-section">Leer más</a>
    </div>
    <div class="col-md-6">
      <div class="embed-responsive embed-responsive-16by9">
        <iframe width="560" height="315" src="//www.youtube.com/embed/wNA1jl9Si2k" frameborder="0" allow="autoplay; encrypted-media" allowfullscreen></iframe>
      </div>
    </div>
  </div>
</div>

<div id="denuncialos" class="container-fluid">
  <div class="row">
    <div class="col-md-6 col-md-offset-3 text-center">
      <h2>Haz tu denuncia</h2>
      <p>Lorem ipsum dolor sit amet, consectetur adipisicing elit. Ipsum recusandae expedita cum, rerum nisi asperiores adipisci eveniet, molestiae in dolorem sit praesentium molestias nulla rem repellat optio? Culpa, impedit, et?</p>
    </div>
    <div class="col-md-2 col-md-offset-4">
      <a href="#" class="btn btn-default">Cómo denunciar?</a>
    </div>
    <div class="col-md-2">
      <a href="#" class="btn btn-default">Buzón de denuncia</a>
    </div>
  </div>
</div>

<div class="container text-center">
  <h3>Material Informativo</h3>
  <div class="row">
    {% for mi in site.material_informativo %}
    <div class="col-md-4">
      <div class="panel panel-default">
        {% if mi.img_related %}
        <div class="panel-heading">
          <img src="{{mi.img_related}}" alt="{{mi.title}}" class="img-responsive">
        </div>
        {% endif %}
        <div class="panel-body">
          {{mi.categories}}
          <a href="{% if mi.categories contains 'video' or mi.categories contains 'archivo' %}{{mi.share_url}}{% else %}{{mi.url}}{% endif %}"{% if mi.categories contains 'video' or mi.categories contains 'archivo' %} target="_blank"{% endif %}>{{mi.title}}</a>
          <p>{{mi.description}}</p>
        </div>
      </div>

    </div>
    {% endfor %}
  </div>
  <a href="#" class="btn btn-default">Ver más material</a>
</div>

<div class="container-fluid text-center">
  <h4>Colaboradores</h4>
  <ul class="list-inline">
    <li><img src="" alt="colaborador 1"></li>
    <li><img src="" alt="colaborador 2"></li>
  </ul>
</div>