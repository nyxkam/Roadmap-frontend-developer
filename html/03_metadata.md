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
<meta name='x:title' content='Título para X'/>
<meta name='x:description' content='Descripción en X'/>
<meta name='x:image:src' content='https://ejemplo.com/imagen.png'/>
<meta name='x:creator' content='@usuario'/>
```

## 5. Metaetiquetas para aplicacione web
Mejorna integración en dispositivos móviles y PWA.
```html
<!-- Modo app en iOS/Android -->
<meta name='apple-mobile-web-app-capable' content='yes'/>
<meta name='mobile-web-app-capable' content='yes'/>
<!-- Nombre corto -->
<meta name='apple-mobile-web-app-title' content='AppName'/>
<meta name='application-name' content='AppName'/>
```

## 6. Otros elementos relacionados 
- Iconos para apps: 
```html
<link rel='apple-touch-startup-image' href='icons/ios-portrait.png' media='orientation: portrait'/>
<link rel='icon' type='image/png' href='/images/favicon.png'/>
```

- Idioma y versiones alternativas:
```html
<link rel='alternate' href='https://ejemplo.com/fr/' hreflang='fr-FR'/>
```

- Canonical URL:
```html
<link rel='canonical' href='https://ejemplo.com'/>
```

- Archivo de manifiesto PWA: 
```html
<link rel='mainfest' href='/app.webmanifest'/>
```

# Tabla de metaetiquetas HTML más comunes

| Tipo / Uso                           | Etiqueta de ejemplo                                                                 | Descripción breve |
|--------------------------------------|--------------------------------------------------------------------------------------|-------------------|
| **Charset**                          | `<meta charset="utf-8" />`                                                          | Define la codificación de caracteres del documento. |
| **Viewport (Responsive)**            | `<meta name="viewport" content="width=device-width, initial-scale=1.0" />`          | Ajusta el contenido a dispositivos móviles. |
| **Descripción SEO**                   | `<meta name="description" content="Breve resumen del contenido" />`                 | Texto mostrado en resultados de búsqueda. |
| **Robots**                           | `<meta name="robots" content="noindex, nofollow" />`                                 | Indica a buscadores si indexar o seguir enlaces. |
| **Color del tema**                   | `<meta name="theme-color" content="#226DAA" />`                                      | Cambia el color de la interfaz del navegador. |
| **Open Graph - Título**              | `<meta property="og:title" content="Título de la página" />`                         | Título mostrado en redes sociales. |
| **Open Graph - Descripción**         | `<meta property="og:description" content="Texto descriptivo" />`                     | Descripción para compartir en redes sociales. |
| **Open Graph - Imagen**              | `<meta property="og:image" content="https://ejemplo.com/imagen.png" />`              | Imagen usada en redes sociales. |
| **Twitter Card - Título**            | `<meta name="twitter:title" content="Título para Twitter" />`                        | Título específico para Twitter. |
| **Twitter Card - Descripción**       | `<meta name="twitter:description" content="Descripción en Twitter" />`               | Texto mostrado al compartir en Twitter. |
| **Twitter Card - Imagen**            | `<meta name="twitter:image:src" content="https://ejemplo.com/img.png" />`            | Imagen para Twitter. |
| **Modo App en iOS/Android**          | `<meta name="apple-mobile-web-app-capable" content="yes" />`                         | Muestra el sitio como app en móviles. |
| **Nombre corto App**                 | `<meta name="application-name" content="AppName" />`                                 | Nombre reducido para pantalla de inicio. |
| **Icono Favicon**                    | `<link rel="icon" type="image/png" href="/favicon.png" />`                           | Icono mostrado en la pestaña del navegador. |
| **Versión alternativa por idioma**   | `<link rel="alternate" href="https://ejemplo.com/fr/" hreflang="fr-FR" />`            | Indica versiones del sitio en otros idiomas. |
| **URL canónica**                     | `<link rel="canonical" href="https://ejemplo.com" />`                                | URL principal para evitar contenido duplicado. |
| **Manifiesto PWA**                   | `<link rel="manifest" href="/app.webmanifest" />`                                    | Configuración para aplicaciones web progresivas. |

---
💡 **Recomendación:**  
Incluye solo las etiquetas necesarias para tu proyecto y evita prácticas obsoletas como `meta keywords` o `refresh` automáticos.

