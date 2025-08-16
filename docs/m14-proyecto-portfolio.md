---
title: M14 · Proyecto A – Portfolio solo HTML
description: Proyecto final de portfolio personal estático solo con HTML.
---

# M14 · Proyecto A – Portfolio solo HTML

## Enunciado
Construye un portfolio personal estático solo con HTML, que presente quién eres, lo que haces y algunos proyectos. Debe ser navegable, accesible y semántico.

## Criterios de aceptación
- Estructura semántica: `header`, `nav`, `main`, `footer`, secciones claras.
- Páginas mínimas: `index.html`, `pages/sobre.html`, `pages/proyectos.html`, `pages/contacto.html`.
- Enlaces de navegación coherentes y descriptivos.
- Imágenes con `alt` adecuado.
- Formulario de contacto básico (nombre, email, mensaje).
- Metadatos: `charset`, `title`, `description`, `viewport`.
- Validación W3C sin errores graves.

## Estructura de archivos

```
/ (raíz)
  index.html
  /pages/
    sobre.html
    proyectos.html
    contacto.html
  /img/
    perfil.jpg
    proyecto-1.jpg
    proyecto-2.jpg
```

## Entregables
- Archivos `.html` y recursos en carpetas `pages/` e `img//`.
- Documento breve `README.html` (opcional) con notas.

## Rúbrica de evaluación (100 pts)
- Semántica y estructura (25)
- Accesibilidad básica (`alt`, `label`, jerarquía) (20)
- Navegación y rutas (15)
- Formularios básicos correctos (15)
- Metadatos y títulos/descripciones únicas (15)
- Organización y validación (10)

## Guía orientativa

```html
<!-- index.html (orientativo) -->
<!DOCTYPE html>
<html lang="es">
  <head>
    <meta charset="utf-8">
    <title>Nombre Apellido — Portfolio</title>
    <meta name="description" content="Portfolio de Nombre Apellido: proyectos, experiencia y contacto.">
    <meta name="viewport" content="width=device-width, initial-scale=1">
  </head>
  <body>
    <header>
      <h1>Nombre Apellido</h1>
      <nav>
        <a href="index.html">Inicio</a>
        <a href="pages/sobre.html">Sobre mí</a>
        <a href="pages/proyectos.html">Proyectos</a>
        <a href="pages/contacto.html">Contacto</a>
      </nav>
    </header>

    <main>
      <section id="intro">
        <h2>Introducción</h2>
        <p>Breve presentación.</p>
        <figure>
          <img src="img/perfil.jpg" alt="Foto de Nombre Apellido sonriendo">
          <figcaption>Foto de perfil.</figcaption>
        </figure>
      </section>

      <section id="destacados">
        <h2>Proyectos destacados</h2>
        <article>
          <h3>Proyecto 1</h3>
          <img src="img/proyecto-1.jpg" alt="Captura de pantalla de Proyecto 1">
          <p>Descripción breve del proyecto.</p>
        </article>
        <article>
          <h3>Proyecto 2</h3>
          <img src="img/proyecto-2.jpg" alt="Captura de pantalla de Proyecto 2">
          <p>Descripción breve del proyecto.</p>
        </article>
      </section>
    </main>

    <footer>
      <p>&copy; 2025 Nombre Apellido</p>
    </footer>
  </body>
</html>
```

## Solución orientativa
<details>
<summary>Ver sugerencias de contenido para páginas</summary>

- `pages/sobre.html`: Biografía con `h1`, secciones “Experiencia”, “Educación”, “Habilidades” (solo texto y listas).
- `pages/proyectos.html`: 3–6 `article` con `h2/h3`, descripción y una imagen cada uno con `alt`.
- `pages/contacto.html`: formulario con `label`/`input` (`text`, `email`) y `textarea` para mensaje; `required` donde aplique.

</details>
