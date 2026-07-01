# ZenderBox — Brand Guidelines (AI Reference)

> Fuente de verdad para cualquier agente de IA, desarrollador o diseñador que trabaje en ZenderBox.
> Última actualización: 2026.

---

## 1. Qué es ZenderBox

Servicio de package-forwarding para clientes latinoamericanos que compran en EE.UU. El cliente recibe una dirección física en Miami (ej. `7971 NW 21 ST, Apto ZB-123301, Doral, FL 33198`), envía paquetes allí y los gestiona desde la app o el dashboard web.

**Mercados**: Colombia, México, Perú, Costa Rica, Rep. Dominicana, Ecuador, Panamá.

**Productos**:
- App móvil (iOS/Android) — canvas 430×932px
- Dashboard web — rail izquierdo 305px + área de contenido
- Web pública — landing/marketing en 1512px desktop

**Usuario de referencia**: Juan Sebastian Acuna · Apto ZB-123301 · Nivel Básico · 1.678/2.000 puntos.

---

## 2. Principio Core: White First

El fondo dominante es **siempre blanco**. Los colores de marca se usan con moderación:
- Acciones primarias (CTAs, botones principales)
- Estados activos en navegación
- Datos clave y highlights
- Capa de fidelización (barras de nivel, logros)

Nunca: gradiente como fondo full-bleed en secciones de contenido extenso. El gradiente tiene impacto porque se usa poco.

---

## 3. Identidad Visual

### Logo

**Wordmark**: "Zender" en cyan `#029ECB` · "Box" en lime `#CCD32A`
**Símbolo**: Dos piezas que forman una Z/B usando el gradiente lime→cyan
**Gradiente del logo**: `linear-gradient(45deg, #CCD32A 0%, #029ECB 85%)`

Versiones disponibles:
- `Hor_color.svg` — horizontal, colores de marca (uso principal)
- `Hor_blanco.svg` — horizontal, todo blanco (sobre fondos de color/gradiente)
- `fav_color.svg` — símbolo solo, colores
- `fav_blanco.svg` — símbolo solo, blanco

**Reglas**:
- Nunca distorsionar ni recolorear el logo
- Sobre fondos cyan o gradiente: usar versión blanca
- Espacio mínimo: 16px alrededor del símbolo

---

## 4. Colores

### Regla de color en texto destacado

**Las palabras de color nunca van con gradiente.** Cuando se colorea texto de marca, cada palabra recibe un color sólido: una en **cyan `#029ECB`** y la otra en **lime `#CCD32A`**. El gradiente se reserva para elementos gráficos (logo, barras de progreso, botones primary, avatares) — nunca para letras.

```
✅ <span style="color:#029ECB">siempre</span> <span style="color:#CCD32A">contigo.</span>
❌ background: linear-gradient(...); -webkit-background-clip: text;
```

---

### Colores primarios de marca

| Token | Hex | Uso |
|-------|-----|-----|
| Cyan (primary) | `#029ECB` | Botones, CTAs, links, tab activo, bordes focused |
| Lime (accent) | `#CCD32A` | Tope del gradiente, barras de nivel, accents |
| **Gradiente** | `linear-gradient(45deg, #029ECB 0%, #CCD32A 85%)` | Botón primary app, sidebar activo, avatares, barras de progreso |
| **Gradiente web** | `linear-gradient(90deg, #CCD32A 0%, #029ECB 85%)` | Botón primary web, hero sections |
| Navy | `#004B72` | Texto principal, encabezados, footer, navbar |
| Dark cyan | `#007B9F` | Hover, pressed, link secundario |

### Neutros

| Hex | Nombre | Uso |
|-----|--------|-----|
| `#1F1F1F` | Muy oscuro | Texto display |
| `#333333` | Cuerpo | Texto principal |
| `#666666` | Secundario | Texto secundario, descripciones |
| `#8A8A8A` | Medio | Texto deshabilitado, placeholders de stats |
| `#B8B8B8` | Placeholder | Inputs placeholder |
| `#DBDBDB` | Divisores | Líneas divisoras |
| `#F6F6F6` | Fondo app | Background de la app, surface deshabilitado |
| `#FFFFFF` | Base | Fondo dominante |

### Estados semánticos (estados de paquete)

| Estado | Color texto | Color fondo | Uso |
|--------|------------|-------------|-----|
| En Tienda | `#0260CB` | `#E8F0FB` | Paquete recibido en tienda |
| En Bodega | `#008C31` | `#F1F6F5` | Paquete en bodega Miami |
| Despachado | `#E66B00` | `#FDF3EA` | En camino a destino |
| En Camino | `#F32735` | `#F4E8E9` | En tránsito internacional |
| Entregado | `#FF28E2` | `#FDE8FB` | Entregado al cliente |

