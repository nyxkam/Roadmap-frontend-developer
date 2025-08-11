# Estructura del documento HTML

## 1. Declaración de tipo y estructura base

- `<!DOCTYPE html>`: indica al navegador que use el __modo estándar__ (informar sobre la versión de HTML que se usa).
- `<html>`: Elemento raíz. Contiene `<head>` (metadatos) y `<body>` (contenido visible).
- **Atributo** `<lang>`: Define el idioma principal del documento (`<html lang='es-PE'>`).
    + Ejemplo: `<span lang='fr-FR'>Ceci n'est pas une pipe.</span>`

## 2. Elementos esenciales en `<head>`

- **Codifcación**:
    ```html
    <meta charset='utf-8'/>
    ```
    Permite usar todos los carácteres, incluidos emojis

- **Título**:
    ```html
    <title>Machine Learning Workshop</title>
    ```
    Visible en la pestaña, buscadores y redes sociales.

- **Meta viewport**(responsive):
    ```html
    <meta name='viewport' content='width-device-width, initial-scale=1'/>
    ```

## 3. Inclusion de CSS

- **Externa (recomendable)**
    ```html
    <link rel='stylesheet' href='styles.css'>
    ```
- **Interna**
    ```html
    <style>
        :root {
            --theme-color:#226DAA;
        }
    </style>
    ```
- **Con `@import` (menos comun)**
    ```html
    <style>
        @import "style.css";
    </style>
    ```

## 4. Otros usos de `<link>`

- **Favicon**:
    ```html
    <link rel='icon' href='/images/favicon.png' type='image/png' alt='icono de la pagina'/>
    ```

- **Apple/Safari**:
    ```html
    <link rel='apple-touch-icon' sizes='100x100' href='/images/mlwicon.png'/>
    <link rel='mask-icon' href='/images/mlwicon.svg' color='#226DAA'/>
    ```
- **Versiones alternativas / traducciones**:
    ```html
    <link rel='alternate' href='https://.../fr/' hreflang='fr-FR'/>
    ```
- **Canonical**:
    ```html
    <link rel='canonical' href='https://www.machinelearning.com'/>
    ```

## 5. JavaScript

- **Interno** (evitar referenciar elementos que aún no existen):
    ```html
    <script>
        document.getElementById('switch').addEventListener('click', function() {
            document.body.classList.toggle('black');
    })
    </script>
    ```
- **Externo con `defer`** (recomendado para no bloquear renderizado):
    ```html
    <script src='js/switch.js' defer></script>
    ```
- `defer` vs `async`:
    + `defer`: descarga paralela, ejecuta después del parseo del documento.
    + `async`: descarga paralela, ejecuta inmediatamente cuando termina la descarga
    (puede interrumpir renderizado).

## 6. `<base>`
- Define URL/target por defecto para enlaces relativos:

    ```html
    <base href='https://machinelearningworkshop.com' target='_top'/>
    ```
    Solo puede haber un `<base>` por documento y debe de ir antes de URL's relativas usadas.

## 7. Comentarios HTML 
    ```html
    <!--- Esto es un comentario y no se renderiza -->
    ```

## 8. Ejemplo mínimo recomendado 

```html
<!DOCTYPE html>
<head>
    <meta charset='utf-8'/>
    <title>Machine Learning Workshop</title>
    <meta name='viewport' content='width-device-width, initial-scale=1'/>
    <link rel='stylesheet' href='styles.css'/>
    <link rel='icon' href='/images/favicon.png'/>
</head>
<body>

    <!-- Contenido visisble -->
    <script src='scripts/main.js' defer></script>
</body>
```
