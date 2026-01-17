# 🏢 Especificación Técnica del Proyecto
## Landing Page Premium - Torres del Poeta

---

## 📋 Resumen Ejecutivo

Este proyecto contiene **10 variantes de diseño** para una landing page de listado de departamento premium en alquiler, ubicado en el edificio **Torres del Poeta** en La Paz, Bolivia.

| Aspecto | Detalle |
|---------|---------|
| **Tipo de Proyecto** | Landing Page Inmobiliaria |
| **Propiedad** | Departamento Premium |
| **Ubicación** | Av. Arce, La Paz, Bolivia |
| **Precio Mensual** | Bs. 8,000 |
| **Tecnología Frontend** | HTML5 + TailwindCSS CDN |

---

## 📁 Estructura del Proyecto

```
45_web_depto/
└── src/
    └── stitch_premium_apartment_listing_v1/
        └── stitch_premium_apartment_listing_v1/
            ├── premium_apartment_listing_v1_1/   ← Variante 1 (Estilo Lujoso Dorado)
            │   ├── code.html
            │   └── screen.png
            ├── premium_apartment_listing_v1_2/   ← Variante 2
            │   ├── code.html
            │   └── screen.png
            ├── premium_apartment_listing_v2_1/   ← Variante 3
            │   ├── code.html
            │   └── screen.png
            ├── premium_apartment_listing_v2_2/   ← Variante 4
            │   ├── code.html
            │   └── screen.png
            ├── premium_apartment_listing_v2_3/   ← Variante 5 (Solo screenshot)
            │   └── screen.png
            ├── premium_apartment_listing_v2_4/   ← Variante 6
            │   ├── code.html
            │   └── screen.png
            ├── premium_apartment_listing_v2_5/   ← Variante 7 (Estilo Minimalista)
            │   ├── code.html
            │   └── screen.png
            ├── premium_apartment_listing_v2_6/   ← Variante 8 (Solo screenshot)
            │   └── screen.png
            ├── premium_apartment_listing_v2_7/   ← Variante 9 (Solo screenshot)
            │   └── screen.png
            └── premium_apartment_listing_v2_8/   ← Variante 10 (Solo screenshot)
                └── screen.png
```

---

## 🎨 Stack Tecnológico

### Frontend
| Tecnología | Versión/Fuente | Uso |
|------------|----------------|-----|
| **HTML5** | Latest | Estructura semántica |
| **TailwindCSS** | CDN (con plugins forms, typography) | Framework de estilos |
| **Google Fonts** | CDN | Tipografías |
| **Material Icons** | Google Fonts CDN | Iconografía |

### Tipografías Utilizadas
- **Playfair Display** (serif) - Títulos y encabezados de lujo
- **Inter** (sans-serif) - Texto de cuerpo y UI

### Paleta de Colores

#### Variante 1 (Estilo Lujoso)
| Variable | Código | Uso |
|----------|--------|-----|
| `primary` | `#C5A059` | Acento dorado premium |
| `background-light` | `#FDFCFB` | Fondo claro |
| `background-dark` | `#0F172A` | Fondo oscuro |
| `navy-900` | `#0A0F1D` | Navy profundo |
| `navy-800` | `#141C2F` | Navy secundario |

#### Variante 2 (Estilo Minimalista)
| Variable | Código | Uso |
|----------|--------|-----|
| `primary` | `#1A1A1A` | Negro elegante |
| `background-light` | `#FFFFFF` | Blanco puro |
| `background-dark` | `#0F172A` | Modo oscuro |

---

## 🏗️ Arquitectura de Componentes

### 1. Header / Navegación
```
┌─────────────────────────────────────────┐
│  🏢 Logo        │  EN/ES  │  ☰ Menú    │
└─────────────────────────────────────────┘
```

**Características:**
- Posición: `fixed` / `sticky` (según variante)
- Efecto glassmorphism: `backdrop-blur-md`
- Selector de idioma (EN/ES)
- Menú hamburguesa para navegación móvil
- Branding: "Torres del Poeta" o "POETA"

---

### 2. Hero Section (Imagen Principal)

