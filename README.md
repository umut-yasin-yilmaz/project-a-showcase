# Project A

[![MVP shipped](https://img.shields.io/badge/MVP-Shipped-2ea043?style=for-the-badge)](https://github.com/umut-yasin-yilmaz/project-a-showcase/releases)
[![Engine](https://img.shields.io/badge/Engine-Godot%204.6.1-478CBF?style=for-the-badge&logo=godot-engine&logoColor=white)](https://godotengine.org/)
[![Stack](https://img.shields.io/badge/Code-Typed%20GDScript-2f2f2f?style=for-the-badge)](https://docs.godotengine.org/en/stable/tutorials/scripting/gdscript/static_typing.html)

![Project A — showcase banner](assets/showcase/hero-mvp.svg)

**Project A** is a **2D roguelite / survivor-like** in development—**Brotato-style** pacing, short runs, and shop choices between waves.

This repository is the **public showcase**: design intent, process artifacts, screenshots, and **optional Windows playtest builds** via [Releases](https://github.com/umut-yasin-yilmaz/project-a-showcase/releases). **Full source and commercial assets stay in a private development repository.**

| | |
|:---|:---|
| **Status** | **MVP shipped** — private dev repo milestones `MVP-01` → `MVP-22`; Git tag **`mvp-0.1`** |
| **Engine** | Godot **4.6.1** |
| **Language** | Typed **GDScript** (production) |
| **Platform target** | PC (**Steam-first**; store page not linked here until that phase is real) |
| **Workflow** | Solo developer; **AI as implementation assistant**—design priorities and acceptance criteria reviewed manually |

## Screenshots (MVP build)

| | | |
| :---: | :---: | :---: |
| ![MVP gameplay 1](assets/showcase/mvp-screenshot-01.png) | ![MVP gameplay 2](assets/showcase/mvp-screenshot-02.png) | ![MVP gameplay 3](assets/showcase/mvp-screenshot-03.png) |

## Core loop

- Fight enemies in timed waves  
- Collect materials from defeated enemies  
- Buy upgrades between waves  
- Survive the full run (MVP: **5 waves** — see [`docs/blueprint.md`](docs/blueprint.md))

## Downloads & releases

- **Playtest (Windows):** check [**Releases**](https://github.com/umut-yasin-yilmaz/project-a-showcase/releases) for the latest zip. Extract and run **`ProjectA.exe`** with all files in the same folder.  
- **Non-commercial** playtest drops unless a release explicitly states otherwise. Not a finished commercial product.  
- **No game source on `main`.** Zips are **not** committed to git—only attached to Releases.

Maintainer workflow (export → zip → Release): [`docs/godot_export_and_release.md`](docs/godot_export_and_release.md) · Release notes template: [`docs/release_playtest_template.md`](docs/release_playtest_template.md) · Full distribution notes: [`docs/distribution_plan.md`](docs/distribution_plan.md)

**Feedback:** [Issues](https://github.com/umut-yasin-yilmaz/project-a-showcase/issues) welcome with build tag and repro steps.

## Documentation

| Document | What it is |
|----------|------------|
| [`docs/blueprint.md`](docs/blueprint.md) | Pitch, session target, core loop, scope / non-goals |
| [`docs/qa_checklist.md`](docs/qa_checklist.md) | MVP + Demo QA gates (Turkish checklist, aligned with shipped MVP) |
| [`docs/risk_register.md`](docs/risk_register.md) | Production risks and mitigations |
| [`docs/credits_and_licenses.md`](docs/credits_and_licenses.md) | Godot MIT, credits, rights |
| [`docs/distribution_plan.md`](docs/distribution_plan.md) | Releases, store handoff, visibility pre-flight |
| [`docs/godot_export_and_release.md`](docs/godot_export_and_release.md) | Godot → zip → GitHub Release |
| [`docs/release_playtest_template.md`](docs/release_playtest_template.md) | Copy-paste Release description |

**Suggested reading order:** blueprint → QA checklist → risk register.

## Repository boundaries

**Included here (safe / curated)**  

- Vision, high-level gameplay goals, MVP milestone context  
- Process artifacts that do not expose production internals  
- Portfolio-ready screenshots  

**Stays in the private dev repository only**  

- Full gameplay source and architecture internals  
- Commercial art, audio, and content pipeline  
- Implementation-level balance tables beyond what this README and blueprint summarize  
- Secrets, credentials, or release-sensitive configuration  

## License & security

- Showcase repo: see [`LICENSE`](LICENSE) and [`docs/credits_and_licenses.md`](docs/credits_and_licenses.md).  
- Vulnerability reporting: [`SECURITY.md`](SECURITY.md).  
- Contributions: [`CONTRIBUTING.md`](CONTRIBUTING.md).

---

## Türkçe

[![MVP](https://img.shields.io/badge/MVP-Yayında-2ea043?style=for-the-badge)](https://github.com/umut-yasin-yilmaz/project-a-showcase/releases)
[![Motor](https://img.shields.io/badge/Motor-Godot%204.6.1-478CBF?style=for-the-badge&logo=godot-engine&logoColor=white)](https://godotengine.org/)

![Project A — vitrin](assets/showcase/hero-mvp.svg)

**Project A**, **Brotato** tempolu bir **2D roguelite / survivor-like** projesidir; kısa koşular ve dalgalar arası dükkân seçimleri odakta.

Bu depo **herkese açık vitrin** katmanıdır: tasarım niyeti, süreç dokümanları, ekran görüntüleri ve isteğe bağlı **Windows playtest** paketleri [**Releases**](https://github.com/umut-yasin-yilmaz/project-a-showcase/releases) üzerinden. **Tam kaynak ve ticari assetler özel geliştirme deposunda kalır.**

| | |
|:---|:---|
| **Durum** | **MVP tamam** — özel repoda `MVP-01` → `MVP-22`; Git etiketi **`mvp-0.1`** |
| **Motor** | Godot **4.6.1** |
| **Dil** | **Typed GDScript** (üretim) |
| **Hedef platform** | PC (**Steam öncelikli**; mağaza sayfası o aşama gerçekleşene kadar burada yok) |
| **Süreç** | Tek başına geliştirme; **yapay zekâ uygulama asistanı** — tasarım öncelikleri ve kabul manuel |

### Ekran görüntüleri (MVP)

| | | |
| :---: | :---: | :---: |
| ![Oyun 1](assets/showcase/mvp-screenshot-01.png) | ![Oyun 2](assets/showcase/mvp-screenshot-02.png) | ![Oyun 3](assets/showcase/mvp-screenshot-03.png) |

### Çekirdek döngü

- Zamanlı dalgalarda savaş  
- Materyal toplama  
- Dalgalar arası yükseltme satın alma  
- Koşuyu tamamlama (MVP: **5 dalga** — ayrıntı [`docs/blueprint.md`](docs/blueprint.md))

### İndirme

- **Windows playtest:** [**Releases**](https://github.com/umut-yasin-yilmaz/project-a-showcase/releases) sayfasından zip; açıp **`ProjectA.exe`** çalıştırın, dosyaları ayırmayın.  
- Varsayılan olarak **ticari olmayan** playtest; nihai ürün değildir.  
- **`main` dalında oyun kaynağı yok.** Zip’ler repoya commit edilmez.

Bakım akışı: [`docs/godot_export_and_release.md`](docs/godot_export_and_release.md) · [`docs/distribution_plan.md`](docs/distribution_plan.md)

**Geri bildirim:** [Issues](https://github.com/umut-yasin-yilmaz/project-a-showcase/issues)

### Dokümanlar

[`docs/blueprint.md`](docs/blueprint.md) · [`docs/qa_checklist.md`](docs/qa_checklist.md) · [`docs/risk_register.md`](docs/risk_register.md) · [`docs/credits_and_licenses.md`](docs/credits_and_licenses.md) · [`docs/distribution_plan.md`](docs/distribution_plan.md) · [`docs/godot_export_and_release.md`](docs/godot_export_and_release.md) · [`docs/release_playtest_template.md`](docs/release_playtest_template.md)

**Önerilen sıra:** blueprint → QA checklist → risk register.

### Lisans ve güvenlik

[`LICENSE`](LICENSE) · [`SECURITY.md`](SECURITY.md) · [`CONTRIBUTING.md`](CONTRIBUTING.md) · [`docs/credits_and_licenses.md`](docs/credits_and_licenses.md)
