# mortgage-tools2

A single-page, dependency-free calculator that compares three Quebec home-purchase
scenarios side by side: cash needed at closing, monthly outlay, and unrecoverable
cost (interest, welcome tax, property/school tax, CMHC premium, QST, closing fees)
over a horizon you choose.

Everything lives in [`index.html`](index.html) — no build step, no framework, no
external JavaScript. The charts are hand-drawn SVG. The only network request is a
Google Fonts stylesheet; the page falls back to system fonts if it's blocked.

## Publishing with GitHub Pages

1. Go to **Settings → Pages** in this repository.
2. Under **Build and deployment → Source**, choose **Deploy from a branch**.
3. Pick the branch you want to serve and the **`/ (root)`** folder, then **Save**.

The site appears at `https://<user>.github.io/mortgage-tools2/` within a minute or
two. `.nojekyll` is present so GitHub serves the files as-is instead of running
them through Jekyll.

## Local preview

Just open `index.html` in a browser, or:

```sh
python3 -m http.server 8000
```

then visit http://localhost:8000.

## Assumptions

The modelling assumptions (2026 welcome-tax brackets, CMHC premium rates, minimum
down payment rules, semi-annual compounding) are listed under **Assumptions and
sources** at the bottom of the page. This is a planning tool, not financial advice.
