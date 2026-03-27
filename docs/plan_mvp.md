# Geliştirme planı — MVP (AI uyumlu, adım-komut modeli)

Bu dosya özet planıdır. Asıl takip tablosu: `docs/plan_mvp_table.csv` (LibreOffice Calc ile aç).

## Bu plan mantıklı mı?

Evet. Hem klasik indie üretim sıralaması (prototype/vertical slice -> alpha/beta) hem AI-assisted geliştirmede önerilen "küçük adım + doğrula + checkpoint commit" yaklaşımıyla uyumlu.

## Kullanım (senin tarif ettiğin gibi)

1. `plan_mvp_table.csv` içinde `Status=TODO` olan sıradaki adımı seç.
2. Bana sadece `Step ID` söyle: "MVP-XX adımını yap".
3. Ben adımı tamamlayınca sen:
   - `docs/qa_checklist.md` içindeki ilgili satırları doldur.
   - `docs/risk_register.md` içinde ilgili riskleri kontrol et.
   - `git status && git add -A && git commit -m "..." && git push` yap.
4. Tabloda `Status` değerini `DONE` yapıp sonraki adıma geç.

## Data-driven ne zaman?

`MVP-14` adımı: çekirdek loop çalışır çalışmaz, sayı patlamadan hemen yapılır.

## Model geçiş kuralı (genel)

- Her adımda önce tabloda yazan **Önerilen model** ile ilerle.
- Aynı hata tekrar ediyorsa, **aynı modelle 2 deneme** yap.
- Hata iki denemede de çözülmezse, tabloda yazan **Hata olursa geç** modeline geç.
- Fallback modelinde de 2 denemede çözülmezse, adımı daha küçük alt adıma böl (`MVP-XX.1` vb.) ve tekrar dene.

## Plan referansları

- MVP tablo: `docs/plan_mvp_table.csv`
- Blueprint: `docs/blueprint.md`
- Denge hedefleri: `docs/mvp_balance_goals.md`
- QA formu: `docs/qa_checklist.md`
- Risk kaydı: `docs/risk_register.md`
