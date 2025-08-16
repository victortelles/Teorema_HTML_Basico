---
title: M01 · Estructura mínima del documento
description: Doctype, html, head, body; partes y propósito de cada sección.
---

# M01 · Estructura mínima de un documento HTML

## Objetivos de aprendizaje
- Construir la plantilla mínima de un documento HTML5.
- Comprender el propósito de `<head>` vs `<body>`.
- Configurar correctamente idioma, codificación y título.

## Prerrequisitos y duración
- Prerrequisitos: M00.
- Duración estimada: 60–90 minutos.

## Resumen teórico
Un documento HTML5 inicia con `<!DOCTYPE html>`, señalando al navegador usar el estándar moderno. El elemento raíz es `<html>`, que debe incluir el atributo `lang` con el idioma principal del documento, relevante para accesibilidad, pronunciación y funciones de autotraducción.

Dentro de `<html>` hay dos grandes secciones:
- `<head>`: metadatos sobre el documento (codificación, título, descripción, favicon, enlaces a otros recursos). No es contenido visible principal.
- `<body>`: contenido visible y semántico de la página (encabezados, párrafos, imágenes, listas, tablas, formularios, etc.).

La codificación de caracteres se especifica con `<meta charset="utf-8">`. UTF-8 permite representar casi todos los caracteres y evita problemas con tildes y caracteres especiales.

El `<title>` define el texto que aparece en la pestaña del navegador, y también es importante para SEO básico y accesibilidad (da contexto a los usuarios que usan lectores de pantalla o navegación por pestañas).

Dentro de `<body>` organizamos el contenido con una jerarquía lógica. En módulos posteriores añadiremos elementos semánticos (`<header>`, `<main>`, `<footer>`) para dar más significado a esa estructura.

Evita duplicar el `doctype` o incluir más de un `<html>`, `<head>` o `<body>`. HTML tolera ciertos errores, pero la validación W3C te ayudará a encontrar y corregir problemas.

## Ejemplos comentados

```html
<!DOCTYPE html>
<html lang="es">
  <head>
    <meta charset="utf-8">
    <title>Estructura mínima</title>
  </head>
  <body>
    <h1>Bienvenido</h1>
    <p>Este documento cumple la estructura mínima HTML5.</p>
  </body>
</html>
```

- `<head>` contiene metadatos; `<body>` aloja el contenido que se muestra.

Otro ejemplo con comentarios:

```html
<!DOCTYPE html>
<html lang="es">
  <head>
    <!-- Metadatos: no visible en el cuerpo -->
    <meta charset="utf-8">
    <title>Mi sitio</title>
  </head>
  <body>
    <!-- Contenido visible -->
    <h1>Portada</h1>
    <p>Texto de ejemplo en el cuerpo.</p>
  </body>
</html>
```

## Ejercicios guiados
1) Crea `plantilla.html` con la estructura mínima y cambia el título a “Plantilla base”.
2) Copia `plantilla.html` en `pages/pagina2.html` y modifica el `h1` a “Segunda página”.
3) Verifica que ambos archivos se abren correctamente desde el navegador haciendo doble clic o usando “Abrir archivo”.

## Retos prácticos
- Reto: Agrega un comentario dentro de `<head>` explicando la finalidad del archivo, y otro en `<body>` con tu nombre y fecha.

## Mini quiz
1) Verdadero/Falso: `<head>` es para contenido visible.  
2) ¿Qué atributo en `<html>` especifica el idioma principal del documento?  
3) ¿Qué etiqueta define el texto de la pestaña del navegador?  
4) Completa: La codificación recomendada es `<meta charset="____">`.  
5) ¿Cuál es el primer elemento requerido por un documento HTML5 moderno?

### Respuestas
1) Falso  2) `lang`  3) `<title>`  4) `utf-8`  5) `<!DOCTYPE html>`

## Checklist
- Sabes crear una estructura mínima válida.
- Diferencias `<head>` y `<body>`.
- Configuras `lang` y `charset` correctamente.

## Errores comunes
- Olvidar `lang`: añádelo siempre.
- Confundir `<title>` con un encabezado visible: el texto visible va en `<h1>`, no en `<title>`.
- Codificación incorrecta: usa UTF-8.

## Referencias
- MDN: Estructura HTML — https://developer.mozilla.org/es/docs/Learn/HTML/Introduction_to_HTML/Getting_started  
- WHATWG: The html element — https://html.spec.whatwg.org/multipage/semantics.html#the-html-element
