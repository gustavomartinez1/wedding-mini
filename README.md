# 🌸 Veltrux Wedding Mini Template

Plantilla de sitio de bodas para el Plan Mini de Veltrux.

## Estructura de Archivos

```
/
├── index.html         # Página principal
├── styles.css       # Estilos con variables CSS
├── assets/
│   ├── hero.jpg   # Foto hero (1920x1080)
│   └── favicon.ico
└── .github/
    └── workflows/
        └── deploy.yml
```

## Personalización de Colores

En `styles.css`, modifica las variables CSS en `:root`:

```css
:root {
  /* Colores */
  --color-crema: #FAF7F2;    /* Fondo principal */
  --color-dorado: #C9A84C;    /* Acentos y títulos */
  --color-texto: #2D2D2D;     /* Texto principal */
  
  /* Fuentes */
  --font-titulo: 'Cormorant Garamond', serif;
  --font-cuerpo: 'Lato', sans-serif;
}
```

## Personalización de Textos (index.html)

### Hero Section
- Nombres: `Nombre Ella` y `Nombre Él` (líneas 27, 31)
- Fecha: `15 de Junio de 2025` (línea 35)

### Info Section
- Fecha del evento: línea 67
- Hora: línea 74 (Ceremonia y Cócket)
- Dress Code: línea 81
- Ubicación: líneas 91-92 (nombre y dirección)

### RSVP Section
- Formspree ID: cambia `TU_FORM_ID` en el atributo `action` del formulario (línea 108)
- Fecha límite: línea 103

### Mapa Section
- Coordenadas Google Maps: modifica el `src` del iframe (línea 133)

## Reemplazar Foto Hero

1. Coloca tu imagen en `assets/hero.jpg`
2. Resolución recomendada: 1920x1080px
3. Formato: JPG o WebP
4. Peso máximo: 500KB (para LCP < 2.5s)

### Generar coords Google Maps:
1. Ve a Google Maps
2. Busca la ubicación
3. Click en "Compartir" > "Insertar un mapa"
4. Copia el src del iframe

## Configurar Formspree

1. Ve a https://formspree.io/
2. Crea una cuenta
3. Crea un nuevo form
4. Copia el form ID (último segmento de la URL)
5. Reemplaza `TU_FORM_ID` en index.html

## Deploy a Cloudflare Pages

### Opción 1: GitHub Actions (automático)
1. Sube el proyecto a GitHub
2. Ve a Settings > Secrets
3. Agrega:
   - `CLOUDFLARE_API_TOKEN` (Token de API)
   - `CLOUDFLARE_ACCOUNT_ID` (ID de cuenta)
4. Haz push a main → deploy automático

### Para obtener credenciales:
1. Ve a Cloudflare Dashboard
2. Profile > API Tokens
3. Crea token con permisos "Edit Cloudflare Pages"
4. Account ID está en Overview

### Opción 2: Manual (Wrangler)
```bash
npx wrangler pages project create wedding-mini
npx wrangler pages deploy . --project-name=wedding-mini
```

## Web Vitals

- LCP < 2.5s: imagen con `loading="lazy"` no es necesaria en hero
- Usa imagen optimizada: WebP, < 500KB
- Considera usar `fetchpriority="high"` en el hero

## Tecnologías Usadas

- HTML5 + CSS3 puro
- Tailwind CDN (solo clases utilitarias)
- Google Fonts ( Cormorant Garamond + Lato)
- Formspree (formulario)
- Google Maps (iframe)

## Licencia

Uso exclusivo Veltrux. No redistribuir.