# Geliştirme planı — MVP → Demo (AI uyumlu, adım-komut modeli)

Bu dosya özet planıdır. Asıl takip tablosu: `docs/plan_demo_table.csv` (LibreOffice Calc ile aç).

## Kullanım (MVP planıyla aynı)

1. `plan_demo_table.csv` içinde sıradaki `TODO` adımı seç.
2. Bana `Step ID` ver: "DEMO-XX adımını yap".
3. Adım bitince QA/Risk/Git döngüsünü tabloya göre uygula.
4. `Status` değerini `DONE` yapıp sıradaki adıma geç.

## Demo hedefi (kısa)

- Core loop anlaşılır.
- İçerik çeşitliliği MVP'den belirgin yüksek.
- UI/SFX/VFX minimum cilalı.
- Windows release build çalışır.
- Steam mağaza varlıkları demo duyurusuna hazır.

## Model geçiş kuralı (genel)

- Her adımda önce tabloda yazan **Önerilen model** ile ilerle.
- Aynı hata tekrar ediyorsa, **aynı modelle 2 deneme** yap.
- Hata iki denemede de çözülmezse, tabloda yazan **Hata olursa geç** modeline geç.
- Fallback modelinde de 2 denemede çözülmezse, adımı daha küçük alt adıma böl (`DEMO-XX.1` vb.) ve tekrar dene.

## Plan referansları

- Demo tablo: `docs/plan_demo_table.csv`
- Blueprint: `docs/blueprint.md`
- Denge hedefleri: `docs/mvp_balance_goals.md`
- QA formu: `docs/qa_checklist.md`
- Risk kaydı: `docs/risk_register.md`