### Semánticos de UI

| Uso | Hex |
|-----|-----|
| Error (app) | `#F32735` |
| Error (web) | `#CC1111` |
| Success | `#008C31` |
| Warning | `#E66B00` |

---

## 5. Tipografía

> **Regla de color en titulares**: cuando un titular usa dos colores de marca, cada palabra lleva un color sólido — una en cyan `#029ECB`, otra en lime `#CCD32A`. Nunca gradiente en texto.

### App móvil y Dashboard web

**Typeface único**: **Plus Jakarta Sans**
Pesos usados: 500 (Medium), 700 (Bold), 800 (ExtraBold — solo código de referido).

| Estilo | Peso | Size | Line-height | Uso |
|--------|------|------|-------------|-----|
| Display L | Bold 700 | 32px | 38px | Títulos de pantalla principal |
| Display | Bold 700 | 24px | 32px | Subtítulos de sección |
| Section Title | Bold 700 | 19px | 24px | Encabezados de sección |
| Title | Bold 700 | 16px | 20px | Títulos de card |
| Title Small | ExtraBold 800 | 14px | 18px | — |
| Button | ExtraBold 800 | 16px | 20px | Labels de botón |
| Body | Medium 500 | 14px | 18px | Texto principal |
| Placeholder | Medium 500 | 13px | 16px | Placeholders de input |
| ID | Bold 700 | 13px | 16px | Códigos, IDs |
| NavBar | Medium 500 | 12px | 15px | Tabs inactivos |
| NavBar On | Bold 700 | 12px | 15px | Tab activo |
| Label | Bold 700 | 12px | 15px | Labels de campo |
| Caption | Medium 500 | 10px | 13px | Metadata, fechas |
| Tag | Medium 500 | 10px | 13px | Badges, tags |

### Web pública (landing/marketing)

Dos familias:
- **Exo** — display, titulares, botones, nav. Pesos: 400, 600, 700, 800.
- **Plus Jakarta Sans** — párrafos, labels, captions, footer.

| Estilo | Font | Peso | Size | LH |
|--------|------|------|------|----|
| display | Exo | Bold 700 | 67px | 77px |
| title | Exo | Bold 700 | 48px | 58px |
| title s | Exo | Bold 700 | 37px | 43px |
| heading | Jakarta | Medium 500 | 21px | 28px |
| button-big | Jakarta | Bold 700 | 18px | 24px |
| body | Jakarta | Regular 400 | 18px | 24px |
| body s | Jakarta | Regular 400 | 16px | 19px |
| label | Jakarta | Medium 500 | 14px | 18px |
| caption | Jakarta | Regular 400 | 14px | 18px |

**Regla de botones web**: label siempre Exo Bold UPPERCASE.

---

## 6. Casing y Escritura

| Elemento | Casing |
|----------|--------|
| Títulos de pantalla/sección | Sentence case |
| Botones | Sentence case Bold (app) / UPPERCASE Bold (web) |
| Badges, categorías | UPPERCASE |
| Metadata, campos | Capitalized |
| Nav web | UPPERCASE |

---

## 7. Componentes — App y Dashboard

### Botones

| Tipo | Fill | Alto | Radius |
|------|------|------|--------|
| Primary | `linear-gradient(45deg, #029ECB 0%, #CCD32A 85%)`, label blanco Bold | 52px | 8px |
| Secondary | Cyan `#029ECB`, label blanco | 52px | 8px |
| Stroke | `#F6F6F6` + 1px `#007B9F` border | 52px | 8px |
| Small Primary | Mismo fill | 34px | 8px |
| Link | Inline, Navy `#004B72` Bold + chevron | — | — |

Hover: `brightness(1.05)` · Press: `scale(0.98)` + `brightness(0.95)` · 150ms ease.

### Cards

- Radius: **10px**
- Fill: blanco
- Borde opcional: `1px solid #029ECB` (branded cards)
- Sin sombra (convención del sistema)
- Padding: 24px (default)

### Inputs

- Radius: 8px
- Border: `1px solid #B8B8B8`
- Focused: `#029ECB`
- Error: `#F32735`
- Disabled: bg `#F6F6F6`

### Avatares

- Forma: circular
- Fill: gradiente `linear-gradient(45deg, #029ECB 0%, #CCD32A 85%)`
- Contenido: monograma blanco
- Tamaños: 44×44px (headers), 105×105px (perfil)

### StateBadge (estados de paquete)

- Pill outline: borde + texto + fondo del color del estado
- Radio: 99px
- Si el estado no existe: gris neutro `#8A8A8A`

### Gamificación

- Level badge: texto "Nivel básico" en pill con gradiente
- Level bar: 5px (compacto) / 20px (detalle) · fill gradiente
- Texto canónico: *"1.678 / 2.000 puntos"* (miles con punto, no coma)

