---
title: M00 · Introducción a la Web y a HTML
description: Qué es la Web, cómo funciona, qué es HTML y cómo se estructura una página.
---

# M00 · Introducción a la Web y a HTML

## Objetivos de aprendizaje
- Entender qué es la Web y cómo funciona el flujo solicitud/respuesta.
- Comprender qué es HTML y su rol en la construcción de páginas.
- Diferenciar contenido, presentación y comportamiento.
- Preparar el entorno de trabajo: editor, navegador y estructura de archivos.

## Prerrequisitos y duración
- Prerrequisitos: ninguno.
- Duración estimada: 60–90 minutos.

## Resumen teórico
La World Wide Web es un sistema de documentos interconectados accesibles por Internet. Cuando escribes una URL en tu navegador, éste envía una solicitud HTTP a un servidor; el servidor responde con recursos (por ejemplo, un documento HTML). El navegador interpreta el HTML para construir el DOM (Document Object Model) y renderiza la página.

HTML (HyperText Markup Language) es un lenguaje de marcado que define la estructura y el contenido de una página. No es un lenguaje de programación: describe elementos como títulos, párrafos, listas, imágenes, enlaces, tablas y formularios mediante etiquetas. La presentación (colores, tamaños, posiciones) se gestiona con CSS, y el comportamiento (interactividad) con JavaScript. En este curso nos centraremos en HTML: estructura semántica y contenido.

Un documento HTML se compone de elementos anidados: cada elemento tiene una etiqueta de apertura, contenido y, normalmente, una etiqueta de cierre. Por ejemplo:
- `<p>` define un párrafo.
- `<a>` define un enlace.
- `<img>` inserta una imagen y emplea atributos como `src` y `alt`.

Las etiquetas pueden llevar atributos que modifican su comportamiento o aportan metadatos. Algunos atributos, como `id`, `class`, `lang` y `title`, se denominan “globales” y pueden existir en muchas etiquetas. Cuidar la semántica implica elegir la etiqueta que mejor describe el propósito del contenido (por ejemplo, `<header>`, `<main>`, `<article>`, `<nav>`, `<footer>`).

Accesibilidad (a11y) significa que las páginas sean utilizables por la mayor diversidad de personas posible, incluidas aquellas con tecnologías de asistencia como lectores de pantalla. Desde el inicio debemos usar texto alternativo (`alt`) para imágenes informativas, `label` en formularios, orden lógico de encabezados y estructura bien definida.

La organización de archivos también es importante. Para proyectos pequeños:
- `index.html` como página principal.
- `pages/` para páginas secundarias.
- `img/` para imágenes.
- `media/` para audios o videos si los hay.

Herramientas básicas:
- Editor de texto/código (VS Code, Sublime Text, etc.).
- Navegador moderno (Firefox, Chrome, Edge, Safari).
- Validador W3C para verificar errores de marcado.

Los estándares HTML evolucionan continuamente (HTML Living Standard de WHATWG). La documentación de MDN es una referencia práctica con ejemplos y compatibilidades. Enlazaremos frecuentemente a estas fuentes.

## Ejemplos comentados

```html
<!-- index.html: primer documento mínimo -->
<!DOCTYPE html>
<html lang="es">
  <head>
    <meta charset="utf-8">
    <title>Mi primera página HTML</title>
  </head>
  <body>
    <h1>¡Hola, Web!</h1>
    <p>Este es mi primer párrafo en HTML.</p>
  </body>
</html>
```

- `<!DOCTYPE html>`: indica el tipo de documento (HTML5).
- `<html lang="es">`: idioma principal del documento.
- `<meta charset="utf-8">`: codificación de caracteres.
- `<title>`: título que verá el usuario en la pestaña del navegador.
- `<h1>` y `<p>`: contenido principal y texto.

## Ejercicios guiados
1) Crea la carpeta `curso-html/` y dentro `index.html` con la estructura mínima (doctype, html, head, body).
2) Añade un `h1` con tu nombre y un `p` con una breve biografía (2–3 líneas).
3) Crea una carpeta `pages/` y agrega `pages/sobre.html` con una estructura mínima y un `h2` “Sobre mí”.
4) En `index.html`, al final del `body`, agrega un enlace a `pages/sobre.html` con el texto “Leer más sobre mí”.

## Retos prácticos
- Reto 1: Agrega un `h2` “Proyectos” y un párrafo explicando qué proyectos te gustaría construir solo con HTML.
- Reto 2: Crea `pages/contacto.html` y enlázalo desde `index.html`.

## Mini quiz
1) HTML es un lenguaje de…  
   a) programación  
   b) marcado  
   c) estilos  
2) ¿Cuál etiqueta define el título de la pestaña del navegador?  
3) Verdadero/Falso: `<img>` siempre requiere etiqueta de cierre.  
4) ¿Cuál atributo global define el idioma del documento raíz?  
5) Completa: El documento estándar actual se define por el doctype `<!_____ html>`.

### Respuestas
1) b  2) `<title>`  3) Falso (es vacía/void)  4) `lang`  5) `DOCTYPE`

## Checklist “lograste aprender esto si…”
- Puedes explicar el ciclo solicitud/respuesta básico de la Web.
- Puedes crear un `index.html` mínimo y abrirlo en el navegador.
- Distingues contenido (HTML), presentación (CSS) y comportamiento (JS).
- Conoces la estructura de carpetas básica.

## Errores comunes y cómo evitarlos
- Olvidar `<!DOCTYPE html>`: puede activar modos de compatibilidad. Inclúyelo siempre.
- No declarar `lang` en `<html>`: complica accesibilidad. Añade `lang="es"`.
- Guardar con codificación incorrecta: usa UTF-8 y `meta charset="utf-8"`.

## Referencias oficiales
- MDN: Introducción a HTML — https://developer.mozilla.org/es/docs/Learn/HTML/Introduction_to_HTML  
- WHATWG HTML — https://html.spec.whatwg.org/
