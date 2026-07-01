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

### Pregunta 6 — Contexto adicional
¿Hay algún elemento específico que deba aparecer: oferta, fecha, nombre de producto, persona, código de descuento? ¿Hay una pieza anterior o referencia visual de la que partir?

---

## Reglas siempre activas — sin excepción

- Español colombiano, tuteo siempre (tu, tus, tienes, hazle). Nunca usted.
- **Sin em-dashes (—). Nunca.** Reemplaza con coma, punto, dos puntos o rearma la frase.
- Sin emoji sueltos — solo anclados a una palabra clave, badge o ítem de navegación. Nunca dos seguidos.
- Palabras de color en titulares: sólido siempre. Una en cyan `#029ECB`, otra en lime `#CCD32A`. **Nunca gradiente CSS en texto** (`-webkit-background-clip: text` está prohibido).
- Overlay sobre foto: siempre tira a cyan profundo (`rgba(0,58,85,0.92)` en la base), nunca negro puro.
- Fotos a sangre completa (full bleed): `object-fit: cover; width: 100%; height: 100%`. Sin márgenes de foto, sin marcos.
- Logos: color (`logo-hor-color.svg`) sobre fondos claros; blanco (`logo-hor-blanco.svg`) sobre fondos oscuros y sobre foto.
- Fotos: solo de Pexels, Unsplash o Pixabay. Nunca sin licencia clara.

---

## Skills disponibles

Usa estos slash commands para tareas específicas:

- `/crear-pieza` — inicia el flujo guiado de preguntas para crear cualquier pieza de comunicación desde cero
- `/humanizer` — revisa y humaniza copy siguiendo la voz ZenderBox
- `/frontend-design` — crea piezas HTML pixel-perfect siguiendo el sistema de diseño

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
