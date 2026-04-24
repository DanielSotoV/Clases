---
layout: page
title: "Docker y Contenedores"
permalink: /materias/docker
---

{% assign materia = site.data.materias | where: "url", "/materias/docker" | first %}

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
| 1 | Introducción a Docker | [Ver notebook](https://github.com/DanielSotoV/Clases/blob/main/Docker/Clase_1_Introduccion_a_Docker.ipynb) |
| 2 | Docker Avanzado | [Ver notebook](https://github.com/DanielSotoV/Clases/blob/main/Docker/Clase_2_Docker_Avanzado.ipynb) |
| 3 | Orquestación y Operaciones | [Ver notebook](https://github.com/DanielSotoV/Clases/blob/main/Docker/Clase_3_Orquestacion_y_Operaciones_Docker.ipynb) |

---

## Repositorio

[Ver todos los materiales en GitHub]({{ materia.repositorio }}){:target="_blank"}

---

## Tareas de esta materia

{% assign tareas_materia = site.data.tareas | where: "materia", "Docker y Contenedores" %}
{% for tarea in tareas_materia %}
- **[{{ tarea.estado | upcase }}]** {{ tarea.nombre }} — *Entrega: {{ tarea.entrega }}*
{% endfor %}
