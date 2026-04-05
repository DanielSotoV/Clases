---
layout: home
title: "Panel Principal"
permalink: /
---

## Bienvenido al Portal de Clases

Aquí encontrarás todo lo que necesitas para gestionar tus materias, tareas y recursos académicos.

---

### Materias activas

{% for materia in site.data.materias %}
- **[{{ materia.nombre }}]({{ site.baseurl }}{{ materia.url }})** — {{ materia.descripcion_corta }}
{% endfor %}

---

### Tareas próximas

{% assign pendientes = site.data.tareas | where: "estado", "pendiente" %}
{% if pendientes.size > 0 %}
| Tarea | Materia | Entrega |
|-------|---------|---------|
{% for tarea in pendientes limit:5 %}| {{ tarea.nombre }} | {{ tarea.materia }} | {{ tarea.entrega }} |
{% endfor %}
{% else %}
*No hay tareas pendientes por el momento. ¡Buen trabajo!*
{% endif %}

---

### Accesos rápidos

<div class="quick-links">
  <a class="quick-card" href="{{ site.baseurl }}/materias/">Materias</a>
  <a class="quick-card" href="{{ site.baseurl }}/calendario">Calendario</a>
  <a class="quick-card" href="{{ site.baseurl }}/tareas">Tareas</a>
  <a class="quick-card" href="{{ site.baseurl }}/recursos">Recursos</a>
  <a class="quick-card" href="{{ site.baseurl }}/politicas">Políticas</a>
  <a class="quick-card" href="{{ site.baseurl }}/contacto">Contacto</a>
</div>

---

### Próximos eventos

{% for evento in site.data.calendario.eventos limit:4 %}
- **{{ evento.fecha }}** — {{ evento.descripcion }} *({{ evento.materia }})*
{% endfor %}
