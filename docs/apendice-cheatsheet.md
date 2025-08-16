---
title: Apéndice · Cheatsheet HTML
description: Hoja de trucos con sintaxis esencial de HTML básico.
---

# Apéndice · Cheatsheet HTML

## Plantilla mínima

```html
<!DOCTYPE html>
<html lang="es">
  <head>
    <meta charset="utf-8">
    <title>Título</title>
    <meta name="description" content="Descripción breve.">
    <meta name="viewport" content="width=device-width, initial-scale=1">
    <link rel="icon" href="img/favicon.png" type="image/png">
  </head>
  <body>
    <main>
      <h1>Encabezado principal</h1>
      <p>Párrafo.</p>
    </main>
  </body>
</html>
```

## Texto y semántica
- Párrafo: `<p>Texto</p>`
- Encabezados: `<h1>` … `<h6>`
- Énfasis: `<em>`, Importancia: `<strong>`
- Código: `<code>`, Preformateado: `<pre>`
- Abreviatura: `<abbr title="...">ABC</abbr>`
- Fecha/hora: `<time datetime="YYYY-MM-DD">15/08/2025</time>`

## Enlaces y rutas
- Enlace: `<a href="pages/sobre.html">Sobre mí</a>`
- Ancla interna: `<a href="#bio">Bio</a>`, destino: `<h2 id="bio">Bio</h2>`

## Imágenes y multimedia
- Imagen: `<img src="img/foto.jpg" alt="Descripción">`
- Audio: `<audio controls><source src="media/audio.mp3" type="audio/mpeg"></audio>`
- Video: `<video controls><source src="media/video.mp4" type="video/mp4"></video>`

## Listas
- Desordenada: `<ul><li>Uno</li><li>Dos</li></ul>`
- Ordenada: `<ol><li>Uno</li><li>Dos</li></ol>`
- Definiciones: `<dl><dt>Término</dt><dd>Definición</dd></dl>`

## Tablas
```html
<table>
  <caption>Título</caption>
  <thead><tr><th scope="col">Col</th></tr></thead>
  <tbody><tr><th scope="row">Fila</th><td>Dato</td></tr></tbody>
</table>
```

## Estructura semántica
`header`, `nav`, `main` (único), `section`, `article`, `aside`, `footer`, `figure`, `figcaption`.

## Formularios (básico)
```html
<form>
  <label for="correo">Correo</label>
  <input id="correo" name="correo" type="email" required>
  <button type="submit">Enviar</button>
</form>
```

## Atributos globales
`id`, `class`, `title`, `lang`, `dir`, `hidden`, `tabindex`, `data-*`.

## Entidades comunes
`&lt;` `<` · `&gt;` `>` · `&amp;` `&` · `&nbsp;` espacio duro

Validador: https://validator.w3.org/
