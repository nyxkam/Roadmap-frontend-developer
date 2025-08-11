# HTML Semántico

HTML semántico significa usar las etiquetas correctas según el signoficado del contenido
no su apariencia.

- No semántico: `<div>` y `<span>` -> No dicen nada sobre el contenido.
- Semántico: `<header>`,`<main>`,`<section>`,`<footer>`, etc -> Indican qué es cada parte 
de la página. 

## Ventaja del HTML semántico:

1. Ayuda a entender la estructur a de la página incluso sin ver el contenido.
2. Mejora la accesibilidad para lectores de pantalla y otras herramientas.
3. Facilita el trabajo de los motores de búsqueda y desarrolladores.
4. Permite que el navegador cree un **árbol de accesibilidad (AOM)** con roles 
claros (ej. banner, navegación, pie de página).

## Rol (`role`):
- Define la función de un elemnto para tecnologías de asistencia.
- Ejemplo: `<buton>` tiene el rol "button" implícito. Si usas `role='button'` en 
otro elemento, solo le dices a un lector de panatlla que es un botón, pero no ganas
la funcionalidad automática de `<button>`.

## Regla de oro:
- **Usa la etiqueta que mejor represente el contenido** (por significado, no por estilo).
- Deja el diseño a CSS, no a HTML.
- Así ahorras trabajo, evitas errores y hace que tu web sea más fácil de usar para todos.

# Chuleta de Elementos HTML Semánticos

| Elemento      | Función principal                                          | Rol implícito                              |
|---------------|------------------------------------------------------------|---------------------------------------------|
| `<header>`    | Encabezado de una página o sección                         | `banner` (si está al inicio)               |
| `<main>`      | Contenido principal de la página                           | `main`                                     |
| `<nav>`       | Menú o enlaces de navegación                               | `navigation`                               |
| `<section>`   | Bloque temático de contenido                               | `region`                                   |
| `<article>`   | Contenido independiente (noticia, post, etc.)              | `article`                                  |
| `<aside>`     | Contenido secundario o relacionado (barra lateral)         | `complementary`                            |
| `<footer>`    | Pie de página de una página o sección                      | `contentinfo` (si está al final global)    |
| `<h1>`-`<h6>` | Títulos y subtítulos jerárquicos                           | `heading`                                  |
| `<p>`         | Párrafo de texto                                           | `paragraph`                                |
| `<ul>` / `<ol>` | Lista desordenada / ordenada                              | `list`                                     |
| `<li>`        | Elemento de lista                                          | `listitem`                                 |
| `<table>`     | Tabla de datos                                             | `table`                                    |
| `<th>`        | Encabezado de tabla                                        | `columnheader` o `rowheader`               |
| `<tr>`        | Fila de tabla                                              | `row`                                      |
| `<td>`        | Celda de tabla                                             | `cell`                                     |
| `<form>`      | Formulario                                                 | `form`                                     |
| `<label>`     | Etiqueta de campo de formulario                            | `label`                                    |
| `<button>`    | Botón interactivo                                          | `button`                                   |
| `<a>`         | Enlace                                                     | `link`                                     |
| `<figure>`    | Imagen o contenido ilustrativo con su descripción         | `figure`                                   |
| `<figcaption>`| Descripción de `<figure>`                                  | `figcaption`                               |

---
💡 **Consejo**: Usa siempre la etiqueta que mejor describa el contenido, no la que "se vea bien". La apariencia se maneja con CSS.

