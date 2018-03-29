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
      <a href="#" class="btn btn-como-denunciar">Cómo denunciar?</a>
    </div>
    <div class="col-md-2">
      <a href="//buzon.denunciacorrupcion.cl/#/" class="btn btn-denuncia">Buzón de denuncia</a>
    </div>
  </div>
</div>

<div id="material-informativo" class="container text-center">
  <h3>Material Informativo</h3>
  <div class="row">
    {% for mi in site.material_informativo %}
    <div class="col-md-4">
      <div class="panel panel-default">
        <div class="panel-heading">
          <img src="{% if mi.img_related %}{{mi.img_related}}{% else %}https://via.placeholder.com/1024x768{% endif %}" alt="{{mi.title}}" class="img-responsive">
        </div>
        <div class="panel-body">
          <a href="{% if mi.categories contains 'video' or mi.categories contains 'archivo' %}{{mi.share_url}}{% else %}{{mi.url}}{% endif %}"{% if mi.categories contains 'video' or mi.categories contains 'archivo' %} target="_blank"{% endif %}>{{mi.title}}</a>
          <p>{{mi.description}}</p>
        </div>
      </div>

    </div>
    {% endfor %}
  </div>
  <a href="#" class="btn btn-default">Ver más material</a>
</div>

<div id="colaboradores" class="container-fluid text-center">
  <h3>Colaboradores</h3>
  <ul class="list-inline">
    {% assign colaboradores = site.data.colaboradores %}
    {% for c in colaboradores %}
    <li><img src="{{c.image}}" alt="{{c.name}}" class="img-responsive"></li>
    {% endfor %}
  </ul>
</div>