# Distribution plan (Project A showcase)

This file is the **step-by-step** companion to the [Downloads & distribution](../README.md#downloads--distribution) section in the root README.

**Repository visibility:** This showcase repo is **private**. Anonymous visitors cannot read the README or download Releases; only you and collaborators (or future invitees) can.

## Step 0 — Baseline

- Private dev repo: source of truth, regular push, milestone tags.
- **Private** showcase: README (EN + TR), screenshots, `docs/` (blueprint, QA, risk), boundaries documented.

## Step 1 — GitHub profile (you, browser)

- You may still **pin** `project-a-showcase` for your own dashboard; **other users typically will not see private pins** on your public profile.
- For **anonymous** portfolio visibility (recruiters, players), use something **public**: profile README, a future **public** repo, **Steam** / **Itch** page, or a personal site—not this private repo alone.
- Optionally set **bio** and **website** to your **public** link of choice.

## Step 2 — First playtest / pre-demo Release (when you have a build)

1. Export a **Windows** (or chosen) build from Godot in the **private** dev repo.
2. Zip the export folder; **do not** `git add` large binaries to `main` history on showcase—use **Releases** only.
3. On GitHub: **project-a-showcase** → **Releases** → **Draft a new release**.
4. Tag example: `playtest-0.1` or `pre-demo-2026-03` (avoid clashing with private dev repo tags if that matters to you).
5. Title example: `Pre-demo playtest (not Steam demo)`.
6. Description: short notes + “**Pre-demo only**; final demo will be on Steam.”
7. Attach the zip as a release asset; **Publish**.

**Note:** Because the repo is private, testers need **GitHub access** to this repository (or you distribute the zip another way).

## Step 3 — After Steam demo goes live

1. Edit showcase **README** → **Downloads & distribution**: add the **Steam demo** URL as the canonical link for **everyone**.
2. **Remove or archive** old GitHub Release assets if you no longer want playtest builds on GitHub.
3. Scan the README for any old “download here” text and update.

## Step 4 — Store compliance

- **Steam:** Fill **AI disclosure** (and other required fields) per [current Steamworks rules](https://partner.steamgames.com/) when you publish the store page.
- Keep a short **credits** note (Godot MIT, third-party assets if any).

## Step 5 — Optional automation (later)

- Godot export via **GitHub Actions** and/or upload to **Itch** with **butler**—only if you want CI; not required for the manual path above.

---

Check off steps in your own tracker; update this file if your tag naming or platforms change.
