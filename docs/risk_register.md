# Risk kaydı (Risk register) — Project A

Amaç: Erken fark et, **tetikleyiciyi** izle, **önlem** al. Her sprint sonunda 10 dakika gözden geçir.

| ID | Risk | Olasılık | Etki | Erken uyarı (tetikleyici) | Önlem / hafifletme | Sahip |
|----|------|----------|------|---------------------------|---------------------|-------|
| R1 | **Scope şişmesi** — “şunu da ekleyelim” ile MVP gecikir | Yüksek | Yüksek | Yeni özellik talebi blueprint **NOT IN THIS GAME** ile çelişiyor | MVP bitene kadar yeni sistem yok; sadece bug/denge; istekleri ayrı bir “sonra” listesine yaz (GitHub Issue veya kısa not) | Sen |
| R2 | **Denge kırılması** — ekonomi veya spawn HP ile uyumsuz | Yüksek | Orta | “Çok kolay / imkânsız” iç test notları artıyor | Denge notları + veri odaklı tablolar (özel depo); tek seferde tek eksen değiştir | Sen |
| R3 | **Determinizm / RNG dağılması** — farklı build’lerde farklı sonuç | Orta | Yüksek | `randf()` ile outcome; kaydedilemeyen run | Run-scoped RNG; tek RNG kaynağı ve kurallar özel depoda dokümante | Sen + AI |
| R4 | **Performans** — çok varil / düşman ile FPS düşüşü | Orta | Orta | Profiler’da düşük FPS; frame spike | Object pooling (sonra); MVP’de düşman üst sınırı | Sen |
| R5 | **AI bağlam kaybı** — sohbet sıfırlanınca yanlış kod üretimi | Yüksek | Orta | Aynı hatayı iki kez düzeltme | Git commit + `docs/blueprint.md` + durum notu; transcript export | Sen |
| R6 | **Steam / export sürprizi** — geç build hatası | Orta | Yüksek | İlk export denemesi çok geç | Milestone’da export görevi erken; preset’i sürekli doğrula | Sen |
| R7 | **Telif / asset** — lisanssız görsel/ses | Düşük | Çok yüksek | Kaynağı belirsiz dosya `assets/` içinde | Sadece lisansı net paketler; `THIRD_PARTY.md` (demo öncesi) | Sen |

---

## Bu sprintte bakılacak 3 soru

1. Blueprint’e aykırı yeni özellik ekledik mi?  
2. Son iç testte B1–B7’den hangisi “Hayır”a kaydı?  
3. Son commit’ten beri kritik crash var mı?

---

## Not

Yeni risk eklendiğinde tabloya satır ekleyin; **kapandı** ise “çözüldü” tarihi ve kısa not yazın.
