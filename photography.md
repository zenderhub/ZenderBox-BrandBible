# ZenderBox — Fotografía, Video e Ilustración

## El territorio visual de ZenderBox

ZenderBox existe en el espacio emocional entre el **deseo** y la **llegada**. Cada imagen debe habitar ese territorio: lo que el usuario quiere, el momento de espera activa, y la satisfacción de recibir.

---

## Los 4 territorios fotográficos

### 1. El Deseo
El usuario descubriendo, eligiendo, comprando.
- Personas navegando en teléfono o laptop
- Pantallas de tiendas online sin marcas obvias
- Momentos de decisión: comparar productos, agregar al carrito
- **Emoción**: curiosidad, anticipación

### 2. La Espera Activa
El seguimiento, la comunicación, el control.
- Persona revisando el tracking en la app
- Notificación en el teléfono
- Chat con soporte
- **Emoción**: tranquilidad, confianza, control

### 3. La Llegada
El momento de recibir el paquete.
- Unboxing — manos abriendo caja, no cara exagerada
- Primer vistazo al producto
- Integración del producto a la vida: persona usando lo que compró
- **Emoción**: satisfacción genuina, no euforia actuada

### 4. El Emprendedor
El usuario que usa ZenderBox para su negocio.
- Persona con productos organizados, inventario pequeño
- Espacio de trabajo real — no oficina corporativa
- Celular o laptop como herramienta de trabajo
- **Emoción**: empoderamiento, profesionalismo accesible

---

## Dirección técnica

### Luz
- Natural, amplia — ventanas, luz de día
- Sin flash artificial frontal
- Sombras suaves, no duras
- Temperatura: cálida-neutra (no fría/azul, no naranja exagerado)

### Composición
- Mix de: close-ups de manos/productos + medios con contexto humano
- Fondo neutro o contextual — no fondos blancos de estudio para emocionales
- Espacio de respiro — no todo lleno de elementos
- Punto de vista del usuario, no del fotógrafo de moda

### Personas
- Latinoamericanas, diversas — Colombia, México, Perú, etc.
- Edad 18–45, mix equitativo
- Ropa casual-cotidiana, no modelos de catálogo
- Expresiones reales — no la sonrisa forzada de stock

### Post-producción
- Color grading sutil — no filtros Instagram
- Contraste natural
- Sin vignettes pesados
- Sin texturas de película (no es una marca vintage)

---

## Lo que NO hacer en fotografía

| Evitar | Por qué |
|--------|---------|
| Aviones, barcos, camiones | Cliché de logística — ZenderBox es personal, no industrial |
| Cajas de cartón sin contexto humano | Comunica bodega, no experiencia de usuario |
| Personas posando con paquetes mirando a cámara | Actuado, no creíble |
| Saturación artificial de colores | Rompe con el mood honesto de la marca |
| Solo hombres o solo mujeres | La marca es para todos |
| Fondos blancos de estudio para escenas emocionales | Frío, sin vida |
| Ropa de marca visible competidora | Conflicto de imagen |

---

## Overlays y tratamiento sobre foto

### Texto sobre foto oscura
```css
background: linear-gradient(to top, rgba(0,0,0,0.75) 0%, transparent 55%);
```

### Glassmorphism sobre foto
```css
background: rgba(255,255,255,0.1);
backdrop-filter: blur(16px);
-webkit-backdrop-filter: blur(16px);
border: 1px solid rgba(255,255,255,0.2);
```

### Glassmorphism oscuro (sobre foto en sección oscura)
```css
background: rgba(0,20,40,0.65);
backdrop-filter: blur(16px);
border: 1px solid rgba(255,255,255,0.15);
```

---

## Ilustraciones isométricas 3D

### Cuándo usar
- Cards "cómo funciona" (pasos del proceso)
- Pantallas de onboarding
- Estados vacíos que necesiten personalidad
- Material de marketing digital

### Estilo
- Cubos/formas isométricas planas, sin render fotorrealista
- Formas geométricas simples — sin detalles excesivos
- Paleta estrictamente de marca

### Paleta isométrica
| Cara | Color | Hex |
|------|-------|-----|
| Superior | Lime | `#CCD32A` |
| Derecha | Cyan | `#029ECB` |
| Izquierda | Dark cyan | `#007B9F` |

### Animación
```css
@keyframes float {
  0%, 100% { transform: translateY(0); }
  50%       { transform: translateY(-6px); }
}
.iso { animation: float 4s ease-in-out infinite; }
```
Desfasar elementos con `animation-delay` para que no se muevan en sincronía.

---

## Video

### Formato y ratio
- Vertical 9:16 para redes/app
- Horizontal 16:9 para web y presentaciones
- Square 1:1 para feed de Instagram

### Duración
- Story/Reel: 6–15 segundos
- Explainer: 30–60 segundos máximo
- Demo de producto: hasta 90 segundos

### Estilo
- Mismo criterio que fotografía: luz natural, personas reales, cotidiano
- Ritmo: ni muy lento (aburrido) ni muy rápido (ansioso)
- Música: instrumental contemporánea — no trap genérico, no versiones de canciones populares
- Sin voz en off corporativa — si hay narración, persona real o texto directo

### Motion para UI/Marketing digital
```
Easing: ease-out (cubic-bezier 0.0, 0.0, 0.2, 1)
Entrada: fade + slide up 4–8px
Duración: 200–300ms
Hover: solo color/opacidad, no scale en elementos de UI grandes
```
