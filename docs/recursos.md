---
layout: page
title: "Recursos"
permalink: /recursos
---

Colección de materiales de estudio organizados por tipo. Edita `_data/recursos.yml` para agregar tus propios recursos.

---

## Apuntes y Notebooks

{% for recurso in site.data.recursos.apuntes %}
- {{ recurso.tipo | capitalize }} · **[{{ recurso.nombre }}]({{ recurso.url }}){:target="_blank"}** `{{ recurso.materia }}`
{% endfor %}

---

## Videos

{% for video in site.data.recursos.videos %}
- **[{{ video.nombre }}]({{ video.url }}){:target="_blank"}** `{{ video.materia }}`
{% endfor %}

---

## Repositorios y herramientas

{% for repo in site.data.recursos.repositorios %}
- **[{{ repo.nombre }}]({{ repo.url }}){:target="_blank"}** — {{ repo.descripcion }}
{% endfor %}

---

## Lecturas recomendadas

{% for lectura in site.data.recursos.lecturas %}
- {{ lectura.tipo | capitalize }} · **[{{ lectura.nombre }}]({{ lectura.url }}){:target="_blank"}** `{{ lectura.materia }}`
{% endfor %}

---

> ¿Tienes un recurso útil? Ábrelo como issue o pull request en el repositorio.
