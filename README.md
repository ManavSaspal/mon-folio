# mon-folio

Portfolio site for **Saathvika**, product designer.

A single self-contained HTML file — no build step, no dependencies, no install.
Open `index.html` in a browser, or serve the folder.

```
index.html      the whole site (HTML + CSS + JS inline)
assets/         the four images it uses
```

## Status

⚠️ **Work in progress. Most of the content is placeholder.**

Real: her name, role, current employer and the brand names in the hero strip.

Placeholder — replace before this goes anywhere public:

- All four project titles and their links (every card points at `#`)
- The four testimonials in "Notes from nice people", including the names
  and roles attributed to them — these people are invented
- The companies in "Places that let me solve things" other than Guardian
- The Medium article titles, the `1:47` video runtime, and `hello@saathvika.me`
- Brand logos: the hero chips and the Guardian folder currently show brand
  names as text. Each chip has a drop-in slot —
  `<span class="bw"><img src="assets/logos/<brand>.svg" alt="<Brand>"></span>`

## Before publishing

- `#summary`, `#contact` and the `resume` nav link resolve to nothing — the
  page has no `id` attributes yet
- A temporary background switcher is still in: clicking the artwork cycles
  three backdrops and shows a readout pill. It's marked `TEMP` in the source
  and should be stripped before launch

## Notes for anyone editing this

- **Nothing scrolls except one element.** `body` is `overflow:hidden`; only
  `.sheet` scrolls. Wheel and touch events outside it are forwarded in.
- **The punch holes are a real mask** on `.page`, so a `box-shadow` there
  would be clipped — the paper's shadow is a separate `.page-shadow` layer.
- **Blur is per-artwork, not global.** `meadow-soft.jpg` ships pre-blurred.
- Verify structural changes by querying the DOM, not by looking at a
  screenshot. Several bugs in this file were invisible in screenshots.
