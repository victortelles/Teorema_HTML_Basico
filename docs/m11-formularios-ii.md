---
title: M11 · Formularios II
description: textarea, select/option/optgroup, button, fieldset/legend, datalist, pattern y validación nativa.
---

# M11 · Formularios II (textarea, select, button, fieldset, datalist, pattern)

## Objetivos
- Usar `textarea`, `select/option/optgroup`, `button`.
- Agrupar controles con `fieldset/legend`.
- Añadir `datalist` para sugerencias.
- Usar `pattern` para validación nativa.

## Prerrequisitos y duración
- Prerrequisitos: M10.
- Duración estimada: 75–105 minutos.

## Resumen teórico
- `textarea` para textos largos; usa `id`, `name`, `rows`, `cols` según necesidad.
- `select` crea listas desplegables; `option` define opciones; `optgroup` agrupa.
- `button` con `type="submit"`, `"reset"` o `"button"`; por defecto suele ser `"submit"` dentro de formularios.
- `fieldset` agrupa controles relacionados; `legend` nombra el grupo (mejora accesibilidad).
- `datalist` provee sugerencias para un `input` por `list="idDelDatalist"`.
- `pattern` acepta una expresión regular para validar formato. Acompáñalo con `title` para guiar al usuario.

## Ejemplos comentados

```html
<form>
  <fieldset>
    <legend>Datos básicos</legend>

    <label for="bio">Biografía</label>
    <textarea id="bio" name="bio" rows="4" cols="40" placeholder="Cuéntanos sobre ti"></textarea>

    <label for="pais">País</label>
    <select id="pais" name="pais" required>
      <optgroup label="América">
        <option value="mx">México</option>
        <option value="ar">Argentina</option>
      </optgroup>
      <optgroup label="Europa">
        <option value="es">España</option>
        <option value="fr">Francia</option>
      </optgroup>
    </select>

    <label for="ciudad">Ciudad</label>
    <input id="ciudad" name="ciudad" list="ciudades">
    <datalist id="ciudades">
      <option value="Ciudad de México">
      <option value="Madrid">
      <option value="Buenos Aires">
    </datalist>

    <label for="codigo">Código (3 letras)</label>
    <input id="codigo" name="codigo" pattern="[A-Za-z]{3}" title="Usa exactamente 3 letras.">
  </fieldset>

  <button type="submit">Guardar</button>
  <button type="reset">Limpiar</button>
</form>
```

## Ejercicios guiados
1) Añade a tu formulario un `fieldset` “Perfil” con `textarea bio` y `select país`.
2) Agrega un `datalist` para sugerir ciudades.
3) Usa `pattern` para validar un código de 3 dígitos (`[0-9]{3}`) con `title` explicativo.

## Retos
- Reto: Crea un formulario “Registro de evento” con dos `fieldset`: “Datos personales” y “Preferencias”; incluye `select` con `optgroup`.

## Mini quiz
1) Verdadero/Falso: `button` siempre es `type="button"`.  
2) ¿Qué elemento etiqueta un grupo de controles en `fieldset`?  
3) ¿Qué atributo conecta `input` con `datalist`?  
4) `pattern` usa…  
   a) iconos  
   b) expresiones regulares  
   c) colores  
5) Completa: Para validar 4 números exactos usarías `pattern="____"`.

### Respuestas
1) Falso (por defecto suele ser submit)  2) `legend`  3) `list`  4) b  5) `[0-9]{4}`

## Checklist
- Agrupas controles relacionados con `fieldset`.
- Añades sugerencias con `datalist` cuando son útiles.
- Documentas `pattern` con `title`.

## Errores comunes
- Olvidar `legend` en grupos.
- `pattern` sin `title`: el usuario no entiende el requisito.
- Usar `select` con demasiadas opciones sin agrupar.

## Referencias
- MDN: `<textarea>` — https://developer.mozilla.org/es/docs/Web/HTML/Element/textarea  
- MDN: `<select>` — https://developer.mozilla.org/es/docs/Web/HTML/Element/select  
- MDN: `<datalist>` — https://developer.mozilla.org/es/docs/Web/HTML/Element/datalist  
- WHATWG: Forms — https://html.spec.whatwg.org/multipage/forms.html
