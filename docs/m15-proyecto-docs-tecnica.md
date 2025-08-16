---
title: M15 · Proyecto B – Página de documentación técnica
description: Proyecto final de documentación técnica solo con HTML.
---

# M15 · Proyecto B – Página de documentación técnica

## Enunciado
Crea una mini documentación técnica de un tema que domines (por ejemplo, “Atajos del teclado de mi editor”). Debe incluir portada, índice de contenidos con anclas internas, varias secciones con encabezados, tablas si son útiles y ejemplos en `<pre><code>`.

## Criterios de aceptación
- `index.html` con portada, `nav`/índice con enlaces a secciones (`#id`).
- Estructura semántica clara: `main`, `section`, `article`.
- Uso de `pre`/`code` para ejemplos y tablas si corresponde.
- Metadatos y accesibilidad básica correctos.
- Validación W3C sin errores graves.

## Estructura de archivos

```
/ (raíz)
  index.html
  /pages/
    guia.html
  /img/
    diagrama.svg
```

## Entregables
- Páginas `.html` con índice y secciones enlazadas.
- Recursos asociados (imágenes/diagramas si aplica).

## Rúbrica (100 pts)
- Organización y semántica (25)
- Navegación interna por anclas (20)
- Claridad de ejemplos `pre`/`code` (20)
- Metadatos y accesibilidad (20)
- Validación y orden (15)

## Guía orientativa

```html
<!DOCTYPE html>
<html lang="es">
  <head>
    <meta charset="utf-8">
    <title>Guía de atajos del editor X</title>
    <meta name="description" content="Referencia rápida de atajos del editor X.">
    <meta name="viewport" content="width=device-width, initial-scale=1">
  </head>
  <body>
    <header>
      <h1>Guía de atajos del editor X</h1>
      <nav aria-label="Índice">
        <a href="#intro">Introducción</a>
        <a href="#edicion">Edición</a>
        <a href="#navegacion">Navegación</a>
      </nav>
    </header>

    <main>
      <section id="intro">
        <h2>Introducción</h2>
        <p>Esta guía resume atajos comunes…</p>
      </section>

      <section id="edicion">
        <h2>Edición</h2>
        <table>
          <caption>Atajos de edición</caption>
          <thead>
            <tr><th scope="col">Acción</th><th scope="col">Atajo</th></tr>
          </thead>
          <tbody>
            <tr><th scope="row">Copiar</th><td>Ctrl+C</td></tr>
            <tr><th scope="row">Pegar</th><td>Ctrl+V</td></tr>
          </tbody>
        </table>
        <pre><code>Bloque de ejemplo</code></pre>
      </section>

      <section id="navegacion">
        <h2>Navegación</h2>
        <p>Usa el índice para saltar entre secciones.</p>
      </section>
    </main>

    <footer>
      <p>&copy; 2025 Tu Nombre</p>
    </footer>
  </body>
</html>
```

## Solución orientativa
<details>
<summary>Ver recomendaciones</summary>

- Añade una `figure` con un diagrama `svg` explicativo (con `figcaption`).
- Crea un glosario final con `dl/dt/dd` de términos clave.
- Asegura `title` y `description` únicos por página.

</details>
