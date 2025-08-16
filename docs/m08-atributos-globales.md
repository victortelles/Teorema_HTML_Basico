---
title: M08 · Atributos globales
description: id, class, title, lang, dir, hidden, tabindex, data-* y buenas prácticas.
---

# M08 · Atributos globales (id, class, title, lang, dir, hidden, tabindex, data-*)

## Objetivos
- Comprender y usar atributos globales en múltiples elementos.
- Identificar buenas prácticas y consideraciones de accesibilidad.
- Usar `data-*` para almacenar datos personalizados no presentacionales.

## Prerrequisitos y duración
- Prerrequisitos: M00–M07.
- Duración estimada: 60–90 minutos.

## Resumen teórico
Atributos globales que puedes encontrar/utilizar en muchos elementos:

- `id`: identificador único en el documento. Útil para anclas internas, relación `label`/`input`, referencias.
- `class`: clasificar elementos en grupos lógicos. Aunque en este curso no usamos CSS, `class` ayuda a identificar roles.
- `title`: información adicional; se muestra como tooltip en algunos navegadores, úsalo con moderación.
- `lang`: idioma del elemento (hereda de `<html lang="...">` pero puede sobrescribirse).
- `dir`: dirección del texto (`ltr`, `rtl`, `auto`), útil para idiomas de derecha a izquierda.
- `hidden`: oculta semánticamente un elemento (no se presenta y las tecnologías de asistencia suelen ignorarlo).
- `tabindex`: controla el orden de tabulación; úsalo con cuidado. En HTML puro, evita abusar para no romper la navegación natural.
- `data-*`: atributos personalizados para almacenar metadatos. Ej.: `data-autor="ana"`.

## Ejemplos comentados

```html
<h2 id="equipo">Equipo</h2>
<p class="intro" title="Resumen">Somos un equipo dedicado...</p>

<p lang="en">This paragraph is in English.</p>
<p dir="rtl">مثال باللغة العربية</p>

<p hidden>Texto oculto para pruebas.</p>

<a href="#equipo" tabindex="0">Volver a Equipo</a>

<article data-tipo="nota" data-autor="ana">
  <h3>Nota</h3>
  <p>Contenido con metadatos personalizados.</p>
</article>
```

## Ejercicios guiados
1) Agrega `id` a tres secciones en `index.html` y crea un índice al inicio con enlaces a cada sección.
2) Marca un párrafo con `lang="en"` si está en inglés.
3) Crea un elemento con `data-*` (p. ej., `data-categoria="tutorial"`).

## Retos
- Reto: Añade un bloque informativo con `title` conciso y útil; evalúa si realmente aporta valor.

## Mini quiz
1) Verdadero/Falso: `id` puede repetirse.  
2) ¿Qué atributo usarías para marcar una palabra en inglés dentro de un párrafo en español?  
3) ¿Para qué sirve `data-*`?  
4) `hidden` hace que el elemento sea…  
5) Completa: `tabindex` debe usarse con ______ para no romper la navegación.

### Respuestas
1) Falso  2) `lang="en"`  3) Guardar metadatos personalizados  4) no presentado/oculto  5) moderación

## Checklist
- Usas `id` únicos y significativos.
- Empleas `lang` y `dir` cuando el contenido lo requiere.
- Evitas abusar de `tabindex`.

## Errores comunes
- Repetir `id`: invalida el documento.
- `title` excesivo o redundante: puede resultar molesto.
- `hidden` usado para contenido esencial: evita ocultar información importante.

## Referencias
- MDN: Global attributes — https://developer.mozilla.org/en-US/docs/Web/HTML/Global_attributes  
- WHATWG: Global attributes — https://html.spec.whatwg.org/multipage/dom.html#global-attributes