**Variante 1 - Estilo Inmersivo:**
```
┌────────────────────────────────────────────┐
│                                            │
│         [Imagen Full-Height]               │
│              480px altura                  │
│                                            │
│  ┌──────────┐                              │
│  │ EXCLUSIVO│  ← Badge dorado              │
│  └──────────┘                              │
│  ╔════════════════════════════════╗        │
│  ║  Premium Living                ║        │
│  ║  📍 Av. Arce, La Paz          ║        │
│  ║                                ║        │
│  ║  Precio Mensual               ║        │
│  ║  Bs. 8,000   [Consultar Ahora]║        │
│  ╚════════════════════════════════╝        │
└────────────────────────────────────────────┘
```

**Variante 2 - Estilo Grid:**
```
┌────────────────────────────────────────────┐
│  [Imagen aspect-ratio 4/5]                 │
│                                            │
│     Torres del Poeta                       │
│     La Paz, Bolivia • Av. Arce             │
└────────────────────────────────────────────┘
┌────────────────────────────────────────────┐
│          MONTHLY RENT                      │
│          Bs. 8,000                         │
│                                            │
│    [═══ Book a Viewing ═══]                │
│      Immediate Availability                │
└────────────────────────────────────────────┘
```

---

### 3. Stats Card (Características Principales)

```
┌─────────────────────────────────────────────┐
│                                             │
│   📏 171 m²  │  🛏️ 4 Dorm  │  🚿 4 Baños   │
│     Área     │  Dormitorios │    Baños      │
│                                             │
└─────────────────────────────────────────────┘
```

**Propiedades del Departamento:**
| Característica | Valor |
|----------------|-------|
| Área Total | 171 m² |
| Dormitorios | 4 (En-suite) |
| Baños | 4 Completos |
| Piso | Alto |
| Exposición | Este-Norte |

---

### 4. Galería de Interiores

**Diseño:** Carrusel horizontal con scroll
```
┌────────────────────────────────────────────┐
│  Interiores Lujosos                        │
│                                            │
│  ┌──────────┐  ┌──────────┐  ┌──────────┐  │
│  │          │  │          │  │          │→ │
│  │  Img 1   │  │  Img 2   │  │  Img 3   │  │
│  │          │  │          │  │          │  │
│  └──────────┘  └──────────┘  └──────────┘  │
│                                            │
│  Descripción del espacio...                │
└────────────────────────────────────────────┘
```

**Contenido:**
- Sala de estar luminosa
- Interiores espaciosos
- Vista nocturna de la ciudad
- Sistema de calefacción por radiadores

---

### 5. Grid de Detalles de Propiedad

```
┌─────────────────┬─────────────────┐
│  📐 Piso Alto   │  ☀️ Luz Natural │
├─────────────────┼─────────────────┤
│  🔥 Calefacción │  🛡️ Seguridad  │
│                 │     24/7        │
└─────────────────┴─────────────────┘
```

**Características Destacadas:**
- Piso alto con vistas panorámicas
- Iluminación natural abundante
- Sistema de calefacción por radiadores
- Seguridad 24/7
- Ventanas termopanel (aislamiento térmico/acústico)

---

### 6. Sección "The Building" (Amenidades)

**Diseño:** Fondo oscuro navy con iconos dorados

```
┌────────────────────────────────────────────┐
│  The Building                              │
│  LIFE AT TORRES DEL POETA                  │
│                                            │
│  🛍️ Centro Comercial & Supermercado        │
│     Acceso directo a tiendas y servicios   │
│                                            │
│  💪 Gimnasio de Nivel Mundial              │
│     Instalaciones de primer nivel          │
│                                            │
│  🍽️ Food Court Exclusivo                   │
│     Variedad gastronómica                  │
│                                            │
│  ┌────────────────────────────────────┐    │
│  │ 🅿️ Parqueo Opcional               >│    │
│  │    Disponible bajo solicitud       │    │
│  └────────────────────────────────────┘    │
└────────────────────────────────────────────┘
```

