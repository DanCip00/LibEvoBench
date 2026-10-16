# LibEvoBench project page

Website for **LibEvoBench: Probing Temporal Knowledge Stratification in Code Generation Models** (NeurIPS 2026, Evaluations & Datasets Track).

## Structure

```
index.html                      the page
static/css/bulma.min.css        Bulma 0.9.4 (vendored)
static/css/index.css            page styles
static/js/leaderboard.js        renders the leaderboard table
static/data/leaderboard.json    leaderboard numbers (edit this to add a model)
static/images/                  figures from the paper
.nojekyll                       serve files as-is on GitHub Pages
```

## Run locally

```
python3 -m http.server 8000
```

Then open http://localhost:8000. Opening `index.html` directly from disk won't load the leaderboard, because browsers block `fetch` on `file://`.

## Deploy on GitHub Pages

Push to the repository, then go to Settings > Pages and choose "Deploy from a branch", branch `main`, folder `/ (root)`.

## Updating the leaderboard

Add an entry to `models` in `static/data/leaderboard.json` with the same fields as the existing ones. Ranks are computed in the browser.

## Credits

Layout adapted from the [Nerfies](https://github.com/nerfies/nerfies.github.io) project page template (CC BY-SA 4.0).
