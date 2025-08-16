---
title: M04 · Imágenes y multimedia básico
description: Imágenes con img, atributos src y alt; audio y video con source y track.
---

# M04 · Imágenes y multimedia básico (img, audio, video, source, track)

## Objetivos
- Insertar imágenes con `<img>` y texto alternativo `alt`.
- Entender formatos comunes (PNG, JPG, SVG).
- Reproducir audio y video con elementos nativos.
- Añadir subtítulos con `<track>`.

## Prerrequisitos y duración
- Prerrequisitos: M00–M03.
- Duración estimada: 60–90 minutos.

## Resumen teórico
`<img>` inserta imágenes. El atributo `src` indica la ruta al archivo; `alt` proporciona una alternativa textual para lectores de pantalla y cuando la imagen no carga. El `alt` debe describir la función de la imagen:
- Informativa: describe el contenido (“Foto de perfil de Ana Pérez”).
- Decorativa: `alt=""` (vacío) para que sea ignorada por tecnologías de asistencia.

Formatos:
- PNG: sin pérdida, soporte transparencia, ideal logos e ilustraciones simples.
- JPG/JPEG: con pérdida, ideal fotografías.
- SVG: vectorial, escalable sin pérdida, ideal íconos/logos.

Multimedia:
- `<audio>` y `<video>` soportan reproducción nativa. Usa `<source>` para ofrecer múltiples formatos (compatibilidad). El atributo `controls` agrega controles. `<track>` añade pistas de texto (subtítulos) para accesibilidad con `kind="subtitles"` o `captions"` y `srclang`.

## Ejemplos comentados

```html
<h2>Imágenes</h2>
<img src="img/perfil.jpg" alt="Foto de perfil de Ana Pérez" width="300" height="300">
<img src="img/decorativo.svg" alt="" aria-hidden="true">

<h2>Audio</h2>
<audio controls>
  <source src="media/podcast.mp3" type="audio/mpeg">
  <source src="media/podcast.ogg" type="audio/ogg">
  Tu navegador no soporta el elemento audio.
</audio>

<h2>Video</h2>
<video controls width="640" height="360">
  <source src="media/demo.mp4" type="video/mp4">
  <source src="media/demo.webm" type="video/webm">
  <track kind="subtitles" src="media/demo.es.vtt" srclang="es" label="Español">
  Tu navegador no soporta el elemento video.
</video>
```

## Ejercicios guiados
1) Copia una imagen a `img/` y agrégala con `<img>` en `index.html` con un `alt` significativo.
2) Inserta una imagen decorativa con `alt=""` y añade `aria-hidden="true"`.
3) Si cuentas con un archivo de audio, insértalo con `<audio controls>` y al menos un `<source>`.

## Retos
- Reto 1: Prepara un video corto en `media/` e inserta subtítulos con un archivo `.vtt` y `<track>`.
- Reto 2: Crea una página `pages/galeria.html` con 4–6 imágenes, cada una con `alt` adecuado.

## Mini quiz
1) Verdadero/Falso: `alt` puede dejarse vacío en imágenes informativas.  
2) ¿Qué formato es ideal para logos escalables sin pérdida?  
3) ¿Qué elemento añade subtítulos a `<video>`?  
4) ¿Qué atributo añade controles de reproducción en `audio`/`video`?  
5) Completa: Una imagen decorativa debe tener `alt="____"`.

### Respuestas
1) Falso  2) SVG  3) `<track>`  4) `controls`  5) "" (vacío)

## Checklist
- Añades `alt` correcto según el propósito.
- Conoces formatos adecuados para cada caso.
- Puedes incluir audio/video con fuentes alternativas.

## Errores comunes
- `alt` genérico como “imagen”: no informa.
- Solo un formato de video: ofrece alternativas si es posible.
- Usar imágenes enormes innecesariamente: optimiza el tamaño del archivo (aunque el estilo no se cubre en este curso).

## Referencias
- MDN: `<img>` — https://developer.mozilla.org/es/docs/Web/HTML/Element/img  
- MDN: `<audio>` — https://developer.mozilla.org/es/docs/Web/HTML/Element/audio  
- MDN: `<video>` — https://developer.mozilla.org/es/docs/Web/HTML/Element/video  
- WHATWG: Images — https://html.spec.whatwg.org/multipage/embedded-content.html#embedded-content
