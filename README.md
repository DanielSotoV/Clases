# Clases

Repositorio de materiales de clase: Criptografía, Docker y Construcción de Sitios Web.

## 🌐 Sitio web

El sitio está publicado en GitHub Pages:
**<https://DanielSotoV.github.io/Clases/>**

### Configurar GitHub Pages

1. Ve a **Settings → Pages** en el repositorio.
2. Fuente: **Deploy from a branch**.
3. Rama: `main`, carpeta: `/docs`.
4. Guarda y espera 1–2 minutos para que el sitio quede activo.

### Ejecutar el sitio localmente

**Requisitos:** Ruby ≥ 3.0, Bundler.

```bash
cd docs
bundle install
bundle exec jekyll serve
```

El sitio quedará disponible en `http://localhost:4000/Clases/`.

### Editar contenido

| Archivo | Qué controla |
|---------|-------------|
| `docs/_config.yml` | Configuración global del sitio |
| `docs/_data/materias.yml` | Lista de materias y sus detalles |
| `docs/_data/tareas.yml` | Lista de tareas con estado y fecha de entrega |
| `docs/_data/calendario.yml` | Horario semanal y eventos importantes |
| `docs/_data/recursos.yml` | Recursos: apuntes, videos, repos, lecturas |
| `docs/assets/css/style.scss` | Estilos personalizados (sobre minima) |

---

## 📁 Estructura del repositorio

```
Clases/
├── Criptografia/      # Notebooks de Criptografía con Python
├── Docker/            # Notebooks de Docker y Contenedores
├── ConstruccionSitioWeb/ # Guía de GitHub Pages
└── docs/              # Sitio Jekyll (GitHub Pages)
    ├── _config.yml
    ├── _data/
    ├── assets/css/
    ├── materias/
    └── *.md
```
