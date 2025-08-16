---
title: M03 · Enlaces y rutas
description: Enlaces con <a>, rutas relativas/absolutas, anclas internas y buenas prácticas.
---

# M03 · Enlaces y rutas (a, href, rutas, anclas)

## Objetivos
- Crear enlaces con `<a>` y el atributo `href`.
- Diferenciar rutas relativas y absolutas.
- Crear anclas internas y buenas prácticas de navegación.

## Prerrequisitos y duración
- Prerrequisitos: M00–M02.
- Duración estimada: 60–90 minutos.

## Resumen teórico
Los enlaces son el núcleo de la Web. La etiqueta `<a>` crea hipervínculos mediante el atributo `href`. Puedes enlazar a:
- Archivos locales: `pages/sobre.html` (ruta relativa).
- URLs absolutas: `https://developer.mozilla.org/`.
- Anclas internas: `#seccion` para saltar a un elemento con `id="seccion"`.

Rutas relativas:
- `./archivo.html` o `archivo.html`: en la misma carpeta.
- `pages/archivo.html`: subcarpeta.
- `../archivo.html`: subir un nivel.

Rutas absolutas:
- Comienzan con `http://` o `https://` y apuntan a dominios externos.

El atributo `title` puede dar contexto adicional al enlace; úsalo con moderación. Para accesibilidad, asegúrate de que el texto del enlace sea descriptivo (“Leer sobre accesibilidad” en lugar de “haz clic aquí”). Evita usar solo “aquí” como ancla.

Puedes crear anclas internas con `id`: cualquier elemento puede tener `id` único. Un enlace a `#contacto` te llevará al elemento con `id="contacto"`.

## Ejemplos comentados

```html
<nav>
  <a href="index.html">Inicio</a>
  <a href="pages/sobre.html">Sobre mí</a>
  <a href="https://developer.mozilla.org/" title="Documentación de MDN">MDN</a>
</nav>

<h2 id="contacto">Contacto</h2>
<p>Escríbeme a mi correo...</p>
<p><a href="#contacto">Ir a contacto</a></p>
```

Rutas relativas:

```html
<!-- Desde index.html -->
<a href="pages/portfolio.html">Ver portfolio</a>
<!-- Desde pages/portfolio.html -->
<a href="../index.html">Volver al inicio</a>
```

## Ejercicios guiados
1) En `index.html`, crea una barra de navegación simple con enlaces a `pages/sobre.html` y `pages/contacto.html`.
2) En `pages/sobre.html`, añade un `h2 id="bio"` y un enlace al final “Volver a Bio” que apunte a `#bio`.
3) Agrega un enlace externo a MDN con `href="https://developer.mozilla.org/"` y un texto descriptivo.

## Retos
- Reto 1: Crea `pages/faq.html` con varios `h3` con `id`. Desde el inicio del documento, crea un índice que enlaza a cada `id`.
- Reto 2: Agrega enlaces de regreso a la parte superior con `href="#top"` colocando `id="top"` en el encabezado principal.

## Mini quiz
1) Verdadero/Falso: Un `id` puede repetirse varias veces en una misma página.  
2) ¿Qué ruta usarías para enlazar a `img/logo.png` desde `pages/portfolio.html`?  
3) ¿Qué tipo de ruta es `https://example.com/ayuda`?  
4) Texto de enlace accesible debe ser…  
   a) “haz clic aquí”  
   b) Descriptivo del destino  
   c) Solo un ícono  
5) Completa: Un enlace a una sección interna usa la sintaxis `href="#____"`.

### Respuestas
1) Falso  2) `../img/logo.png`  3) Absoluta  4) b  5) id del destino

## Checklist
- Usas `a` con `href` correctamente.
- Diferencias rutas relativas/absolutas.
- Empleas texto de enlace descriptivo y `id` únicos.

## Errores comunes
- `href="#"` sin `id` destino: añade `id` o usa la URL correcta.
- Texto “aquí” aislado: no es accesible.
- Rutas relativas que no consideran la carpeta actual: revisa la estructura de directorios.

## Referencias
- MDN: `<a>` — https://developer.mozilla.org/es/docs/Web/HTML/Element/a  
- WHATWG: The a element — https://html.spec.whatwg.org/multipage/text-level-semantics.html#the-a-element
