# Blueprint (v0) — Brotato-like 2D (Godot 4.6.1, GDScript)

## 1) One-sentence pitch
- Bu oyun: Tek bir karakterle dalga dalga düşmanları kesip, düşen materyalleri toplayarak tur sonunda marketten eşya/güçlendirme alıp güçlendiğin ve toplam 5 dalga hayatta kalmayı hedeflediğin 2D bir roguelite run deneyimi.

## 2) Target player / session
- **Target player**: Vampire Survivors veya Brotato gibi 2D roguelite/roguelike oyunları oynamayı seven oyuncular.
- **Target session length (5 dalga run)**: Dalga süreleri: 1. dalga **60 sn**; sonraki her dalga bir öncekinden **+15 sn** (2→75 sn, 3→90 sn, 4→105 sn, 5→120 sn). **Toplam ≈ 7,5 dk** (450 sn) — kazanma koşulu 5 dalga hayatta kalmak.
- **Platform**: PC (Steam)

## 3) Core gameplay loop (plain language)
Oyuncu dalga boyunca düşmanları keser ve materyal toplar → oyun yeni düşman dalgalarıyla baskıyı artırır → oyuncu dalga sonunda marketten eşya/güçlendirme satın alarak build’ini şekillendirir → 5 dalgayı hayatta kalırsa kazanır (ölürse run biter).

## 4) MVP / Vertical Slice (ilk “tam oynanabilir dilim”)
### Definition of “done”
- **Must have**
  - Player hareket + temel kontrol
  - Düşmanlar spawn olur ve oyuncuya yaklaşır
  - Basit hasar/ölüm (oyuncu ve düşman için)
  - Wave/süre ilerler ve bir “fail condition” vardır (ölüm veya süre biter)
  - Dalga arası market: toplanan materyalle en az 1 satın alma / güçlendirme seçimi (MVP’de sınırlı ürün listesi yeter)
- **Nice to have (sonra)**
  - Ses/partikül/polish
  - Çoklu silah/upgrade çeşitliliği

## 5) NOT IN THIS GAME (scope kalkanı)
MVP ve ilk demo için aşağıdaki sistemler **bilinçli olarak yok** (Brotato / VS tarzı çekirdeğe odaklanmak için):

- Multiplayer / co-op yok
- PvP yok
- Açık dünya / büyük harita keşfi yok
- Hikâye / diyalog / uzun metinler yok (MVP ve demo öncesi)
- Crafting (malzeme ile eşya üretme) yok
- Base building (üs kurma) yok
- Metroidvania tarzı kalıcı harita ilerleme yok
- Karmaşık envanter yönetimi (grid, ağırlık vb.) yok
- Procedural dünya / oda üretimi yok
- Online leaderboard / cloud save yok (ilk sürümlerde)

**Belki sonra (demo / erken erişim sonrası, ayrı karar):** Çok kısa flavor metin veya mini hikâye — blueprint v1’de netleştirilir; MVP’yi şişirmemek için şimdilik dışarıda.

## 6) Game pillars (3 madde)
1. **Yüksek tekrar oynanabilirlik:** Run’lar **kısa** ve **tekrarlanabilir**; oyuncu “bir tur daha” diyebileceği tempoda kalsın.
2. **Dalgalar arası seçim:** **Toplanan materyalle** marketten **silah veya güçlendirme** satın alarak build’ini şekillendirmek — run’un stratejik omurgası bu.
3. **Öngörülebilir zorluk:** Zorluk eğrisi öngörülebilir artar; **“haksız” ani sıçramalar** yok. Dalga ilerledikçe baskı artsın ama oyuncu “neden şimdi bu kadar zor?” demesin; sıkıcı düz çizgi veya sebepsiz zorluk sıçraması hedeflenmez.

## 7) Minimal milestones (çok kısa)
- **M0 — Vertical Slice**: Bölüm 4 “done” şartları sağlandı.
- **M1 — Alpha**: Core loop + 2–3 düşman + 2–3 upgrade, UI temel; crash yok.
- **M2 — Beta**: İçerik “yeterli” (örn. 10 upgrade, 5 düşman), balans turu; performans kabul edilebilir.
- **M3 — RC / Steam-ready**: Export alınır, store build çalışır; kritik bug yok.

## 8) Open questions (AI’ye ve bana hatırlatıcı) — kararlar (MVP)
- **Saldırı modeli:** **Otomatik saldırı (VS benzeri)** — oyuncu hareket + kaçınma; silahlar kendi vurur. MVP’de nişanlı / manuel ateş yok.
- **Meta progression:** **MVP’de yok.** Sadece run içi materyal + dalga arası market; her run sıfırdan (kalıcı unlock / meta para yok). İleride “oyuncu sıkılıyor mu?” sorusuna göre hafif meta ayrı karar.

## 9) MVP balance goals
İlk oynanabilir sürüm için **6 adet** denge hedefi (tempo, dalga eğrisi, TTK bandı, ekonomi/market, seçim anlamı, ölüm hissi) ve sayısal v0 hipotezleri, **ayrıntılı denge notları** ile birlikte **özel geliştirme deposundaki** `docs/mvp_balance_goals.md` dosyasında tutulur; playtest ile güncellenir.

**Ölçekleme (v0, özet):** Zorluk öncelikle **spawn / baskı** ile artar; düşman **HP** doğrusal çarpanla (`×1.00` … `×1.40`, 5 dalga). Ekonomi: **2 materyal/öldürme**, tavan **60**, en ucuz teklif **30**.

## 10) Geliştirme planları (bu vitrin deposunda)
Bu repoda **yüksek seviye** blueprint, [`qa_checklist.md`](qa_checklist.md) ve [`risk_register.md`](risk_register.md) bulunur. **Sprint tabloları, ayrıntılı MVP→Demo planları ve CSV takip dosyaları** ticari süreç için **özel geliştirme deposunda** kalır; vitrin ile orayı senkron tutmak bakımcının sorumluluğundadır.

