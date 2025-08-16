---
title: M10 · Formularios I
description: form, label, input básicos, name/value, placeholder, required.
---

# M10 · Formularios I (form, label, input, name/value, placeholder, required)

## Objetivos
- Crear formularios con `<form>` e inputs básicos.
- Asociar `<label>` a controles de formulario.
- Entender `name`/`value`, `placeholder`, `required`.

## Prerrequisitos y duración
- Prerrequisitos: M00–M09.
- Duración estimada: 75–105 minutos.

## Resumen teórico
`<form>` encapsula controles que se envían al servidor. Cada control debe tener un `name`; al enviar se envía par `name=value`. A nivel HTML:
- `<label>` asociado a un control con `for="id-del-control"` o anidando el control mejora accesibilidad y área clicable.
- `input` tiene múltiples tipos: `text`, `email`, `password`, `number`, `url`, etc.
- `placeholder` muestra una pista breve dentro del campo. No sustituye `label`.
- `required` activa validación nativa (no permite enviar si está vacío).

La acción de envío se define con `action` y `method` en `<form>`. Aunque aquí no procesamos en backend, la estructura prepara el formulario para un futuro servidor.

## Ejemplos comentados

```html
<form action="/procesar" method="get">
  <div>
    <label for="nombre">Nombre</label>
    <input id="nombre" name="nombre" type="text" required placeholder="Tu nombre completo">
  </div>
  <div>
    <label for="correo">Correo</label>
    <input id="correo" name="correo" type="email" required placeholder="tucorreo@ejemplo.com">
  </div>
  <div>
    <label for="edad">Edad</label>
    <input id="edad" name="edad" type="number" min="0" step="1">
  </div>
  <button type="submit">Enviar</button>
</form>
```

## Ejercicios guiados
1) Crea un formulario de contacto con campos: nombre (texto, requerido), email (email, requerido), asunto (texto) y botón enviar.
2) Asegura que cada `input` tenga `id`, `name` y `label` asociado.
3) Prueba la validación nativa del navegador (deja campos requeridos vacíos).

## Retos
- Reto: Añade un `input type="url"` con `placeholder`, y valida que el navegador detecta URLs inválidas.

## Mini quiz
1) Verdadero/Falso: `placeholder` reemplaza `label`.  
2) ¿Qué atributo define el nombre del campo en el envío?  
3) ¿Cómo asocias un `label` con un `input`?  
4) ¿Qué tipo de input ayuda a validar correos?  
5) Completa: El atributo que impide enviar vacío es `_______`.

### Respuestas
1) Falso  2) `name`  3) `for` con el `id` del input o anidando el input  4) `type="email"`  5) `required`

## Checklist
- Cada control tiene `label` y `name`.
- Usas tipos de `input` apropiados.
- Pruebas validación nativa.

## Errores comunes
- Omitir `label`: reduce accesibilidad/usabilidad.
- Reutilizar `id` entre inputs.
- Usar `placeholder` como único indicador del campo.

## Referencias
- MDN: Formularios — https://developer.mozilla.org/es/docs/Learn/Forms  
- MDN: `<input>` — https://developer.mozilla.org/es/docs/Web/HTML/Element/input  
- WHATWG: Forms — https://html.spec.whatwg.org/multipage/forms.html
