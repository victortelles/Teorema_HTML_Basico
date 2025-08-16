# Teorema / Curso HTML Básico

Material introductorio de HTML (solo HTML, sin CSS ni JavaScript) para principiantes absolutos. Incluye 16 módulos con teoría, ejemplos, ejercicios, retos, mini-quizzes, proyectos finales y apéndices (glosario, cheatsheet, recursos).

Demo en Netlify:
- https://friendly-cupcake-3e4414.netlify.app/

Aviso
- Contenido generado con asistencia de IA para fines educativos.
- Enfocado en buenas prácticas básicas, semántica, accesibilidad esencial y validación.

Estructura
- `mkdocs.yml` (configuración del sitio)
- `docs/` (contenido en Markdown)
- `site/` (salida estática generada por MkDocs)

Requisitos
- Python 3.11+ (sugerido)
- Dependencias en `requeriments.txt`: MkDocs, Material for MkDocs, etc.

Uso local
1. Instalar dependencias: `pip install -r requeriments.txt`
2. Servir en local: `mkdocs serve` (o `python -m mkdocs serve`)
3. Construir estático: `mkdocs build` (o `python -m mkdocs build`)

Despliegue (Netlify)
- Build command: `pip install -r requeriments.txt && python -m mkdocs build --clean`
- Publish directory: `site`
- Alternativas: GitHub Pages (`mkdocs gh-deploy`), Vercel (usar `vercel.json`).

Créditos y licencia
- Autoría: generada por IA con curaduría humana.
- Uso educativo. Consulta MDN y WHATWG para referencias oficiales.
