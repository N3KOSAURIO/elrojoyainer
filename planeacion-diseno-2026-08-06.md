# planeacion-diseno — elrojoyainer v2.0

**Fecha**: 2026-08-06
**Template base**: Influtics (influtics-1.0.0)
**Objetivo**: Adaptar template Influtics a Yainer, paleta terracota, sin saturación

---

## 1. Análisis del template

El template Influtics tiene estructura SCSS profesional con:
- **Variables**: `--tt-pink: #F820A3`, `--tt-gold: #FFA945`, gradiente rosa→dorado
- **Tipografía**: Inter (Google Fonts)
- **Layout**: Multi-page con secciones modulares (header, hero, social-links, reels, service, intro, live, videos, contact, article, footer)
- **Dependencias**: Bootstrap 5, Swiper, Splide, Plyr, SlimSelect, noUiSlider, FsLightbox
- **16 páginas HTML**: index, about, blog, blog-details, contact, login, register, checkout, pricing, service, service-details, video-shop, video-shop-details, videos-1/2/3, video-details

## 2. Dirección creativa

### Paleta — Terracota Colombiano (desde CONTEXT.md)

| Token | Hex | Uso |
|-------|-----|-----|
| `--tt-pink` → `--tt-terracota` | `#C67B5C` | Primario (reemplaza pink) |
| `--tt-gold` → `--tt-ambar` | `#E8A838` | Acento (reemplaza gold) |
| `--tt-gradient-1` | `linear-gradient(90deg, #C67B5C, #E8A838)` | Gradiente principal |
| `--ttLightRed` → `--tt-crema` | `#FFF8F0` | Fondo claro |
| `--ttRed` → `--tt-terracota-dark` | `#A85D3F` | Hover/activo |
| `--black` | `#2D2420` | Texto (café oscuro) |
| `--white` | `#FFFFFF` | Blanco puro |
| `--ttGray` | `#B5B5B5` | Sin cambios |
| `--ttGray2` | `#808080` | Sin cambios |

### Tipografía
- **Mantener Inter** (ya cargada en el template, rápida, profesional)
- Pesos: 400, 500, 600, 700, 800, 900

### Filosofía visual
- **Menos saturación**: el rosa neón (#F820A3) se reemplaza por terracota cálido (#C67B5C)
- **Profesional colombiano**: light mode, tonos tierra, sensación artesanal
- **Conservar estructura**: mismas secciones, mismos componentes, solo cambian colores y contenido

## 3. Plan de cambios

### Fase 1 — Variables y colores (1 archivo)
- `assets/scss/main/_variables.scss`: reemplazar pink/gold por terracota/ámbar

### Fase 2 — Contenido index.html (1 archivo)
- Hero: "I'm Linda Susan" → "Soy Yainer", "Beauty & Lifestyle" → "Creador de Contenido | Pamplona"
- Social links: reemplazar por 3 IG + 1 FB de Yainer
- Reels/Videos: placeholder con los datos del CONTEXT
- Services: Sketches, Producción, Contenido, Colaboraciones
- Intro: Bio de Yainer, "Párchese 0 estrés"
- Contact: email real
- Footer: créditos Yainer

### Fase 3 — Limpieza de páginas innecesarias
- **Eliminar HTML**: login, register, checkout, pricing, video-shop, video-shop-details
- **Conservar HTML**: index, about, blog, blog-details, contact, service, service-details, videos-1/2/3, video-details
- **SCSS**: mantener todo (no afecta tener estilos de páginas no usadas)

### Fase 4 — Imágenes
- Reemplazar `banner-2-img.png` por foto real de Yainer (del Drive)
- Reemplazar `user-dp-2.png` por avatar de Yainer
- Placeholders de video/artículo: mantener los del template (son genéricos)
- Logo SVG: reemplazar "Linda" por "Yainer" (o crear nuevo)

### Fase 5 — Verificación
- Abrir index.html en navegador
- Verificar responsive
- Verificar que todas las secciones cargan con nuevos colores

## 4. Lo que NO se toca

- Estructura SCSS (sections/, pages/, main/)
- Vendor libraries (bootstrap, swiper, splide, plyr, etc.)
- Lógica JS (main.js)
- Fuentes (Inter, Flaticon)
- HTML de páginas que se conservan (se adaptan después si el usuario pide)

## 5. Reglas del vault que aplican

- **Regla 2**: Planear antes de ejecutar ✓ (este documento)
- **Regla 4**: TODO.md inmutable — solo añadir al final
- **Regla 34**: Seguridad — revisar imágenes del Drive antes de usar
- **Regla 49**: Trabajo del vault dentro del vault — resultado final en `Projects/Personales/Elrojoyainer/`
- **Regla 58**: Separación Pixell ↔ Personales — esto es Personal, no tocar Pixell
