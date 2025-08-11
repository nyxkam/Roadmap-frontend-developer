# Metaetiquetas en HTML

## 1. Concepto
Las **metaetiquetas** (`<meta>`) definen metadatos que no pueden representarse con `<title>`, `<link>`, `<script>`, `<style>` o `<base>`.  
Se ubican en el `<head>` y afectan cómo el navegador, motores de búsqueda y redes sociales interpretan la página.

---

## 2. Tipos principales

### a) Directivas pragma (`http-equiv`)
Replican configuraciones de encabezados HTTP.  
**Ejemplos:**
```html
<!-- Establecer conjunto de caracteres -->
<meta charset="utf-8" />

<!-- Política de seguridad de contenido -->
<meta http-equiv="content-security-policy" content="default-src https:" />

<!-- Evitar: auto-actualización y redirección -->
<meta http-equiv="refresh" content="60; https://ejemplo.com" />
```

### b) Metadatos con nombre (`name`)
Definen información usada por navegadores y motores de búsqueda.
**Ejemplo**

```html
<!-- Descripción SEO -->
<meta name='description' content='Breve resumen del contenido'/>
<!-- Evitar meta keywords (ya no son útiles ) -->
<!-- Robots (indexar o no) -->
<meta name='robots' content='noindex, nofollow'/>
<!-- Color de l tema -->
<meta name='theme-color' content='#226DAA' media='(prefers-color-scheme: dark)'/>
```

## 3. Open Graph (OG)
Protocolo para redes sociales como Facebook o LinkedIn. Usa `property` en lugar de 
`name`.
**Ejemplo**
```html
<meta property='og:title' content='Título de la página'/>
<meta property='og:description' content='Descripción para rede sociales'/>
<meta property='og:image' content='https://ejemplo.com/imagen.png'/>
<meta property='og:image:alt' content='Descripción de la imagen'/>
```

## 4. X Cards 
Similar a Open Graph, pero con `name='x:...`.
**Ejemplo**
```html

```
