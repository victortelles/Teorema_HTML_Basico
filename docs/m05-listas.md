---
title: M05 · Listas
description: Listas desordenadas, ordenadas y de definiciones; usos semánticos y navegación.
---

# M05 · Listas (ul, ol, li, dl, dt, dd)

## Objetivos
- Crear listas desordenadas (`ul`) y ordenadas (`ol`) con `li`.
- Usar listas de definiciones (`dl`, `dt`, `dd`).
- Comprender su uso para menús y agrupaciones lógicas.

## Prerrequisitos y duración
- Prerrequisitos: M00–M04.
- Duración estimada: 45–75 minutos.

## Resumen teórico
Las listas ayudan a estructurar colecciones de ítems. `ul` crea listas sin orden numérico; `ol` crea listas numeradas; `li` representa cada elemento. Las listas de definiciones (`dl`) agrupan pares término/definición con `dt` y `dd`.

En navegación, es común usar `ul` para agrupar enlaces dentro de `<nav>`. Semánticamente, permite a tecnologías de asistencia comprender que se trata de una colección.

## Ejemplos comentados

```html
<h2>Tareas</h2>
<ul>
  <li>Leer documentación</li>
  <li>Practicar ejercicios</li>
  <li>Validar HTML</li>
</ul>

<h2>Pasos</h2>
<ol>
  <li>Crear estructura</li>
  <li>Agregar contenido</li>
  <li>Probar en el navegador</li>
</ol>

<h2>Glosario breve</h2>
<dl>
  <dt>HTML</dt>
  <dd>Lenguaje de marcado para documentos web.</dd>
  <dt>Atributo</dt>
  <dd>Información adicional en una etiqueta.</dd>
</dl>
```

## Ejercicios guiados
1) Crea un menú de navegación en `index.html` usando `ul` con 3–4 enlaces.
2) En `pages/faq.html`, crea una lista ordenada con 5 pasos para “Publicar una página”.
3) Construye un mini glosario en `pages/glosario.html` usando `dl/dt/dd`.

## Retos
- Reto: En `pages/recetas.html`, crea una lista ordenada con pasos de una receta y, por cada paso, una sublista `ul` con notas.

## Mini quiz
1) Verdadero/Falso: `li` solo puede aparecer dentro de `ul` u `ol`.  
2) ¿Qué elemento representa un término en un glosario?  
3) ¿Qué elemento agrupa la lista de definiciones?  
4) ¿Qué tipo de lista usarías para pasos secuenciales?  
5) Completa: Un menú suele representarse con `____` y elementos `li`.

### Respuestas
1) Verdadero  2) `dt`  3) `dl`  4) `ol`  5) `ul`

## Checklist
- Sabes cuándo usar `ul` vs `ol`.
- Empleas `dl/dt/dd` para pares término/definición.
- Estructuras menús como listas.

## Errores comunes
- Mezclar `li` fuera de listas.
- Usar listas para indentar sin sentido semántico.
- No anidar sublistas correctamente.

## Referencias
- MDN: `<ul>`, `<ol>`, `<li>` — https://developer.mozilla.org/es/docs/Web/HTML/Element/ul  
- MDN: `<dl>`, `<dt>`, `<dd>` — https://developer.mozilla.org/es/docs/Web/HTML/Element/dl  
- WHATWG: Grouping content — https://html.spec.whatwg.org/multipage/grouping-content.html