**Amenidades del Edificio:**
| Amenidad | Descripción |
|----------|-------------|
| Centro Comercial | Acceso directo al mall integrado |
| Supermercado | Servicios básicos sin salir del edificio |
| Gimnasio | Instalaciones fitness de primer nivel |
| Food Court | Variedad gastronómica exclusiva |
| Parqueo | Opcional, disponible bajo solicitud |
| Seguridad | Servicio de conserjería 24/7 con control biométrico |

---

### 7. Sección de Términos de Alquiler (Variante Minimalista)

```
┌────────────────────────────────────────────┐
│  ┌────────────────────────────────────┐    │
│  │        LEASE TERMS                 │    │
│  │                                    │    │
│  │  Monthly Rent ........... Bs. 8,000│    │
│  │  Maintenance (Expensas) . ~Bs. 500 │    │
│  │  Parking Space ........ Optional   │    │
│  │  Property Type ... Premium Resid.  │    │
│  │                                    │    │
│  │  [═══ Request Documents ═══]       │    │
│  │  [─── Call Agent ───────────]      │    │
│  └────────────────────────────────────┘    │
│                                            │
│  Managed by Elite Realty Group             │
│  License #88219-LP • Torres del Poeta      │
└────────────────────────────────────────────┘
```

**Condiciones de Alquiler:**
| Concepto | Monto |
|----------|-------|
| Alquiler Mensual | Bs. 8,000 |
| Expensas/Mantenimiento | ~Bs. 500 aprox. |
| Parqueo | Opcional |
| Tipo de Propiedad | Residencial Premium |

---

### 8. Footer / Contacto

```
┌────────────────────────────────────────────┐
│       Contacto para Visitas                │
│                                            │
│  📞 +591 700 00000                         │
│  ✉️ ventas@torresdelpoeta.bo               │
│                                            │
│  © 2024 Luxury Real Estate Bolivia         │
└────────────────────────────────────────────┘
```

**Información de Contacto:**
- Teléfono: +591 700 00000
- Email: ventas@torresdelpoeta.bo / enio@laejarr.poeta.com
- Agente: Elite Realty Group
- Licencia: #88219-LP

---

### 9. Barra de Acción Fija (Bottom Bar)

**Variante 1 - CTA Principal:**
```
┌────────────────────────────────────────────┐
│  [═══ 📅 Agendar Visita ═══]   [💬 Chat]   │
└────────────────────────────────────────────┘
```

**Variante 2 - Navegación App-like:**
```
┌────────────────────────────────────────────┐
│   🏠 Home  │  ❤️ Fav  │  💬 Chat  │  👤 User│
└────────────────────────────────────────────┘
```

---

## 📱 Diseño Responsivo

### Configuración Mobile-First
- **Max-width contenedor:** `max-w-md` (448px)
- **Breakpoints implícitos:** Diseño optimizado para móviles
- **Viewport mínimo:** `min-height: max(884px, 100dvh)`

### Elementos Responsivos
| Elemento | Comportamiento |
|----------|----------------|
| Header | Fixed/Sticky con blur |
| Galería | Scroll horizontal nativo |
| Grid Stats | 2 columnas adaptables |
| Bottom Bar | Fixed bottom |

---

## ✨ Efectos y Animaciones

### CSS/Tailwind Classes Utilizadas

| Efecto | Clase | Descripción |
|--------|-------|-------------|
| Glassmorphism | `backdrop-blur-md bg-white/80` | Efecto vidrio esmerilado |
| Gradiente oscuro | `bg-gradient-to-t from-black/40` | Overlay para legibilidad |
| Transiciones | `transition-all duration-300` | Animaciones suaves |
| Hover scale | `active:scale-95` | Feedback táctil |
| Sombra elevada | `shadow-xl` | Elevación de cards |
| Bordes redondeados | `rounded-2xl`, `rounded-full` | Estética moderna |

### Modo Oscuro
- Soporte completo via `dark:` prefixes
- Toggle automático via `darkMode: "class"`

---

## 🔗 Integraciones Externas

### Imágenes (Google Cloud Storage)
Las imágenes están alojadas en `lh3.googleusercontent.com/aida-public/`

