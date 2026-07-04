<div align="center">

# Merka

**Dress measurements on paper, without the paper.**

[![Live demo](https://img.shields.io/badge/demo-GitHub%20Pages-2e2420?style=flat-square)](https://krwg.github.io/merka/)
[![License](https://img.shields.io/badge/license-MIT-af52de?style=flat-square)](LICENSE)
[![Stack](https://img.shields.io/badge/stack-vanilla%20HTML%20%2B%20SVG-8a7a70?style=flat-square)](docs/index.html)
[![Privacy](https://img.shields.io/badge/data-local%20only-green?style=flat-square)](#privacy)

</div>

---

Merka is a **small browser tool** for home dressmaking: you type body measurements after a fitting, and Merka draws them on a **clear dress sketch** — ready to **print** or **save as PNG**.

It was built for a real workflow: my mom sews as a hobby. For years she wrote every measurement by hand on paper sketches after each fitting — easy to lose, hard to redraw, awkward to store. Merka keeps the same ritual (measure → sketch → keep), but the numbers live in a neat diagram you can file, print, or share.

**No account. No cloud. No install.** Open the page, enter values, done.

**[→ Open Merka](https://krwg.github.io/merka/)**

---

## Why Merka

| Before | With Merka |
|--------|------------|
| Hand-drawn lines and numbers on loose paper | Typed measurements on a consistent half-pattern sketch |
| Redrawing after every fitting | Update fields; lines appear only where you have values |
| Faded notes in a folder | **Print** or **Save as PNG** for a clean copy |
| — | Values remembered in **your browser** (`localStorage`) for the next session |

The UI is in **Russian** (standard dressmaking abbreviations: ОГ, ОТ, ОБ, etc.) — the audience is the sewing table, not a dev README.

---

## Features

- **12 measurement fields** — bust, waist, hips, neck, shoulder width, sleeve length, front/back length to waist, garment length, armhole, wrist, and more
- **Live sketch** — SVG half-pattern; dimension lines show only for filled fields
- **Apply / Clear** — explicit apply button plus debounced auto-update while typing
- **Print** — print stylesheet hides the editor; sketch only on paper
- **Export PNG** — high-resolution image from the sketch (canvas export)
- **Offline-friendly** — single static page; works without a backend after first load (fonts load from Google Fonts when online)

---

## Quick start

**Use online:** [https://krwg.github.io/merka/](https://krwg.github.io/merka/)

**Run locally:**

```bash
git clone https://github.com/krwg/merka.git
cd merka
# any static server, e.g.:
npx --yes serve docs
# open http://localhost:3000
```

Or open `docs/index.html` directly in a browser (PNG export may vary by browser security rules).

---

## How it works

1. Enter measurements in centimeters (placeholders suggest typical values).
2. Click **Применить** or wait a moment — labels appear on the sketch (`96 см`, etc.).
3. **Распечатать** for a paper copy at the machine, or **Сохранить как PNG** for a digital file.

Data is stored under the key `dressMeasurementsV2` in **localStorage** on your device only.

---

## Privacy

Merka does not send your measurements anywhere. There is no analytics, no login, and no server-side storage. Clear site data in the browser to reset saved values.

---

## Project layout

```
merka/
├── docs/
│   └── index.html    # entire app (HTML + CSS + SVG + JS)
├── LICENSE           # MIT
└── README.md
```

---

## License

**MIT** — see [LICENSE](LICENSE).

---

<div align="center">

Built with care by [krwg](https://github.com/krwg) · for the sewing table, not the cloud

</div>
