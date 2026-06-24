# Studio Ronin — landing page

The home/portfolio for **Studio Ronin** (`studioronin.app`) — a solo creative-software
studio building worldbuilding and map-making tools. *Worlds, assembled one panel at a time:
chance proposes the chaos, the maker authors the meaning.*

## What this is

A single self-contained **`index.html`** — vanilla HTML/CSS/JS, **no build step, no framework,
no bundler**. It introduces the studio and showcases its two live apps:

- **The Sortis Vellum** — a digital worldbuilding engine · <https://sortis-vellum.vercel.app>
- **Generations** — a panel map viewer · <https://generationsmap.studioronin.app>

The hero uses an ambient **Three.js** scene (a panel-map that assembles itself, then a
"generation" shimmer sweeps outward). It's loaded from CDN and **degrades gracefully**: if
Three.js or WebGL is unavailable, the page falls back to a static parchment vignette and stays
fully intact. `prefers-reduced-motion` is honored.

The aesthetic matches the apps: the "survivor's almanac" look — dark parchment-and-ink, with
ember/red, verdigris/green, and gold as the precious accents.

## Run locally

Any static server works, e.g.:

```sh
npx serve -l 4500 .
```

Then open <http://localhost:4500>.

## Deploy

Static site on **Vercel**. Point a project at this repo (no build command, output = repo root)
and assign the `studioronin.app` apex domain. Auto-deploys on `git push`.

## Placeholders to update

- Contact email (`hello@studioronin.app`)
- Maker bio / exact taglines (optional)
- A real logo, if/when there is one (currently an inline SVG compass seal)
