Vas a construir una pieza HTML pixel-perfect siguiendo el sistema de diseño ZenderBox.

Lee `BRAND.md`, `photography.md` y `tokens.md` antes de empezar si aún no los has leído en esta sesión.

## Reglas de construcción

**Canvas y escala**
- Define el canvas exacto al formato pedido (ej. 1080×1080 para feed, 1080×1920 para story)
- El artboard va centrado en pantalla con fondo neutro (#F0F0F0) alrededor
- Auto-escala con JS para que quepa en cualquier viewport sin scroll:
  ```js
  function scale() {
    const s = Math.min(window.innerWidth / W, window.innerHeight / H) * 0.92;
    document.getElementById('artboard').style.transform = `scale(${s})`;
    document.getElementById('artboard').style.transformOrigin = 'top center';
  }
  window.addEventListener('resize', scale); scale();
  ```

**Fotografía**
- Siempre full bleed: `position: absolute; inset: 0; width: 100%; height: 100%; object-fit: cover`
- Overlay sobre foto (siempre tira a cyan profundo, nunca negro):
  ```css
  background: linear-gradient(to top,
    rgba(0,58,85,0.92) 0%,
    rgba(1,75,105,0.78) 25%,
    rgba(2,90,125,0.42) 52%,
    rgba(2,120,160,0.14) 75%,
    transparent 100%
  );
  ```

**Tipografía**
- App / producto: `@import url('https://fonts.googleapis.com/css2?family=Plus+Jakarta+Sans:wght@500;700;800&display=swap')`
- Web pública: suma Exo: `family=Exo:wght@400;700&family=Plus+Jakarta+Sans:wght@400;500;700`

**Logos (SVGs en la raíz del repo)**
- Fondo claro → `logo-hor-color.svg`
- Fondo oscuro o sobre foto → `logo-hor-blanco.svg`
- Standalone pequeño → `logo-fav-color.svg` o `logo-fav-blanco.svg`

**Color en texto**
- Palabras destacadas en titulares: `<span style="color:#029ECB">cyan</span>` y `<span style="color:#CCD32A">lime</span>`
- **Nunca** `background: linear-gradient(...); -webkit-background-clip: text`

**Guardado y descarga automática**
- Guarda el archivo HTML en el escritorio del usuario (`~/Desktop/`) con nombre descriptivo
- Una vez guardado, **descarga automáticamente el archivo al ordenador** disparando un link de descarga desde el propio HTML:
  ```js
  // Al cargar la página, dispara descarga automática del archivo en el formato pedido
  window.addEventListener('load', () => {
    const a = document.createElement('a');
    a.href = window.location.href;
    a.download = 'nombre-de-la-pieza.html'; // ajusta el nombre según la pieza
    a.click();
  });
  ```
- Si el formato pedido era imagen (PNG/JPG), usa `html2canvas` o indica al usuario que puede hacer captura desde el preview con el navegador. Si el flujo permite exportar PNG directamente, usa Canvas API para generar el blob y descargarlo:
  ```js
  // Exportar como PNG con html2canvas (CDN bloqueado en Artifacts — usar en servidor local)
  html2canvas(document.getElementById('artboard')).then(canvas => {
    const a = document.createElement('a');
    a.download = 'nombre-pieza.png';
    a.href = canvas.toDataURL('image/png');
    a.click();
  });
  ```
- La descarga debe ocurrir **sin que el usuario tenga que hacer nada** — automática al abrir el archivo

## Al terminar

Muestra el preview y confirma:
- Logo correcto para el fondo
- Foto full bleed (si hay)
- Overlay en cyan profundo (si hay foto)
- Palabras de color en sólido (no gradiente en texto)
- Copy en español colombiano, sin em-dashes
