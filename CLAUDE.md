# ZenderBox Brand Bible — Claude Code

## Lee esto primero, siempre

Este repositorio es el Brand Bible oficial de ZenderBox. Cualquier pieza de comunicación que se cree desde aquí debe cumplir el sistema de identidad completo.

Antes de cualquier tarea de diseño o copy, lee:

- `BRAND.md` — sistema completo de identidad: colores, tipografía, componentes, voz
- `photography.md` — reglas de fotografía, tratamiento de imagen y overlays
- `voice.md` — voz, tono y copy verbatim
- `tokens.md` — tokens de color, tipografía y espaciado

---

## Flujo obligatorio para crear cualquier pieza

Cuando alguien pida crear un post, brochure, banner, story, flyer, email o cualquier pieza de comunicación, **haz estas preguntas de una en una** antes de escribir código o copy. Espera la respuesta antes de pasar a la siguiente. Da contexto en cada pregunta para que el equipo entienda por qué importa.

### Pregunta 1 — Tipo y canal
¿Qué tipo de pieza vamos a crear y para qué canal?

Opciones comunes:
- Post feed Instagram (1080×1080 · 1:1)
- Story / Reels cover (1080×1920 · 9:16)
- Carrusel Instagram (múltiples slides 1:1)
- Brochure / flyer (A4 vertical, carta, etc.)
- Banner web (leaderboard, hero, email header)
- Presentación / deck (16:9)
- Otro — que lo describan

El formato define el canvas, la jerarquía visual y cómo se comporta el texto.

### Pregunta 2 — Objetivo
¿Qué tiene que lograr esta pieza? ¿Venta de un servicio, awareness de marca, instrucción de uso, apoyo a una campaña, promoción puntual, apoyo a una comunidad? ¿Hay un CTA específico que deba aparecer?

### Pregunta 3 — Fotografía
¿La pieza necesita fotografía?

- Si **sí**: ¿tienen la foto o quieren que la busque en Pexels, Unsplash o Pixabay?
- Si **busco yo**: ¿qué debe transmitir la foto? Pide una descripción del mood (emoción, contexto, tipo de persona si hay, lugar, producto si aplica) y cualquier restricción de composición (espacio para texto, orientación, etc.).
- Si **tienen la foto**: que compartan la URL o el archivo.

### Pregunta 4 — Copy
¿Hay texto ya definido o hay que construirlo?

- Si **hay copy**: que lo compartan tal cual, aunque sea borrador.
- Si **hay que construirlo**: ¿cuál es el mensaje principal? ¿Qué información no puede faltar? ¿Hay alguna frase o CTA que deba aparecer exacto?

### Pregunta 5 — Artboards
¿Cuántas versiones o formatos se necesitan? Por ejemplo: feed + story, versión A/B con dos headlines, español + inglés, varios tamaños del mismo diseño.

### Pregunta 6 — Audiencia y país
¿El copy va dirigido a un país específico o debe ser genérico para toda Latinoamérica?

- Si **país específico**: nombrarlo en el copy cuando tenga sentido (ej. "en Colombia", "desde Venezuela"). El tono, los referentes culturales y los ejemplos deben resonar con esa audiencia.
- Si **sin país**: usar referentes neutros latinoamericanos. Nunca mencionar un país concreto. Frases como "en tu país", "donde estés" o "en toda Latinoamérica" si aplica.

Esto define si el copy puede usar gentilicios, referencias locales o debe mantenerse regional.

### Pregunta 7 — Contexto adicional
¿Hay algún elemento específico que deba aparecer: oferta, fecha, nombre de producto, persona, código de descuento? ¿Hay una pieza anterior o referencia visual de la que partir?

---

## Datos de contacto reales — siempre verificar

Antes de incluir cualquier dato de contacto en una pieza, verifica en **www.zenderbox.com** que sea el dato real. Nunca uses placeholders, números inventados ni emails de ejemplo.

Datos vigentes confirmados (verificar si cambian):
- WhatsApp: **+1 786-442-3800**
- Web: **www.zenderbox.com**
- Instagram: **@zenderbox.col**
- Facebook: **facebook.com/zenderbox.col**
- TikTok: **@zenderbox**

---

## Iconos en piezas de comunicación — emojis, no Lucide

En piezas de comunicación (posts, brochures, stories, banners, emails): usa **emojis** para los iconos de contenido, no Lucide ni ninguna librería SVG externa.

Lucide (`unpkg.com/lucide`) es solo para la **UI del producto** (app móvil, dashboard). En una pieza impresa o de redes sociales no hay interactividad, los SVG de Lucide pueden no renderizar, y los emojis son más directos y legibles.

| En lugar de | Usa |
|---|---|
| `<i data-lucide="globe">` | 🌐 |
| `<i data-lucide="package">` | 📦 |
| `<i data-lucide="smartphone">` | 📱 |
| `<i data-lucide="trending-up">` | 📈 |
| `<i data-lucide="mail">` | 📧 |
| `<i data-lucide="message-circle">` | 💬 |
| `<i data-lucide="map-pin">` | 📍 |