---

## 8. Componentes — Web pública

### Botones

| Tipo | Fill | Label |
|------|------|-------|
| Button_big_primary | `linear-gradient(90deg, #CCD32A 0%, #029ECB 85%)` | Blanco Exo Bold UPPERCASE |
| Button_big_secondary | Cyan `#029ECB` | Blanco Exo Bold UPPERCASE |
| Button_big_tertiary | Outlined navy | Navy Exo Bold UPPERCASE |
| Button_sm_secondary | Cyan | Blanco |

Radius botones web: **900px**.

### Cards web

- Radius: **24px**
- Fill: blanco
- Padding: 24–32px
- Título: Exo Bold 21/28 navy
- Body: Exo Regular 18/24 **cyan** (no navy — es deliberado)

### Motion web

- Entrada cards: fade + slide up 4–8px · 200–300ms ease-out
- Hover botón: gradiente 10% más brillante
- Press: scale(0.98) · 80ms
- Nav sticky: 116px → 69px al hacer scroll

---

## 9. Espaciado y Layout

### App

- Canvas: 430×932px
- Padding lateral: 16px
- Cards padding: 20px
- Secciones: 32px

| Token | Valor |
|-------|-------|
| margin | 16px |
| xxxs | 2px |
| xxs | 4px |
| xs | 8px |
| sm | 10px |
| m | 12px |
| md | 16px |
| xl | 20px |
| xxl | 32px |

Gaps: 4 / 8 / 12 / 16 / 24 / 48px

### Dashboard web

- Rail izquierdo: 305px
- Padding área contenido: 24px 40px 64px
- Container: L=1286px · M=1068px · S=630px · XS=300px

### Web pública

- Canvas desktop: 1512px · Columna: 1286px · Gutters: 113px
- Canvas mobile: 430px · Padding: 16px

### Radios por producto

| Elemento | App/Dashboard | Web pública |
|----------|---------------|-------------|
| Cards | 10px | 24px |
| Botones | 8px | 900px |
| Avatares/badges/pills | 99px | 900px |
| Inputs | 8px | 8px |

---

## 10. Iconografía

Set custom basado en **Lucide** (stroke icons).

| ZenderBox | Lucide |
|-----------|--------|
| Flecha derecha | `chevron-right` |
| Flecha izquierda | `chevron-left` |
| Cerrar | `x` |
| Ayuda | `help-circle` |
| Buscar | `search` |
| Barcode | `scan-barcode` |
| WhatsApp | `message-circle` |
| Chevron abajo | `chevron-down` |
| Moda | `shirt` |
| Tecnología | `laptop` |
| Hogar | `home` |
| Mascotas | `paw-print` |
| Belleza | `sparkles` |
| Deportes | `dumbbell` |

**Convenciones**:
- Stroke: `1.8px` uniforme
- Tamaño default: 18×18px
- Color: hereda del contexto (navbar inactivo: `#8A8A8A`, activo: cyan)
- Sin fills — solo stroke

---

## 11. Fotografía

### Reglas obligatorias

**El overlay oscuro sobre foto siempre tira a cyan.** Nunca negro puro (`#000`), nunca navy (`#004B72`). El color oscuro de marca es cyan profundo — incluso en las sombras, la identidad visual debe ser reconocible. Ver token exacto en la sección Overlays más abajo.

**La fotografía es siempre la primera opción.** Toda pieza de comunicación debe explorar primero una solución con foto real. Solo si el formato no lo permite (icono, ilustración de proceso, estado vacío) se recurre a ilustración.

**Las fotos se consiguen en bibliotecas libres**, en este orden:
1. **Pexels** — pexels.com (CC0, uso comercial sin atribución)
2. **Unsplash** — unsplash.com (uso comercial libre)
3. **Pixabay** — pixabay.com (uso comercial libre)

**Las fotos van siempre a sangre completa (full bleed).** Cubren el 100 % del área designada sin bordes ni márgenes. El texto y los overlays van sobre la foto extendida.
```css
/* Correcto */
object-fit: cover; width: 100%; height: 100%;
/* Incorrecto: foto con márgenes, marcos o borde visible */
```

### Concepto

ZenderBox existe en el espacio entre el deseo y la llegada. Las fotos capturan:
1. **El deseo** — personas comprando online, navegando tiendas, eligiendo productos
2. **La espera activa** — trackeo en el celular, anticipación
3. **La llegada** — unboxing, alegría genuina, momento de conexión con el producto
4. **El emprendedor** — personas usando ZenderBox para su negocio

### Dirección

