# QA checklist — MVP ve Demo

Bu form **tek başına veya bir testçiyle** kullanılır. Her satırda **Evet / Hayır / Kısmen** işaretle; **not** sütununa kısa gözlem yaz.

**Build bilgisi (her oturumda doldur):**
- Tarih: 2026-03-28 (MVP-22 freeze + tag `mvp-0.1`)
- Build / commit: `git rev-parse --short HEAD` — yerelde doğrula
- Platform: Windows (Steam hedefi)
- Kontrol: klavye (WASD) + fare (menü/market)

*MVP-01:* `scenes/`, `scripts/`, `resources/`, `assets/` klasör yapısı; proje açılıyor (A1).  
*MVP-02:* `run/main_scene` artık `res://scenes/menu.tscn` (MVP-19); oyun sahnesi kökü `Node2D` (`Main`). F5 → menü → Başlat.  
*MVP-03:* `RunState` autoload; run RNG tek `RandomNumberGenerator` (`reset_run`).  
*MVP-04:* `DamagePipeline` autoload; tüm hasar `apply_damage` tek giriş noktasından.  
*MVP-05:* `scenes/player.tscn` + WASD hareket.  
*MVP-06:* `Camera2D` oyuncu altında, smoothing.  
*MVP-07:* `enemy_base.tscn` + düz çizgi AI.  
*MVP-08/16:* `SpawnManager`; dalga bazlı aralık ve max düşman (`balance.tres`).  
*MVP-09:* Otomatik saldırı + temas hasarı → `DamagePipeline`.  
*MVP-10:* `run_ended` kazanma/kaybetme.  
*MVP-11/14:* `WaveTimer` + `balance.tres` dalga süreleri 60/75/90/105/120 sn.  
*MVP-12:* Materyal +2/kill, tavan 60, HUD.  
*MVP-13:* Dalga arası market, `shop_open`.  
*MVP-14:* `BalanceData` + `balance.tres` merkezi denge.  
*MVP-15:* `wave_hp_multipliers`, `_scaled_hp()`.  
*MVP-17:* HUD paneli (can çubuğu, dalga, materyal).  
*MVP-18:* `SfxBus` + `assets/sfx/*.wav`.  
*MVP-19:* Menü, pause (`PauseOverlay`), sonuç düğmeleri.  
*MVP-20:* Doğrulama; market+pause ESC çakışması giderildi; B tablosu; MVP kabul.
*MVP-22:* MVP freeze (yeni özellik yok, yalnızca bugfix); git tag `mvp-0.1`.

---

## A) MVP build — fonksiyonel (plan: `plan_mvp.md` çıkışı)

| # | Kontrol | Evet | Hayır | Kısmen | Not |
|---|---------|------|-------|--------|-----|
| A1 | Oyun F5 ile açılıyor, ana akışa girilebiliyor | Evet | | | MVP-19: menü → Başlat → oyun. |
| A2 | Oyuncu hareket ediyor; kamera takip ediyor | Evet | | | MVP-05–06. |
| A3 | Düşmanlar spawn oluyor ve tehdit oluşturuyor | Evet | | | MVP-08/16. |
| A4 | Otomatik saldırı çalışıyor (nişan yok) | Evet | | | MVP-09. |
| A5 | Hasar/ölüm tek mantıklı yoldan gidiyor | Evet | | | `DamagePipeline`. |
| A6 | Dalga süreleri 60 / 75 / 90 / 105 / 120 sn | Evet | | | `balance.tres`. |
| A7 | 5 dalga tamamlanınca kazanma | Evet | | | `notify_wave_completed(5)`. |
| A8 | Oyuncu ölünce kaybetme | Evet | | | `run_ended(false)`. |
| A9 | Materyal +2/kill, tavan 60 | Evet | | | HUD. |
| A10 | Dalga sonrası market; 30luk satın alım mümkün | Evet | | | Dalga 1–4. |
| A11 | HP ölçekleme ×1.00 … ×1.40 | Evet | | | `_scaled_hp()`. |
| A12 | Spawn baskısı dalga ile artıyor | Evet | | | 2.2s/8 → 0.9s/35. |
| A13 | Crash/softlock yok | Evet | | | `shop_open` + pause düzeltmesi. |

---

## B) MVP build — denge ve his (`mvp_balance_goals.md`)

| # | Kontrol | Evet | Hayır | Kısmen | Not |
|---|---------|------|-------|--------|-----|
| B1 | Run ~7,5 dk bandı | Evet | | | Toplam 450 sn. |
| B2 | Dalga eğrisi öğren → baskı → climax | | | Kısmen | Playtest onayı gerekir. |
| B3 | Haksız ani sıçrama nadiren | | | Kısmen | Playtest gerekir. |
| B4 | Düşman TTK ~1–4 sn | Evet | | | ~1–1.5 sn. |
| B5 | Markette boş gezme nadiren | | | Kısmen | Kısa dalgada sıkı olabilir. |
| B6 | Market seçenekleri anlamlı | Evet | | | Can + hasar. |
| B7 | Ölüm nedeni okunabilir | | | Kısmen | Can çubuğu var; hasar sayısı yok. |

---

## C) Demo build — ek çubuk (`plan_mvp_to_demo.md`)

| # | Kontrol | Evet | Hayır | Kısmen | Not |
|---|---------|------|-------|--------|-----|
| C1 | Ana menü + ses/tam ekran | | | Kısmen | Tam ekran ayarı yok. |
| C2 | Sonuç ekranı | | | Kısmen | Skor/özet yok. |
| C3 | Market UI okunaklı | | | Kısmen | İkon yok. |
| C4 | SFX | Evet | | | SfxBus. |
| C5 | Müzik | | | | Henüz yok. |
| C6 | Düşük donanım FPS | | | | — |
| C7 | Windows export | Evet | | | MVP-21: release export `build/windows/ProjectA.exe` + smoke run; 2026-03-28. |
| C8 | Steam demo akışı | | | | — |
| C9 | Mağaza sayfası | | | | — |

---

## D) Sonuç kararı

- **MVP onayı:** A kritikleri (A7, A8, A10, A13) Evet.  
- **Demo onayı:** C çoğunluğu Evet değil; MVP-21 sonrası.

**İmzalı karar:**  
- **MVP kabul** — A tamam; B1/B4/B6 Evet; B2/B3/B5/B7 Kısmen.  
- **Demo red** — C2/C3 Kısmen; C5–C6 test dışı; C7 Evet (MVP-21).
