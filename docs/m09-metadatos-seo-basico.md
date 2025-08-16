---
title: M09 · Metadatos y SEO básico
description: charset, viewport, title, description, favicons y nociones de indexación.
---

# M09 · Metadatos y SEO básico

## Objetivos
- Configurar metadatos esenciales: `charset`, `title`, `meta viewport`, `meta description`.
- Entender el rol de los favicons.
- Conocer prácticas básicas de indexación sin entrar en SEO avanzado.

## Prerrequisitos y duración
- Prerrequisitos: M00–M08.
- Duración estimada: 60–90 minutos.

## Resumen teórico
Metadatos clave en `<head>`:

- `charset`: `<meta charset="utf-8">` para codificación correcta.
- `title`: título conciso y descriptivo por página.
- `meta description`: `<meta name="description" content="...">` resumen breve para motores de búsqueda y compartir.
- `meta viewport`: `<meta name="viewport" content="width=device-width, initial-scale=1">` ayuda a que la página se adapte al ancho del dispositivo. Aunque no cubrimos responsive con CSS, el `viewport` evita escalas incorrectas en móviles.

Favicons: íconos del sitio mostrados en pestañas y marcadores. Se declaran con `<link rel="icon" href="img/favicon.ico">` o formatos modernos (`.png`, `.svg`) según soporte.

Buenas prácticas SEO básicas en HTML:
- Títulos (`<title>`) únicos por página.
- Encabezados jerárquicos (`h1–h6`) coherentes.
- Texto alternativo en imágenes informativas.
- Enlaces descriptivos.
- Contenido relevante y bien estructurado.

## Ejemplos comentados

```html
<!DOCTYPE html>
<html lang="es">
  <head>
    <meta charset="utf-8">
    <title>Sobre mí — Ana Pérez</title>
    <meta name="description" content="Biografía y experiencia de Ana Pérez, desarrolladora web.">
    <meta name="viewport" content="width=device-width, initial-scale=1">
    <link rel="icon" href="img/favicon.png" type="image/png">
  </head>
  <body>
    <h1>Sobre mí</h1>
    <p>Hola, soy Ana…</p>
  </body>
</html>
```

## Ejercicios guiados
1) Añade `meta description` únicos a `index.html` y `pages/sobre.html`.
2) Declara `meta viewport` en tus páginas principales.
3) Agrega un favicon (`img/favicon.png`) con `<link rel="icon">`.

## Retos
- Reto: Redacta títulos y descripciones concisas para tres páginas, enfocándote en claridad y propósito.

## Mini quiz
1) Verdadero/Falso: `title` puede ser igual en todas las páginas.  
2) ¿Qué meta ayuda en móviles a escalar correctamente?  
3) ¿Para qué sirve `meta description`?  
4) ¿Qué etiqueta enlaza el favicon?  
5) Completa: `viewport` típico es `width=________, initial-scale=1`.

### Respuestas
1) Falso  2) `meta name="viewport"`  3) Resumen para buscadores/compartir  4) `<link rel="icon" ...>`  5) `device-width`

## Checklist
- Cada página tiene `title` y `description` únicos.
- `viewport` presente.
- Favicon declarado.

## Errores comunes
- Descripciones demasiado largas o genéricas.
- Falta de `viewport` en móviles.
- Repetir títulos en todas las páginas.

## Referencias
- MDN: Metadatos en `<head>` — https://developer.mozilla.org/es/docs/Learn/HTML/Introduction_to_HTML/The_head_metadata_in_HTML  
- WHATWG: The head element — https://html.spec.whatwg.org/multipage/semantics.html#the-head-element
