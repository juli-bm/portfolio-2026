# Portfolio 2026 — Juliette Mouillac

Two versions of the same portfolio, sharing the same content:

- **`creative/`** — plain HTML/CSS/JS, illustrated flower design (deployed at the site root).
- **`dsfr/`** — Vue 3 + Vite rewrite of the [DSFR](https://www.systeme-de-design.gouv.fr/)-styled
  version (deployed at `/dsfr/`). See [dsfr/README.md](dsfr/README.md) for local dev setup.

Each version links to the other (top-right pill on the creative homepage, "Créative" button
in the DSFR header).

## Deployment

GitHub Pages is built via [`.github/workflows/deploy.yml`](.github/workflows/deploy.yml) on
every push to `main`:

1. `creative/` is copied as-is to the site root.
2. `dsfr/` is built with Vite and copied to `/dsfr/`.
3. The combined output is deployed via the GitHub Pages Actions artifact.

In the repo's **Settings → Pages**, set **Source** to **GitHub Actions** for this to work.
