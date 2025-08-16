---
title: M12 · Accesibilidad esencial
description: Textos alternativos, estructura semántica, etiquetas de formularios, roles mínimos y orden lógico.
---

# M12 · Accesibilidad esencial en HTML

## Objetivos
- Aplicar textos alternativos, estructura y encabezados correctos.
- Asociar etiquetas y controles en formularios.
- Respetar orden lógico de lectura y foco.
- Conocer roles mínimos y buenas prácticas.

## Prerrequisitos y duración
- Prerrequisitos: M00–M11.
- Duración estimada: 60–90 minutos.

## Resumen teórico
Accesibilidad (a11y) busca que todos puedan usar tu sitio. En HTML, prácticas clave:
- Texto alternativo en imágenes informativas (`alt` claro). Decorativas con `alt=""`.
- Estructura semántica: un solo `<main>`, encabezados jerárquicos, secciones identificables.
- Formularios: `label` conectado a cada control; `fieldset/legend` para grupos.
- Orden de lectura y navegación por teclado natural (evita abusar de `tabindex`).
- Texto de enlace significativo; evita “aquí”.
- Contraste y estilos no se cubren, pero el contenido debe entenderse sin estilo adicional.

Roles ARIA mínimos: en HTML semántico, muchos roles están implícitos. Evita roles redundantes. Si un rol no añade valor claro, no lo uses. Prefiere elementos nativos (`nav`, `header`, `footer`, `button`, etc.) que ya exponen roles y comportamientos.

Prueba con teclado: Tab, Shift+Tab para recorrer enlaces y controles. Usa lectores de pantalla (NVDA, VoiceOver) para detectar problemas de estructura o descripciones faltantes.

## Ejemplos comentados

```html
<main id="contenido">
  <h1>Guía</h1>
  <section>
    <h2>Introducción</h2>
    <p>Objetivos del documento…</p>
  </section>

  <figure>
    <img src="img/grafica.png" alt="Gráfica de barras con ventas trimestrales: Q1 10k, Q2 12k, Q3 9k, Q4 15k">
    <figcaption>Ventas por trimestre.</figcaption>
  </figure>

  <form>
    <label for="busqueda">Buscar</label>
    <input id="busqueda" name="q" type="search" placeholder="Término a buscar">
    <button type="submit">Buscar</button>
  </form>
</main>
```

## Ejercicios guiados
1) Revisa tus imágenes y actualiza `alt` con descripciones útiles según su función.
2) Asegura que cada `input` tenga `label`. Agrupa campos relacionados con `fieldset`.
3) Recorre tu página con el teclado y verifica el orden de foco.

## Retos
- Reto: Prepara una mini auditoría: lista 5 mejoras de accesibilidad aplicadas a tu sitio.

## Mini quiz
1) Verdadero/Falso: Un `alt` vacío puede ser correcto.  
2) ¿Qué elemento ya implica rol de navegación?  
3) ¿Qué relación debe existir en formularios para accesibilidad?  
4) ¿Es aconsejable abusar de `tabindex` para “forzar” el orden?  
5) Completa: Estructura jerárquica correcta con `h1` seguido de `h2`, luego `____` si hace falta.

### Respuestas
1) Verdadero (para decorativas)  2) `<nav>`  3) `label` asociado a su control (`for`/`id`)  4) No  5) `h3`

## Checklist
- `alt` adecuados y `alt=""` en decorativas.
- Navegación por teclado fluida.
- Formularios etiquetados.

## Errores comunes
- `alt` ausentes o inútiles.
- Encabezados saltados (de `h1` a `h4` sin contexto).
- Formularios sin `label`.

## Referencias
- MDN: Accesibilidad — https://developer.mozilla.org/es/docs/Learn/Accessibility  
- WHATWG/ARIA mappings — https://html.spec.whatwg.org/multipage/aria.html
