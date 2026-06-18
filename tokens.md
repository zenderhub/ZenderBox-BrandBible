# ZenderBox — Design Tokens

Referencia completa de tokens CSS y valores de diseño para implementación en código.

## CSS Custom Properties

```css
:root {
  /* ── COLORES DE MARCA ── */
  --zb-cyan:        #029ECB;
  --zb-lime:        #CCD32A;
  --zb-navy:        #004B72;
  --zb-dark-cyan:   #007B9F;

  /* ── GRADIENTES ── */
  --zb-grad:        linear-gradient(45deg,  #029ECB 0%, #CCD32A 85%); /* app/dashboard */
  --zb-grad-web:    linear-gradient(90deg,  #CCD32A 0%, #029ECB 85%); /* web pública */
  --zb-grad-hero:   linear-gradient(135deg, #CCD32A 0%, #029ECB 100%); /* hero sections */

  /* ── NEUTROS ── */
  --zb-ink:         #1F1F1F;
  --zb-ink-body:    #333333;
  --zb-ink-soft:    #666666;
  --zb-ink-mid:     #8A8A8A;
  --zb-placeholder: #B8B8B8;
  --zb-divider:     #DBDBDB;
  --zb-surface:     #F6F6F6;
  --zb-white:       #FFFFFF;

  /* ── SEMÁNTICOS UI ── */
  --zb-error-app:   #F32735;
  --zb-error-web:   #CC1111;
  --zb-success:     #008C31;
  --zb-warning:     #E66B00;

  /* ── ESTADOS DE PAQUETE ── */
  --state-tienda-text:    #0260CB;
  --state-tienda-bg:      #E8F0FB;
  --state-bodega-text:    #008C31;
  --state-bodega-bg:      #F1F6F5;
  --state-despachado-text:#E66B00;
  --state-despachado-bg:  #FDF3EA;
  --state-camino-text:    #F32735;
  --state-camino-bg:      #F4E8E9;
  --state-entregado-text: #FF28E2;
  --state-entregado-bg:   #FDE8FB;

  /* ── TIPOGRAFÍA ── */
  --font-head: 'Plus Jakarta Sans', sans-serif;  /* app/dashboard */
  --font-web-head: 'Exo', sans-serif;            /* web pública titulares */
  --font-body: 'Plus Jakarta Sans', sans-serif;

  /* ── ESPACIADO ── */
  --sp-xxxs: 2px;
  --sp-xxs:  4px;
  --sp-xs:   8px;
  --sp-sm:   10px;
  --sp-m:    12px;
  --sp-md:   16px;
  --sp-xl:   20px;
  --sp-xxl:  32px;
  --sp-margin: 16px;

  /* ── GAP ── */
  --gap-xxs: 4px;
  --gap-xs:  8px;
  --gap-sm:  12px;
  --gap-md:  16px;
  --gap-lg:  24px;
  --gap-xl:  48px;

  /* ── RADIOS ── */
  --radius-full: 99px;
  --radius-md:   10px;   /* cards app/dashboard */
  --radius-sm:   8px;    /* botones app, inputs */
  --radius-web-card: 24px; /* cards web pública */
  --radius-web-btn:  900px; /* botones web pública */

  /* ── BORDES ── */
  --border-md: 1px;
  --border-lg: 2px;
  --border-xs: 0.33px;

  /* ── SOMBRAS ── */
  --shadow-card: none; /* por convención, cards sin sombra */
  --shadow-modal: 0 24px 64px rgba(0,0,0,0.18);
  --shadow-chip:  0 8px 24px rgba(0,0,0,0.12);
  --shadow-cta:   0 4px 20px rgba(2,158,203,0.3);
}
```

## Escala tipográfica — App/Dashboard (Plus Jakarta Sans)