---

## Reglas siempre activas — sin excepción

- Español colombiano, tuteo siempre (tu, tus, tienes, hazle). Nunca usted.
- **País en el copy**: si la pieza va dirigida a un país específico, úsalo en el copy con naturalidad (gentilicios, referencias locales). Si va sin país definido, usa referentes neutros latinoamericanos y nunca menciones un país concreto.
- **Sin em-dashes (—). Nunca.** Reemplaza con coma, punto, dos puntos o rearma la frase.
- **Titulares de piezas de comunicación: siempre en MAYÚSCULAS** (`text-transform: uppercase`). Sin excepción en posts, stories, brochures, banners y flyers.
- **Emoji obligatorio en el titular**: toda pieza de comunicación debe tener al menos 1 emoji anclado al inicio o dentro del titular principal, en contexto con el tema. Nunca emoji decorativo suelto fuera del titular. Nunca dos emojis seguidos sin texto entre ellos.
- Palabras de color en titulares: sólido siempre. Una en cyan `#029ECB`, otra en lime `#CCD32A`. **Nunca gradiente CSS en texto** (`-webkit-background-clip: text` está prohibido).
- **Overlay sobre foto: siempre cyan claro de marca**, nunca navy ni negro puro. CSS obligatorio:
  ```css
  background: linear-gradient(to top,
    rgba(2,158,203,0.88) 0%,
    rgba(2,158,203,0.62) 30%,
    rgba(2,158,203,0.28) 58%,
    rgba(2,158,203,0.08) 78%,
    transparent 100%
  );
  ```
- **Sin raya divisora** entre titular y párrafo de cuerpo. No usar `<hr>`, ni bordes, ni líneas decorativas entre esos dos elementos.
- Fotos a sangre completa (full bleed): `object-fit: cover; width: 100%; height: 100%`. Sin márgenes de foto, sin marcos.
- **Logos**: color (`logo-hor-color.svg`) sobre fondos claros; blanco (`logo-hor-blanco.svg`) sobre fondos oscuros y sobre foto. **Tamaño mínimo**: `width: clamp(110px, 22%, 148px)` en canvas 1080px. Proporciones bloqueadas, nunca distorsionar. Margen de respiro mínimo 18px respecto a cualquier borde.
- **Tipografía en piezas de comunicación**:
  - Titular: `font-size: clamp(44px, 9.5%, 80px)`, `font-weight: 800`, `line-height: 1.05`. **Nunca ponerle `max-width` al titular**: ocupa el ancho completo del área de contenido (de margen a margen). Si el texto es corto, que se vea grande. Si es largo, que fluya en varias líneas ocupando todo el ancho.
  - Cuerpo: `font-size: clamp(15px, 3.2%, 22px)`, `font-weight: 400`, `line-height: 1.55`.
  - El cuerpo sí puede tener `max-width` para legibilidad (máximo 85% del área de contenido).
- Fotos: solo de Pexels, Unsplash o Pixabay. Nunca sin licencia clara.

---

## Skills disponibles

Usa estos slash commands para tareas específicas:

- `/crear-pieza` — inicia el flujo guiado de preguntas para crear cualquier pieza de comunicación desde cero
- `/humanizer` — revisa y humaniza copy siguiendo la voz ZenderBox
- `/frontend-design` — crea piezas HTML pixel-perfect siguiendo el sistema de diseño

---

## Descarga automática — siempre

Cuando una pieza quede lista, **descárgala automáticamente** al ordenador del usuario en el formato que se pidió al inicio, sin que tenga que hacer nada:

- **HTML**: guarda en `~/Desktop/` con nombre descriptivo y dispara un `<a download>` al cargar la página.
- **PNG / JPG**: usa `html2canvas` sobre el artboard para generar el blob y descargarlo con `canvas.toDataURL()`. Si el entorno no permite CDN externo, genera el archivo desde el servidor local e indica la ruta exacta donde quedó guardado.
- El nombre del archivo debe ser descriptivo: `zenderbox-[tipo]-[breve-descripcion].ext` (ej. `zenderbox-post-venezuela.html`, `zenderbox-story-black-friday.png`).
- Nunca termines una pieza sin confirmar que el archivo ya está en el ordenador del usuario.

---

## Notas técnicas para construcción HTML

- Canvas exacto al formato pedido (ej. 1080×1080 px para feed Instagram)
- Auto-escala con JS para que quepa en cualquier viewport:
  ```js
  const s = Math.min(window.innerWidth / W, window.innerHeight / H);
  document.getElementById('artboard').style.transform = `scale(${s})`;
  ```
- Tipografía: importa **Plus Jakarta Sans** para app/producto; **Exo + Plus Jakarta Sans** para web pública
- SVGs de logo disponibles en la raíz del repo: `logo-hor-color.svg`, `logo-hor-blanco.svg`, `logo-fav-color.svg`, `logo-fav-blanco.svg`