### CDN Utilizados
| Recurso | URL |
|---------|-----|
| TailwindCSS | `cdn.tailwindcss.com` |
| Google Fonts | `fonts.googleapis.com` |
| Material Icons | `fonts.googleapis.com` |

---

## 📊 Comparativa de Variantes

| ID | Estilo | Paleta | Hero | Stats | CTA Principal |
|----|--------|--------|------|-------|---------------|
| v1_1 | Lujoso | Dorado/Navy | Inmersivo 480px | Card flotante | "Consultar Ahora" |
| v1_2 | Lujoso | Dorado/Navy | Similar a v1_1 | Card flotante | "Consultar Ahora" |
| v2_1 | Semi-minimal | Mixto | Grid moderno | Grid 2x2 | "Book a Viewing" |
| v2_2 | Semi-minimal | Mixto | Grid moderno | Grid 2x2 | "Book a Viewing" |
| v2_3 | Hero grande | Neutro | Carrusel full-width | Iconos simples | WhatsApp + Booking |
| v2_4 | Minimalista | Negro/Blanco | Grid vertical | Grid 2x2 | "Book a Viewing" |
| v2_5 | Minimalista | Negro/Blanco | Grid vertical | Grid 2x2 bordes | "Book a Viewing" |
| v2_6 | Hero grande | Neutro | Carrusel full-width | - | WhatsApp + Booking |
| v2_7 | Info-heavy | Neutro | Sin hero visible | Completo con iconos | "Agendar Visita" |
| v2_8 | Hero grande | Neutro | Carrusel full-width | - | WhatsApp + Booking |

---

## 🎯 Funcionalidades Interactivas (Propuestas)

> [!NOTE]
> Los archivos HTML actuales son mockups estáticos. Las siguientes funcionalidades requerirían JavaScript adicional:

### Pendientes de Implementación
- [ ] Carrusel de imágenes funcional
- [ ] Formulario de contacto
- [ ] Integración WhatsApp (click-to-chat)
- [ ] Toggle de modo oscuro
- [ ] Selector de idioma funcional
- [ ] Menú hamburguesa desplegable
- [ ] Validación de formularios

---

## 📝 Recomendaciones

### Optimizaciones Sugeridas

1. **Performance:**
   - Migrar imágenes a un CDN propio con optimización WebP
   - Implementar lazy loading para imágenes
   - Considerar self-hosting de TailwindCSS (build production)

2. **SEO:**
   - Agregar meta descriptions
   - Implementar Schema.org para propiedades inmobiliarias
   - Optimizar alt texts de imágenes

3. **Accesibilidad:**
   - Agregar labels a botones icon-only
   - Mejorar contraste en algunos textos
   - Agregar skip-links para navegación

4. **Conversión:**
   - Implementar tracking de analytics
   - A/B testing entre variantes
   - Formulario de captura de leads

---

## 📞 Información del Inmueble

### Resumen Ejecutivo del Departamento

| Característica | Detalle |
|----------------|---------|
| **Edificio** | Torres del Poeta |
| **Ubicación** | Av. Arce, La Paz, Bolivia |
| **Tipo** | Departamento Premium Residencial |
| **Área** | 171 m² |
| **Dormitorios** | 4 (2 en-suite) |
| **Baños** | 4 completos |
| **Piso** | Alto |
| **Orientación** | Este-Norte |
| **Alquiler** | Bs. 8,000/mes |
| **Expensas** | ~Bs. 500/mes |
| **Parqueo** | Opcional (bajo solicitud) |
| **Disponibilidad** | Inmediata |

### Características Premium
- ✅ Ventanas termopanel (aislamiento térmico y acústico)
- ✅ Calefacción por radiadores
- ✅ Iluminación natural abundante
- ✅ Vistas panorámicas de La Paz
- ✅ Seguridad 24/7 con control biométrico
- ✅ Acceso a gimnasio
- ✅ Centro comercial integrado
- ✅ Food court en el edificio

---

*Documento generado el 16 de enero de 2026*
*Proyecto: 45_web_depto - Landing Page Torres del Poeta*
