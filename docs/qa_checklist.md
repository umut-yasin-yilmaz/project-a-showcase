# QA checklist — MVP ve Demo

Bu form **tek başına veya bir testçiyle** kullanılır. Her satırda **Evet / Hayır / Kısmen** işaretle; **not** sütununa kısa gözlem yaz.

**Build bilgisi (her oturumda doldur):**
- Tarih: ____
- Build / commit: `git rev-parse --short HEAD` → ____
- Platform: Windows (Steam hedefi)
- Kontrol: klavye (WASD) + fare (varsa)

---

## A) MVP build — fonksiyonel (plan: `plan_mvp.md` çıkışı)

| # | Kontrol | Evet | Hayır | Kısmen | Not |
|---|---------|------|-------|--------|-----|
| A1 | Oyun F5 ile açılıyor, ana akışa girilebiliyor | | | | |
| A2 | Oyuncu hareket ediyor; kamera takip ediyor | | | | |
| A3 | Düşmanlar spawn oluyor ve tehdit oluşturuyor | | | | |
| A4 | Otomatik saldırı çalışıyor (nişan yok) | | | | |
| A5 | Hasar/ölüm tek mantıklı yoldan gidiyor (gözle görülür bug yok) | | | | |
| A6 | Dalga süreleri blueprint ile uyumlu: 60 / 75 / 90 / 105 / 120 sn | | | | |
| A7 | 5 dalga tamamlanınca **kazanma** tetikleniyor | | | | |
| A8 | Oyuncu ölünce **kaybetme** tetikleniyor | | | | |
| A9 | Materyal: öldürme başına +2, tavan 60 (UI veya debug ile doğrulanabiliyor) | | | | |
| A10 | Her dalga sonrası market açılıyor; en ucuz 30 ile **en az bir** satın alma mümkün | | | | |
| A11 | HP ölçeklemesi: dalga 1→5 doğrusal çarpan (×1.00 … ×1.40) hissediliyor | | | | |
| A12 | Spawn baskısı dalga ile artıyor (ana zorluk ekseni) | | | | |
| A13 | Crash yok; softlock yok (menüde/trende takılma) | | | | |

---

## B) MVP build — denge ve his (`mvp_balance_goals.md`)

| # | Kontrol | Evet | Hayır | Kısmen | Not |
|---|---------|------|-------|--------|-----|
| B1 | Run toplam süresi ~7,5 dk bandında “sıkıcı uzun” hissi vermiyor | | | | |
| B2 | 1. dalga öğrenilebilir; 3. dalga baskı artıyor; 5. dalga climax | | | | |
| B3 | “Haksız ani sıçrama” hissi nadiren (neden zorlandığım okunuyor) | | | | |
| B4 | Tipik düşman TTK ~1–4 sn bandı (sünger / kaçamama uçları yok) | | | | |
| B5 | Markette “boş gezdim / harcayamadım” nadiren | | | | |
| B6 | Market seçeneklerinde en az biri “mantıklı” (hepsi çöp değil) | | | | |
| B7 | Ölüm sonrası “neden öldüm?” cevabı verilebiliyor | | | | |

---

## C) Demo build — ek çubuk (`plan_mvp_to_demo.md`)

| # | Kontrol | Evet | Hayır | Kısmen | Not |
|---|---------|------|-------|--------|-----|
| C1 | Ana menü + ses/tam ekran ayarları çalışıyor | | | | |
| C2 | Run özeti veya sonuç ekranı var | | | | |
| C3 | Market UI: fiyat + ikon/kısa açıklama okunaklı | | | | |
| C4 | SFX seti temel olayları karşılıyor (sessiz değil) | | | | |
| C5 | Müzik loop (en az 1) run sırasında rahatsız etmiyor | | | | |
| C6 | Düşük donanımda hedef FPS’e yakın (kendi PC’nde not) | | | | |
| C7 | Windows release export ile çalışan klasör build’i | | | | |
| C8 | Steam demo hedefi varsa: demo app / depo akışı test edildi | | | | |
| C9 | Mağaza sayfası: capsule + en az 6 screenshot + kısa açıklama güncel | | | | |

---

## D) Sonuç kararı

- **MVP onayı:** A ve B tablolarında **kritik maddeler** (A13 crash, A7–A8 win/lose, A10 market) tam **Evet** olmalı.  
- **Demo onayı:** C tablosunda çoğunluk **Evet**; kalanlar için bilinen sorunlar listesi + tarih.

**İmzalı karar:**  
- Bu build **MVP kabul** / **red** — gerekçe: ____  
- Bu build **Demo kabul** / **red** — gerekçe: ____
