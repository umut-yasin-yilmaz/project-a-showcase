# Distribution plan (Project A showcase)

Companion to the [Downloads & releases](../README.md#downloads--releases) section in the root README.

## Roles

- **Private dev repository (`project-a`):** source of truth for code, assets, and milestone tags.
- **This showcase repository (`project-a-showcase`):** public-facing narrative, safe `docs/`, screenshots on `main`, and **Windows playtest zips** attached to **Releases** (never committed to `main`).

## Maintainer: pin on GitHub profile

After the showcase is the page you want visitors to see first:

1. Open your GitHub profile while logged in → **Customize your pins** (or profile editor).
2. Pin **`project-a-showcase`** (up to six repositories).
3. Optionally set **Bio** and **Website** to this repo or a future store page.

Private pins are only visible to you; public visitors see public pinned repos.

## Playtest release (Godot export → zip → GitHub)

Detailed steps: [`godot_export_and_release.md`](godot_export_and_release.md).

1. In the private `project-a` repo, export **Windows Desktop** (preset → `build/windows/ProjectA.exe`).
2. Zip the **`build/windows/`** output (exe + `.pck` and any DLLs together). **Do not** commit the zip to either repo’s `main`.
3. On GitHub: **project-a-showcase** → **Releases** → **Draft a new release**.
4. Create a new tag, e.g. `playtest-0.1` or `build-2026-03-28`.
5. Title example: `Windows playtest build`.
6. Description: [`release_playtest_template.md`](release_playtest_template.md).
7. Attach the zip → **Publish**.

Anyone can download from **Releases** while this repository is **public**. Use **Collaborators** only if you ever need a private preflight.

## After a store demo exists (later)

*Skip until you actually ship a store demo (e.g. Steam).*

1. Update the root README **Downloads & releases** with an official demo / store link if you want one canonical URL.
2. Archive or remove obsolete playtest Release assets if they confuse players.
3. Align download wording with what you actually ship.

## Store compliance (when you have a store page)

- **Steam:** complete required disclosures (including AI-related fields when applicable) per [Steamworks](https://partner.steamgames.com/) rules.
- Keep [`credits_and_licenses.md`](credits_and_licenses.md) updated and mirror essentials in-game / on the store when required.

## Optional automation (later)

- Godot export via **GitHub Actions** and/or upload to **Itch** with **butler**—only if you want CI; not required for the manual path above.

---

## Appendix: visibility pre-flight (toggling public / private)

Use this before changing repository visibility so you do not surprise visitors or leak work-in-progress.

**Content**

- README (EN + TR): no draft phrases you do not want seen; screenshots match the advertised build (e.g. tag `mvp-0.1`).
- `docs/*.md`: safe for outsiders—no secrets, keys, or internal credentials.
- `assets/showcase/`: only portfolio-safe crops; no raw commercial sources.

**GitHub**

- Default branch is **`main`**.
- No large binaries on `main` (use **Releases** for zips).
- After visibility changes, open the repo in a **logged-out** or incognito window: README renders, images load, Releases behave as expected.

Update this file when your tag naming or target platforms change.