- **Luz**: natural, amplia, sin flash artificial
- **Paleta**: tonos cálidos/neutros — no saturar artificialmente
- **Personas**: diversas, latinoamericanas, reales — no modelos de stock evidentes
- **Encuadre**: close-ups de manos/productos + medios con contexto
- **Mood**: cotidiano y aspiracional a la vez — ni lujoso ni precario

### Lo que NO hacer

- Fotos de bodega/almacén para comunicar al usuario final
- Aviones o barcos como metáfora de envío (cliché del sector)
- Personas posando con cajas sin contexto emocional
- Saturación artificial de colores
- Fotos reducidas con márgenes o marcos visibles

### Overlays sobre fotos

Para texto encima de foto — el overlay **siempre tira a cyan**, nunca a negro puro ni navy:
```css
linear-gradient(to top,
  rgba(0,58,85,0.92) 0%,
  rgba(1,75,105,0.78) 25%,
  rgba(2,90,125,0.42) 52%,
  rgba(2,120,160,0.14) 75%,
  transparent 100%
)
```
Para glassmorphism: `background: rgba(255,255,255,0.1); backdrop-filter: blur(16px); border: 1px solid rgba(255,255,255,0.2)`

---

## 12. Ilustraciones isométricas 3D

Estilo: cubos/formas isométricas planas con las caras del gradiente de marca.

Paleta isométrica:
- Cara superior: lime `#CCD32A`
- Cara derecha: cyan `#029ECB`
- Cara izquierda: dark cyan `#007B9F`

Uso: en cards de "cómo funciona", en pantallas de onboarding, en estados vacíos.
Animación: `translateY` suave, 4s ease-in-out, amplitud 6–8px.

---

## 13. Voz y Tono

Ver [`voice.md`](voice.md) para guía completa.

### Resumen rápido

- **Idioma**: Español latinoamericano. Ningún texto de UI en inglés.
- **Trato**: `tu`, `tus`, `tienes`, `hazle`. Nunca "usted".
- **Personalidad**: Empoderador · Transparente · Práctico · Cercano y colombiano
- **Emojis con medida** — no como decoración genérica. Se usan uno a la vez, anclados a una palabra clave, un badge o un elemento de navegación. Nunca dos emojis seguidos, nunca como reemplazo de iconos en UI de producto. En copy: solo si refuerzan un estado o categoría específica (`📦 En bodega`, `✅ Entregado`).
- **Sin em-dashes** (—)

### Copy verbatim importante

- *"Hola, Juan"*
- *"Mis datos en Estados Unidos"*
- *"Usa esta dirección y datos exactamente como aparecen aquí en todas tus compras online."*
- *"¿No encuentras un paquete? Seguro no lo has agregado a la APP para hacerle seguimiento."*
- *"Hazle seguimiento a tus compras"*
- *"Consigue hasta 900 puntos"*
- *"Abrir mi casillero gratis"* (CTA principal web)
- *"Trae a Colombia los productos que quieras desde donde quieras."*

### Números y moneda

- Miles con punto: `1.678 puntos`
- Moneda: `$8.99 USD`
- Porcentajes: `40%` (sin espacio)

---

## 14. Diferencias por producto (resumen)

| | App + Dashboard | Web pública |
|--|----------------|-------------|
| Tipografía | Plus Jakarta Sans only | Exo + Jakarta |
| Error | `#F32735` | `#CC1111` |
| Cards radius | 10px | 24px |
| Botones radius | 8px | 900px |
| Canvas | 430×932 / 1286px | 1512px |
| Primario | Cyan `#029ECB` | Cyan `#029ECB` |
| Gradiente | `45deg, cyan→lime` | `90deg, lime→cyan` |

---

## 15. Checklist para cualquier nueva pieza

- [ ] ¿El fondo base es blanco o neutro claro?
- [ ] ¿El gradiente se usa con moderación (no como fondo de secciones de texto extenso)?
- [ ] ¿Los textos principales están en `#333333` o `#004B72`?
- [ ] ¿Se usa Plus Jakarta Sans en el producto correcto?
- [ ] ¿Los botones primarios tienen el gradiente o el fill correcto según el contexto?
- [ ] ¿El copy está en español latinoamericano, en tuteo?
- [ ] ¿Los números usan punto como separador de miles?
- [ ] ¿Se exploró primero una solución con fotografía real antes de recurrir a ilustración?
- [ ] ¿La foto viene de una biblioteca libre (Pexels, Unsplash o Pixabay)?
- [ ] ¿La foto va a sangre completa (full bleed, sin márgenes ni marcos)?
- [ ] ¿Las fotos siguen la dirección de luz natural y diversidad latina?
- [ ] ¿Los iconos son Lucide con stroke 1.8px?
- [ ] ¿Los radios de cards y botones corresponden al producto (app vs web)?
- [ ] ¿Los emojis están anclados a una palabra clave o badge (no sueltos, no dos seguidos)?
