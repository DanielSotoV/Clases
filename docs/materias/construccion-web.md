---
layout: page
title: "Construcción de Sitios Web"
permalink: /materias/construccion-web
---

{% assign materia = site.data.materias | where: "url", "/materias/construccion-web" | first %}

{{ materia.descripcion }}

---

## Temas del curso

{% for tema in materia.temas %}
- {{ tema }}
{% endfor %}

---

## Clases y notebooks

| # | Tema | Notebook |
|---|------|----------|
| 1 | Sitio Web con GitHub Pages | [Ver notebook](https://github.com/DanielSotoV/Clases/blob/main/ConstruccionSitioWeb/SitioWeb_GitHub.ipynb) |

---

## Repositorio

[Ver todos los materiales en GitHub]({{ materia.repositorio }}){:target="_blank"}

---

## Tareas de esta materia

{% assign tareas_materia = site.data.tareas | where: "materia", "Construcción de Sitios Web" %}
{% for tarea in tareas_materia %}
- **[{{ tarea.estado | upcase }}]** {{ tarea.nombre }} — *Entrega: {{ tarea.entrega }}*
{% endfor %}
