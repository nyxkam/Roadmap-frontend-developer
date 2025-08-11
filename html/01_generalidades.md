# Lenguaje de marcado de hipertexto (HTML)

## **Definición**:
Lenguaje estandar para describir la estructura de documentos web 
mediante elementos y atributos.

## **Composición**:
Son árboles de nodos que incluyen elementos HTML y nodos de texto.

## **Función de los elementos**:
Proporcionan semántica y formato para crear componentes como:
- Párrafos, listas y tablas
- Imágenes y controles de formularios

## **Características de los elementos**:
- Pueden tener atributos y contenido (otros elementos o texto)
- Algunos están vacíos y se definen solo por etiquetas/atributos 

## **Categorías de elementos**:
Se dividen en tipos como metadatos, secciones, texto, formato, contenido multimedia,
interactivos y secuencias de comandos.

>[!NOTE] **Palabras Clave**                                                
> Estructura web, semántica, árbol de nodos, atributos, etiquetas.

# Elementos 

## Fucnión de los elementos HTML 
Encierran contenido para definir su apariencia/comportamiento usando etiquetas
con corchetes angulares (`< >`).

## Estructura de un elemento:
- Etiqueta apertura: `<h1>`
- Contenido: Texto o elementos internos (ej: `Taller de aprendizaje automático`)
- Etiqueta de cierre: `</h1>` (misma qye apertura + barra `/`)
  > -> Elemento completo  = Etiqueta de apertura + Contenido + Etiqueta cierre

## Diferencia crucial:
- **Etiqueta**: Solo el marcado entre `< >` (ej: `<h1>` o `</h1>`).
- **Elemento**: Conjunto completo de: 
  > -> (etiquetas + contenido + elementos anidados) 


> [!TIP] **Error común**                                                               
> Muchos usan "etiqueta" y "elementos" indistintamente, pero técnicamente son 
> conceptos distions.                                                         

```html
<h1>Taller de aprendizaje automático</h1>
```

* Etiquetas: `<h1>` y `</h1>`
* Elementos: Todo el bloque (incluye  etiquetas  +  texto contenido)

> [!ATTENTION] **Dato**                                                                          
> Algunas etiquetas de cierre omitidas causan problemas más grandes:              
> No cerrar algunas etiquetas como `<script>`,`<style>`,`<template>`, `<textarea>`
> y `<title>`.                                                                    

## Tipos de elementos en HTML

### 1. **Elementos no reemplazados**
- Ejemplos: `<p>`, `<h1>`, `<ul>`.
- Tienen **etiqueta de apertura** y **etiqueta de cierre** (a veces opcinales).
- Pueden incluir:
 + Texto 
 + Otros elementos (subelementos).
- Usos comunes:
 + Hipervínculos(`<a>`).
 + Encabezados(`<h1>`...`<h6>`).
 + énfasis(`<em>`,`<strong>`).

### 2. **Elementos reemplazados**
- Su contenido **se sustituye por un onbjeto** externo o interfaz gráfica.
- Ejemplos com>unes:
 + `<img>` -> imagen.
  + `<inptu>` -> control de formulario.  
 + `<video>`, `<iframe>`, `<object>`, `<picture>`.

- Características:
 + Apariencia predeterminda según el navegador.
 + Estilo CSS limitado (más en imágenes raster y controles de UI).
 + **SVG**: totalmente escalable y personalizable (dependiendo de cómo se inserte). 

### 3. **Elementos vacios (o nulos)**
- **No tienen contenido interno** ni etiqueta de cierre.
- Opcionalmente se pueden cerrar con una barra (`<img/>`). 
- Ejemplos:
 + `<br>`, `<col>`, `<embed>`, `<hr>`, `<img>`, `<input>`, `<link>`, `<meta>`,
 `<source>`, `<track>`, `<wbr>`.
- La mayoría son reemplazados, pero no todos (ej. `<meta>` no se reemplaza y
solo proporciona información).
- Algunos elementos reemplazados **no son vacios** porque pueden tener contenido 
interno (`<video>`, `<iframe>`).

>[!SUMMARY] En Resumen:                                                                 
> **No reemplazados** -> Contienen texto/elementos, totalmente estilizables.        
> **Reemplazados** -> Sustituidos por un objeto externo o UI; estilizado limitado.  
> **Vacios** -> No tienen contenido ni cierre; pueden ser reemplazados o no.        

# Atributos 
- **Qué son**: Información extra que se añade en la etiqueta de apertura de un elemento 
para definir su comportamiento, apariencia o funcionalidad. 
- **Formato**: `nombre='valor'` (recomendado usar minúsculas y comillas siempre).
- **Tipos**:
    + **Globales**: Pueden usarse en cualquier elemento (`id`, `class`, `style`, etc.).
    + **Específicos**: solo aplican a cietos elementos (`src`, en `<img>`, `href` en `<a>`).
    + **Booleanos**: No requieren valor, solo el nombre (`disable`, `checked`, `ismap`).
- **Reglas importantes**:
    + Solo aparecen en la _etiqueta de apertura_.
    + Si el valor tiene espacios o caracteres espaciales, es obligatorio usar comillas.
    + HTML no distingue mayúsculas, pero CSS y JS si en algunos casos (como `id`,`class`).
    + Buenas prácticas: usar minúsculas, comillas y espacio entre atributos.
>[!DONE] Ejemplo:
```html
<a href='register' title='Ir a registro'>Registro</a>
<img src='switch.svg' alt='Interruptor de luz' ismap>
```

| Tipo de atributo | Descripción | Ejemplo |
|------------------|-------------|---------|
| **Global**       | Se pueden usar en cualquier elemento HTML. | `<div id="main" class="container"></div>` |
| **Específico**   | Solo aplican a ciertos elementos. | `<img src="foto.jpg" alt="Descripción">` |
| **Booleano**     | No requiere valor, solo el nombre (valor implícito `true`). | `<input type="checkbox" checked>` |
| **Con valor**    | Pares `nombre="valor"` que definen configuración o datos. | `<a href="https://ejemplo.com" title="Visitar">Enlace</a>` |
| **Sensible a mayúsculas** | Algunos valores como `id` y `class` distinguen mayúsculas en CSS/JS. | `<div id="MenuPrincipal"></div>` |