```css
.zb-display-l  { font-size: 32px; line-height: 38px; font-weight: 700; }
.zb-display    { font-size: 24px; line-height: 32px; font-weight: 700; }
.zb-section    { font-size: 19px; line-height: 24px; font-weight: 700; }
.zb-title      { font-size: 16px; line-height: 20px; font-weight: 700; }
.zb-title-sm   { font-size: 14px; line-height: 18px; font-weight: 800; }
.zb-button     { font-size: 16px; line-height: 20px; font-weight: 800; }
.zb-body       { font-size: 14px; line-height: 18px; font-weight: 500; }
.zb-placeholder{ font-size: 13px; line-height: 16px; font-weight: 500; }
.zb-id         { font-size: 13px; line-height: 16px; font-weight: 700; }
.zb-navbar     { font-size: 12px; line-height: 15px; font-weight: 500; }
.zb-navbar-on  { font-size: 12px; line-height: 15px; font-weight: 700; }
.zb-label      { font-size: 12px; line-height: 15px; font-weight: 700; }
.zb-caption    { font-size: 10px; line-height: 13px; font-weight: 500; }
.zb-tag        { font-size: 10px; line-height: 13px; font-weight: 500; }
```

## Botones — App/Dashboard

```css
/* Primary */
.btn-primary {
  background: linear-gradient(45deg, #029ECB 0%, #CCD32A 85%);
  color: #ffffff;
  height: 52px;
  border-radius: 8px;
  font-size: 16px;
  font-weight: 800;
  padding: 0 24px;
  border: none;
}

/* Secondary */
.btn-secondary {
  background: #029ECB;
  color: #ffffff;
  height: 52px;
  border-radius: 8px;
}

/* Stroke */
.btn-stroke {
  background: #F6F6F6;
  color: #007B9F;
  border: 1px solid #007B9F;
  height: 52px;
  border-radius: 8px;
}

/* Hover/Press states */
.btn:hover  { filter: brightness(1.05); }
.btn:active { transform: scale(0.98); filter: brightness(0.95); }
/* Transition: 150ms ease */
```

## Botones — Web pública

```css
/* Primary */
.btn-web-primary {
  background: linear-gradient(90deg, #CCD32A 0%, #029ECB 85%);
  color: #ffffff;
  border-radius: 900px;
  font-family: 'Exo', sans-serif;
  font-weight: 700;
  font-size: 18px;
  text-transform: uppercase;
  padding: 18px 40px;
  border: none;
}

/* Secondary */
.btn-web-secondary {
  background: #029ECB;
  color: #ffffff;
  border-radius: 900px;
}

/* Tertiary */
.btn-web-tertiary {
  background: transparent;
  color: #004B72;
  border: 2px solid #004B72;
  border-radius: 900px;
}
```

## Inputs

```css
.input {
  border: 1px solid #B8B8B8;
  border-radius: 8px;
  font-size: 14px;
  font-weight: 500;
  color: #333333;
  background: #FFFFFF;
  height: 48px;
  padding: 0 16px;
}
.input:focus   { border-color: #029ECB; outline: none; }
.input.error   { border-color: #F32735; }
.input:disabled { background: #F6F6F6; color: #8A8A8A; }
```

## State Badges (estados de paquete)

```css
.badge-tienda    { color: #0260CB; background: #E8F0FB; border: 1px solid #0260CB33; }
.badge-bodega    { color: #008C31; background: #F1F6F5; border: 1px solid #008C3133; }
.badge-despachado{ color: #E66B00; background: #FDF3EA; border: 1px solid #E66B0033; }
.badge-camino    { color: #F32735; background: #F4E8E9; border: 1px solid #F3273533; }
.badge-entregado { color: #FF28E2; background: #FDE8FB; border: 1px solid #FF28E233; }

/* Shared */
.state-badge {
  border-radius: 99px;
  font-size: 10px;
  font-weight: 700;
  letter-spacing: 0.06em;
  text-transform: uppercase;
  padding: 3px 10px;
  white-space: nowrap;
}
```
