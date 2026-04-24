# Checklist de Personalización - Plan Mini

## ✅ Antes de Entregar al Cliente

### 1. Textos Principales
- [ ] Nombres de los novios (línea 27 y 31 en index.html)
- [ ] Fecha de la boda (línea 35)
- [ ] Fecha y hora del evento (líneas 67, 74)
- [ ] Dress code (línea 81)
- [ ] Nombre del lugar (línea 91)
- [ ] Dirección completa (línea 92)
- [ ] Fecha límite RSVP (línea 103)

### 2. Fotos y Multimedia
- [ ] Reemplazar `assets/hero.jpg` con foto real (1920x1080, máx 500KB)
- [ ] Verificar que la imagen cargue correctamente
- [ ] (Opcional)Agregar favicon.ico

### 3. Funcionalidad RSVP
- [ ] Crear cuenta en Formspree.io
- [ ] Reemplazar `TU_FORM_ID` en línea 108 de index.html
- [ ] Probar el formulario (enviar una confirmación de prueba)
- [ ] Configurar notificación por email en Formspree

### 4. Mapa
- [ ] Buscar ubicación real en Google Maps
- [ ] Generar nuevo embed iframe
- [ ] Reemplazar src del iframe (línea 133)

### 5. Colores (opcional)
- [ ] Revisar paleta por defecto (crema/dorado/oscuro)
- [ ] Ajustar si es necesario en styles.css (líneas 7-11)

### 6. Deploy
- [ ] Subir a GitHub
- [ ] Configurar secrets de Cloudflare
- [ ] Verificar deploy exitoso
- [ ] Probar en URL de producción

---

## 📋 Notas para el Cliente

copy/paste para enviar:

```
Hola! Aquí tienes tu sitio de boda personalizado.

📍 URL: [TU-DOMINIO.pages.dev]

Para editar:
- Nombres y fecha: en index.html
- Colors: en styles.css (variables CSS)
- Foto hero: replace assets/hero.jpg
- RSVP: usa [TU-FORM-SPREE-LINK]

Cualquier duda, me avisas!
```

---

## 🔧 Mantenimiento

Si necesitas cambiar algo después de entregar:

| Cambio | Dónde | Cómo |
|--------|-------|------|
| Nombres | index.html | Líneas 27, 31 |
| Fecha | index.html | Línea 35 |
| Colors | styles.css | Variables en :root |
| Foto | assets/ | Replace hero.jpg |
| RSVP form | index.html | Cambiar form ID |
| Mapa | index.html | Nuevo embed iframe |

---

## ⚡ Guía Rápida de Troubleshooting

| Problema | Solución |
|---------|---------|
| Imagen no carga | Verificar ruta en index.html línea 24 |
| Form no envía | Verificar form ID en Formspree |
| Mapa no aparece | Verificar src del iframe |
| Fonts no cargan | Chequear conexión a Google Fonts |
| Deploy falló | Verificar secrets de Cloudflare |