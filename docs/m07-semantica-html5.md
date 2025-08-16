---
title: M07 · Semántica HTML5 esencial
description: Estructurar la página con header, nav, main, section, article, aside, footer, figure y figcaption.
---

# M07 · Semántica HTML5 esencial

## Objetivos
- Estructurar páginas con `<header>`, `<nav>`, `<main>`, `<section>`, `<article>`, `<aside>`, `<footer>`.
- Usar `<figure>` y `<figcaption>` para contenido ilustrado.
- Comprender cómo la semántica mejora accesibilidad y SEO básico.

## Prerrequisitos y duración
- Prerrequisitos: M00–M06.
- Duración estimada: 75–105 minutos.

## Resumen teórico
La semántica describe el significado del contenido. HTML5 introdujo elementos para estructurar documentos de forma más clara:

- `<header>`: cabecera de una página o sección (título, logo, navegación secundaria).
- `<nav>`: sección de navegación con enlaces principales.
- `<main>`: contenido principal único de la página (debe aparecer una sola vez).
- `<section>`: agrupa contenido temático dentro de una parte del documento; suele llevar encabezado propio.
- `<article>`: contenido independiente/autocontenido (noticia, entrada de blog, tarjeta).
- `<aside>`: contenido relacionado pero secundario (barras laterales, notas).
- `<footer>`: pie de página o sección (créditos, enlaces legales).
- `<figure>` agrupa contenido ilustrativo con `<figcaption>` como leyenda.

Una página típica incluye un `header` con `nav`, un `main` con varias `section` o `article`, y un `footer`. Usa encabezados jerárquicos adecuados en cada sección para mejorar la navegación por lectores de pantalla.

## Ejemplos comentados

```html
<header>
  <h1>Mi Sitio</h1>
  <nav>
    <a href="index.html">Inicio</a>
    <a href="pages/sobre.html">Sobre mí</a>
    <a href="pages/contacto.html">Contacto</a>
  </nav>
</header>

<main>
  <article>
    <header>
      <h2>Última publicación</h2>
      <p>Publicado el <time datetime="2025-08-15">15/08/2025</time></p>
    </header>
    <p>Contenido del artículo...</p>
  </article>

  <section>
    <h2>Galería</h2>
    <figure>
      <img src="img/paisaje.jpg" alt="Paisaje montañoso al atardecer">
      <figcaption>Paisaje al atardecer.</figcaption>
    </figure>
  </section>
</main>

<aside>
  <h2>Notas</h2>
  <p>Enlaces útiles y anuncios.</p>
</aside>

<footer>
  <p>&copy; 2025 Mi Sitio</p>
</footer>
```

## Ejercicios guiados
1) Reestructura `index.html` para incluir `header`, `nav`, `main` y `footer`.
2) Dentro de `main`, agrega una `section` con `h2` y un `article` con `h2`.
3) Inserta una `figure` con imagen y `figcaption`.

## Retos
- Reto: Crea `pages/blog.html` con tres `article` autocontenidos (cada uno con su `header` y `h3`), y un `aside` con enlaces a artículos populares.

## Mini quiz
1) Verdadero/Falso: Puede haber múltiples `<main>` por documento.  
2) ¿Qué etiqueta representa contenido autocontenido, como una noticia?  
3) ¿Qué etiqueta usas para agrupar ilustraciones con una leyenda?  
4) ¿Dónde ubicarías enlaces de navegación principales?  
5) Completa: Contenido secundario relacionado va en `_____`.

### Respuestas
1) Falso  2) `<article>`  3) `<figure>` + `<figcaption>`  4) `<nav>`  5) `<aside>`

## Checklist
- Usas una sola etiqueta `<main>`.
- Estructuras con `section`/`article` y encabezados claros.
- Añades `figure/figcaption` cuando corresponde.

## Errores comunes
- Usar `div` genéricos en lugar de semántica disponible (aunque `div` existe, aquí priorizamos semántica).
- Colocar navegación fuera de un contexto identificable.
- Omitir encabezados en secciones, dificultando la navegación.

## Referencias
- MDN: Estructura semántica — https://developer.mozilla.org/es/docs/Glossary/Semantics  
- MDN: `<main>` — https://developer.mozilla.org/es/docs/Web/HTML/Element/main  
- WHATWG: Sections — https://html.spec.whatwg.org/multipage/sections.html
