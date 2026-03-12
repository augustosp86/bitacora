# ✈️ Bitacora

**Planificá itinerarios, controlá gastos y consultá el clima. Sin cuentas, sin servidores, sin drama.**

Bitacora es una app web mobile-first de planificación de viajes. Un solo archivo HTML, sin frameworks, sin backend. Tus datos viven en tu dispositivo.

---

## ¿Qué hace?

- 📅 **Itinerario por día** — Timeline visual agrupado por ciudad, con vuelos, hoteles y actividades
- 📍 **Mapa de lugares** — Hoteles y actividades con links directos a Google Maps
- 💸 **Presupuesto real** — Gastos por categoría, barra de progreso, gráfico de torta y barras
- 🌤️ **Clima integrado** — Pronóstico para cada destino vía Open-Meteo
- 🔗 **Compartir viaje** — Genera un link comprimido con todo el itinerario
- 💾 **Backup JSON** — Export e import de todos los viajes
- 📄 **Export PDF / HTML** — Itinerario completo para imprimir o guardar
- 🌐 **Bilingüe** — Toggle ES / EN

---

## Estructura del repo

```
/
├── index.html      ← Landing page
├── app.html        ← La app Bitacora completa
└── README.md
```

---

## Deploy en Vercel

1. Subí el repo a GitHub
2. Entrá a [vercel.com](https://vercel.com) → **Add New Project** → importá tu repo
3. Vercel detecta `index.html` automáticamente como raíz → **Deploy**

Tu app queda en:
- `https://tu-app.vercel.app/` → landing
- `https://tu-app.vercel.app/app.html` → la app

**Último paso:** reemplazá en `index.html` las dos líneas:
```js
const APP_URL = 'https://tu-app.vercel.app/app.html';
const DL_URL  = 'https://tu-app.vercel.app/app.html';
```

---

## Deploy en GitHub Pages

1. Subí el repo a GitHub
2. Entrá a **Settings → Pages**
3. Source: **Deploy from a branch** → `main` → `/ (root)` → **Save**

Tu app queda en:
- `https://tu-usuario.github.io/tu-repo/` → landing
- `https://tu-usuario.github.io/tu-repo/app.html` → la app

---

## Datos y privacidad

- Todo se guarda en `localStorage` del navegador
- No hay servidor, no hay base de datos, no hay tracking
- Export/import JSON para backup y migración entre dispositivos
- Versionado interno: la app migra datos automáticamente entre versiones

---

## Stack

- HTML + CSS + Vanilla JS
- Sin frameworks, sin dependencias npm
- Fuentes: [Fraunces](https://fonts.google.com/specimen/Fraunces) + [Geist](https://vercel.com/font)
- Clima: [Open-Meteo API](https://open-meteo.com/) (gratis, sin API key)
- Geocoding: [Open-Meteo Geocoding](https://open-meteo.com/en/docs/geocoding-api)

---

## Licencia

MIT — hacé lo que quieras.
