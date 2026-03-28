# Showcase media (`assets/showcase/`)

Public-safe images for the repository README and profile links.

## Files

| File | Role |
|------|------|
| `mvp-screenshot-01.png` … `mvp-screenshot-03.png` | MVP build screenshots (align with Git tag **`mvp-0.1`** or update captions when you refresh the vitrin). |
| `hero-mvp.svg` | Optional banner asset; root `README.md` does not embed it by default (add an image line if you want a hero later). |

## Guidelines

- Do not commit raw commercial source assets from the private repo—only crops and captures suitable for a public page.
- Prefer PNG or short GIF; keep file sizes reasonable for GitHub rendering.

## Wiring

Root [`README.md`](../../README.md) references `assets/showcase/mvp-screenshot-0*.png` and may reference `hero-mvp.svg`. If you rename files, update those paths.
