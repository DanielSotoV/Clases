---
layout: page
title: "🔐 Criptografía con Python"
permalink: /materias/criptografia
---

{% assign materia = site.data.materias | where: "url", "/materias/criptografia" | first %}

{{ materia.descripcion }}

---

## 📋 Temas del curso

{% for tema in materia.temas %}
- {{ tema }}
{% endfor %}

---

## 📓 Clases y notebooks

| # | Tema | Notebook |
|---|------|----------|
| 1 | Fundamentos de Criptografía | [Ver notebook](https://github.com/DanielSotoV/Clases/blob/main/Criptografia/Clase1_Fundamentos_Criptografia.ipynb) |
| 2 | Aritmética Modular | [Ver notebook](https://github.com/DanielSotoV/Clases/blob/main/Criptografia/Clase2_Aritmetica_Modular.ipynb) |
| 3 | Criptografía Simétrica – Bloques | [Ver notebook](https://github.com/DanielSotoV/Clases/blob/main/Criptografia/Clase3_Criptografia_Simetrica_Bloques.ipynb) |
| 4 | Criptografía de Flujo y MACs | [Ver notebook](https://github.com/DanielSotoV/Clases/blob/main/Criptografia/Clase4_Criptografia_Flujo_y_MACs.ipynb) |
| 5 | Funciones Hash Criptográficas | [Ver notebook](https://github.com/DanielSotoV/Clases/blob/main/Criptografia/Clase5_Funciones_Hash_Criptograficas.ipynb) |
| 6 | Criptografía Asimétrica – RSA | [Ver notebook](https://github.com/DanielSotoV/Clases/blob/main/Criptografia/Clase6_Criptografia_Asimetrica_RSA.ipynb) |
| 7 | Curvas Elípticas (ECC) | [Ver notebook](https://github.com/DanielSotoV/Clases/blob/main/Criptografia/Clase7_Criptografia_Curvas_Elipticas_ECC.ipynb) |

---

## 🔗 Repositorio

[Ver todos los materiales en GitHub]({{ materia.repositorio }}){:target="_blank"}

---

## ✅ Tareas de esta materia

{% assign tareas_materia = site.data.tareas | where: "materia", "Criptografía con Python" %}
{% for tarea in tareas_materia %}
- **[{{ tarea.estado | upcase }}]** {{ tarea.nombre }} — *Entrega: {{ tarea.entrega }}*
{% endfor %}
