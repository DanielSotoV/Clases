---
layout: page
title: "Calendario"
permalink: /calendario
---

## Horario semanal

| Día | Hora | Materia | Aula | Tipo |
|-----|------|---------|------|------|
{% for dia in site.data.calendario.horario %}{% for bloque in dia.bloques %}| **{{ dia.dia }}** | {{ bloque.hora }} | {{ bloque.materia }} | {{ bloque.aula }} | {{ bloque.tipo }} |
{% endfor %}{% endfor %}

---

## Eventos y fechas importantes

{% assign eventos = site.data.calendario.eventos %}

### Entregas

{% assign entregas = eventos | where: "tipo", "entrega" %}
{% for e in entregas %}
- **{{ e.fecha }}** — {{ e.descripcion }} `{{ e.materia }}`
{% endfor %}

### Exámenes

{% assign examenes = eventos | where: "tipo", "examen" %}
{% for e in examenes %}
- **{{ e.fecha }}** — {{ e.descripcion }} `{{ e.materia }}`
{% endfor %}

### Proyectos

{% assign proyectos = eventos | where: "tipo", "proyecto" %}
{% for e in proyectos %}
- **{{ e.fecha }}** — {{ e.descripcion }} `{{ e.materia }}`
{% endfor %}

---

> **Tip:** Agrega este calendario a tu aplicación favorita exportando los eventos manualmente o pidiéndole a tu profesor el archivo `.ics`.
