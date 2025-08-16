---
title: M13 · Validación y buenas prácticas
description: Uso del validador W3C, comentarios, entidades HTML, organización de archivos y calidad.
---

# M13 · Validación, calidad y buenas prácticas

## Objetivos
- Validar HTML con W3C Validator.
- Usar comentarios, entidades y codificación correctamente.
- Organizar archivos y seguir buenas prácticas.

## Prerrequisitos y duración
- Prerrequisitos: M00–M12.
- Duración estimada: 60–90 minutos.

## Resumen teórico
Validar HTML ayuda a detectar errores (etiquetas mal anidadas, atributos inválidos, ids duplicados). El Validador W3C permite pegar el código, subir un archivo o proporcionar una URL.

Comentarios: `<!-- ... -->` documentan el código, no deben contener secretos. Entidades HTML permiten representar caracteres especiales: `&lt;`, `&gt;`, `&amp;`, `&nbsp;` cuando sea necesario.

Organización:
- Carpetas `img/`, `pages/`, `media/`.
- Nombres de archivo en minúsculas y sin espacios: `sobre-mi.html`.
- Rutas relativas coherentes.
- Un `index.html` como punto de entrada.

Buenas prácticas:
- Semántica clara y consistente.
- Textos de enlace descriptivos.
- `lang` y `charset` correctos.
- `alt` y `label` apropiados.
- Títulos y descripciones únicas.

## Ejemplos comentados

```html
<!-- Comentario: sección de proyectos -->
<section id="proyectos">
  <h2>Proyectos</h2>
  <p>Algunos trabajos &amp; logros destacados.</p>
</section>
```

## Ejercicios guiados
1) Valida tus páginas con el Validador W3C y corrige los errores reportados.
2) Revisa duplicados de `id` y ajusta a nombres únicos.
3) Revisa títulos y descripciones por página.

## Retos
- Reto: Elabora una guía de estilo corta (archivo `pages/guia-estilo.html`) indicando convenciones de nombres y estructura.

## Mini quiz
1) Verdadero/Falso: Validar es opcional y no aporta valor.  
2) ¿Cuál es la sintaxis de comentario en HTML?  
3) ¿Qué entidad representa `&`?  
4) ¿Qué archivo suele ser la entrada al sitio?  
5) Completa: Nombres de archivo preferible en _______ y sin espacios.

### Respuestas
1) Falso  2) `<!-- comentario -->`  3) `&amp;`  4) `index.html`  5) minúsculas

## Checklist
- Páginas validadas sin errores críticos.
- Comentarios útiles y concisos.
- Archivos organizados.

## Errores comunes
- No validar y dejar errores invisibles.
- Usar entidades innecesarias (solo cuando hace falta).
- Estructura desordenada de carpetas.

## Referencias
- Validador W3C — https://validator.w3.org/  
- MDN: Entidades — https://developer.mozilla.org/es/docs/Glossary/Entity  
- WHATWG: Syntax — https://html.spec.whatwg.org/multipage/syntax.html
