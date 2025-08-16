---
title: M06 · Tablas
description: Estructura de tablas, encabezados, secciones, caption y accesibilidad básica.
---

# M06 · Tablas (table, thead, tbody, tfoot, tr, th, td, caption, scope)

## Objetivos
- Crear tablas con encabezados, cuerpo y pie.
- Añadir `caption` y atributos `scope` para accesibilidad.
- Comprender cuándo usar tablas (datos tabulares) y cuándo no.

## Prerrequisitos y duración
- Prerrequisitos: M00–M05.
- Duración estimada: 60–90 minutos.

## Resumen teórico
Las tablas organizan datos tabulares. La estructura típica:
- `<table>` contenedor general.
- `<caption>` título descriptivo (mejora accesibilidad).
- `<thead>`, `<tbody>`, `<tfoot>` secciones lógicas.
- Filas con `<tr>`.
- Encabezados con `<th>` y celdas de datos con `<td>`.
- `scope="col"` o `scope="row"` en `<th>` ayuda a asociar encabezados con celdas.

No uses tablas para maquetar páginas; su propósito es representar datos. Una tabla accesible debe tener `caption` claro, encabezados bien definidos y scope apropiado.

## Ejemplos comentados

```html
<table>
  <caption>Horarios del curso</caption>
  <thead>
    <tr>
      <th scope="col">Módulo</th>
      <th scope="col">Tema</th>
      <th scope="col">Duración</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th scope="row">M01</th>
      <td>Estructura</td>
      <td>60 min</td>
    </tr>
    <tr>
      <th scope="row">M02</th>
      <td>Texto</td>
      <td>75 min</td>
    </tr>
  </tbody>
  <tfoot>
    <tr>
      <td colspan="3">Duraciones estimadas</td>
    </tr>
  </tfoot>
</table>
```

## Ejercicios guiados
1) Crea `pages/tabla-precios.html` con una tabla que incluya `caption`, `thead`, `tbody` y `tfoot`.
2) Usa `th` con `scope="col"` para los encabezados de columna y `scope="row"` para los renglones.
3) Agrega una fila en el pie con una nota aclaratoria.

## Retos
- Reto: Crea una tabla de contacto con columnas: “Nombre”, “Email”, “Rol”; añade `caption` y valida que el HTML sea correcto.

## Mini quiz
1) Verdadero/Falso: `caption` es recomendable para describir la tabla.  
2) ¿Qué atributos en `th` ayudan a accesibilidad?  
3) ¿Qué sección suele contener los encabezados?  
4) ¿Debe usarse tabla para maquetar un layout?  
5) Completa: Las filas se crean con `____`.

### Respuestas
1) Verdadero  2) `scope="col"` y `scope="row"`  3) `thead`  4) No  5) `<tr>`

## Checklist
- Incluyes `caption` descriptivo.
- Divides en `thead`, `tbody`, `tfoot` si aplica.
- Usas `th` y `scope` correctamente.

## Errores comunes
- Mezclar `td` cuando deberían ser `th`.
- Omitir `scope` en tablas complejas.
- Usar tablas para diseño.

## Referencias
- MDN: `<table>` — https://developer.mozilla.org/es/docs/Web/HTML/Element/table  
- WHATWG: Tabular data — https://html.spec.whatwg.org/multipage/tables.html
