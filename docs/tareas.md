---
layout: page
title: "Tareas"
permalink: /tareas
---

Aquí se listan todas las tareas organizadas por estado. Edita `_data/tareas.yml` para actualizar el contenido.

---

## Pendientes

{% assign pendientes = site.data.tareas | where: "estado", "pendiente" | sort: "entrega" %}
{% if pendientes.size > 0 %}
{% for tarea in pendientes %}
<div class="tarea-card tarea-pendiente">
  <div class="tarea-header">
    <span class="tarea-nombre">{{ tarea.nombre }}</span>
    <span class="tarea-badge badge-pendiente">Pendiente</span>
  </div>
  <p class="tarea-desc">{{ tarea.descripcion }}</p>
  <div class="tarea-meta">
    <span>{{ tarea.materia }}</span>
    <span>Entrega: <strong>{{ tarea.entrega }}</strong></span>
    <span>Prioridad: {{ tarea.prioridad }}</span>
  </div>
</div>
{% endfor %}
{% else %}
*No hay tareas pendientes. ¡Excelente!*
{% endif %}

---

## En progreso

{% assign en_progreso = site.data.tareas | where: "estado", "en progreso" | sort: "entrega" %}
{% if en_progreso.size > 0 %}
{% for tarea in en_progreso %}
<div class="tarea-card tarea-progreso">
  <div class="tarea-header">
    <span class="tarea-nombre">{{ tarea.nombre }}</span>
    <span class="tarea-badge badge-progreso">En progreso</span>
  </div>
  <p class="tarea-desc">{{ tarea.descripcion }}</p>
  <div class="tarea-meta">
    <span>{{ tarea.materia }}</span>
    <span>Entrega: <strong>{{ tarea.entrega }}</strong></span>
    <span>Prioridad: {{ tarea.prioridad }}</span>
  </div>
</div>
{% endfor %}
{% else %}
*No hay tareas en progreso actualmente.*
{% endif %}

---

## Completadas

{% assign completadas = site.data.tareas | where: "estado", "completada" | sort: "entrega" %}
{% if completadas.size > 0 %}
{% for tarea in completadas %}
<div class="tarea-card tarea-completada">
  <div class="tarea-header">
    <span class="tarea-nombre">{{ tarea.nombre }}</span>
    <span class="tarea-badge badge-completada">Completada</span>
  </div>
  <p class="tarea-desc">{{ tarea.descripcion }}</p>
  <div class="tarea-meta">
    <span>{{ tarea.materia }}</span>
    <span>Entregada: <strong>{{ tarea.entrega }}</strong></span>
  </div>
</div>
{% endfor %}
{% else %}
*Aún no hay tareas completadas.*
{% endif %}

---

> Para agregar o editar tareas, modifica el archivo `docs/_data/tareas.yml` en el repositorio.
