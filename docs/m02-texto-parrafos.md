---
title: M02 · Texto, párrafos y semántica de texto
description: Párrafos, saltos, encabezados y etiquetas semánticas de texto en HTML.
---

# M02 · Texto y párrafos (p, br, hr), cabeceras (h1–h6), semántica de texto

## Objetivos
- Usar correctamente `p`, `br`, `hr`, y jerarquía de encabezados `h1–h6`.
- Aplicar semántica de texto: `strong`, `em`, `small`, `mark`, `abbr`, `time`, `code`, `pre`.
- Estructurar el contenido para mejorar legibilidad y accesibilidad.

## Prerrequisitos y duración
- Prerrequisitos: M00–M01.
- Duración estimada: 60–90 minutos.

## Resumen teórico
Los párrafos (`<p>`) son bloques de texto corrido. Evita usar múltiples `br` para separar párrafos; en cambio, crea un nuevo `<p>`. Los saltos de línea (`<br>`) son útiles para casos específicos (direcciones postales, poesía). La regla horizontal (`<hr>`) indica un cambio temático o separación semántica.

Los encabezados (`<h1>` a `<h6>`) estructuran el documento en niveles. Debe existir un solo `<h1>` representando el tema principal de la página; `h2`, `h3`, etc. subdividen secciones. Una jerarquía lógica mejora la navegación y la accesibilidad, pues los lectores de pantalla pueden saltar entre encabezados.

Semántica de texto:
- `<strong>` indica énfasis fuerte (importancia).
- `<em>` indica énfasis (acento) en una palabra o frase.
- `<small>` para notas o avisos secundarios.
- `<mark>` resalta texto relevante.
- `<abbr>` marca abreviaturas y puede incluir `title` con la expansión.
- `<time>` representa fechas y horas; ideal con `datetime`.
- `<code>` para fragmentos de código en línea.
- `<pre>` preserva espacios y saltos (útil para bloques de texto preformateados).

Estas etiquetas agregan significado; no controlan estilos visuales en este curso. Su uso correcto ayuda a SEO y accesibilidad.

## Ejemplos comentados

```html
<h1>Guía de Estudio</h1>
<h2>Introducción</h2>
<p>Este documento explica conceptos básicos de HTML.</p>

<h2>Convenciones</h2>
<p>El <strong>énfasis fuerte</strong> indica importancia. El <em>énfasis</em> cambia el tono.</p>
<p><small>Nota: Esta guía es introductoria.</small></p>
<p>Para resaltar, usa <mark>marcado</mark>.</p>
<p>La abreviatura <abbr title="HyperText Markup Language">HTML</abbr> es clave.</p>

<p>Fecha de publicación: <time datetime="2025-08-15">15 de agosto de 2025</time></p>

<hr>

<p>Fragmento de código en línea: <code>&lt;p&gt;Hola&lt;/p&gt;</code></p>
<pre>
&lt;!-- Texto preformateado --&gt;
Línea 1
  Línea 2 con espacios
Línea 3
</pre>
```

## Ejercicios guiados
1) Crea `pages/guia.html` con `h1` y dos secciones `h2`. En cada sección escribe dos párrafos.
2) En el primer párrafo usa `strong` y en el segundo `em`. Añade una nota `small`.
3) Inserta una fecha con `<time datetime="YYYY-MM-DD">` y un término con `abbr` y `title`.

## Retos
- Reto 1: Agrega un bloque `pre` que incluya una dirección postal con saltos `br` justificados (por ejemplo, firma o poema).
- Reto 2: Inserta una `hr` entre secciones donde cambie el tema.

## Mini quiz
1) Verdadero/Falso: Es correcto usar múltiples `br` para separar párrafos.  
2) ¿Qué etiqueta representa el título principal de la página?  
3) ¿Qué atributo de `<time>` normaliza una fecha?  
4) `<abbr>` debería incluir el atributo _______ con la expansión.  
5) ¿Qué etiqueta conserva los espacios y saltos tal cual?

### Respuestas
1) Falso  2) `<h1>`  3) `datetime`  4) `title`  5) `<pre>`

## Checklist
- Estructuras el contenido con encabezados lógicos.
- Usas `<p>` para párrafos y `<br>` solo cuando corresponde.
- Empleas etiquetas semánticas de texto adecuadas.

## Errores comunes
- Varias etiquetas `<h1>` por página: usa una sola.
- Usar `<br>` para crear espacio: crea nuevos párrafos/secciones.
- Olvidar `title` en `<abbr>`: añade contexto para lectores.

## Referencias
- MDN: Párrafos — https://developer.mozilla.org/es/docs/Web/HTML/Element/p  
- MDN: Encabezados — https://developer.mozilla.org/es/docs/Web/HTML/Element/Heading_Elements  
- MDN: Semántica de texto — https://developer.mozilla.org/es/docs/Learn/HTML/Introduction_to_HTML/HTML_text_fundamentals  
- WHATWG: Text-level semantics — https://html.spec.whatwg.org/multipage/text-level-semantics.html
