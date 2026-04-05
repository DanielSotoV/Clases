---
layout: page
title: "Materias"
permalink: /materias/
---

Estas son las materias activas del semestre. Haz clic en cada tarjeta para ver el detalle, temas y recursos.

<div class="materias-grid">
{% for materia in site.data.materias %}
<div class="materia-card materia-{{ materia.color }}">
  <h3><a href="{{ site.baseurl }}{{ materia.url }}">{{ materia.nombre }}</a></h3>
  <p>{{ materia.descripcion_corta }}</p>
  <a class="btn-ver" href="{{ site.baseurl }}{{ materia.url }}">Ver materia →</a>
</div>
{% endfor %}
</div>
