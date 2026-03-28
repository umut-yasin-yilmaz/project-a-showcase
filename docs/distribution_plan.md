# Distribution plan (Project A showcase)

This file is the **step-by-step** companion to the [Downloads & distribution](../README.md#downloads--distribution) section in the root README.

## Step 0 — Baseline (done when this file exists)

- Private dev repo: source of truth, regular push, milestone tags.
- Public showcase: README (EN + TR), screenshots, `docs/` (blueprint, QA, risk), boundaries documented.

## Step 1 — GitHub profile (you, browser)

- Pin **project-a-showcase** on your GitHub profile (up to 6 pins).
- Optionally set **bio** and **website** (showcase URL or future store link).

## Step 2 — First playtest / pre-demo Release (when you have a build)

1. Export a **Windows** (or chosen) build from Godot in the **private** repo.
2. Zip the export folder; **do not** `git add` large binaries to `main` history on showcase—use **Releases** only.
3. On GitHub: **project-a-showcase** → **Releases** → **Draft a new release**.
4. Tag example: `playtest-0.1` or `pre-demo-2026-03` (avoid clashing with private repo tags if that matters to you).
5. Title example: `Pre-demo playtest (not Steam demo)`.
6. Description: short notes + “**Pre-demo only**; final demo will be on Steam.”
7. Attach the zip as a release asset; **Publish**.

## Step 3 — After Steam demo goes live

1. Edit showcase **README** → **Downloads & distribution**: add the **Steam demo** URL as the canonical link.
2. **Remove or archive** old GitHub Release assets if you no longer want playtest builds public.
3. Scan the README for any old “download here” text and update.

## Step 4 — Store compliance

- **Steam:** Fill **AI disclosure** (and other required fields) per [current Steamworks rules](https://partner.steamgames.com/) when you publish the store page.
- Keep a short **credits** note (Godot MIT, third-party assets if any).

## Step 5 — Optional automation (later)

- Godot export via **GitHub Actions** and/or upload to **Itch** with **butler**—only if you want CI; not required for the manual path above.

---

Check off steps in your own tracker; update this file if your tag naming or platforms change.
