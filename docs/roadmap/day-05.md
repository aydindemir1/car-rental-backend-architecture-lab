# Day 05 — CSS ve responsive görünüm

Durum: **Planlandı**. Day bir milestone'dır; takvim günü sınırı yoktur.

## Önkoşul ve scope

[Day 4](day-04.md) kapanır; cumulative implementation branch'inden `day/05` türetilir. Bu gün başka datastore'ların sahipliğini devralmaz. Ortak kararlar [Project Decisions](../PROJECT-DECISIONS.md) belgesindedir.

## Görevler

1. Flexbox, Grid, responsive breakpoints, typography, layout ve focus states ile HTML ekranlarını tamamla.
2. Requirement, alternatif, data/resource ownership, failure mode ve version compatibility kararını ADR'ye kaydet.
3. Mevcut dosya yapısında minimal gerçek use-case'i uygula; ihtiyaç yoksa aynı responsibility için ikinci ürün ekleme.
4. Mobil/desktop görünüm ve focus görünürlüğü için ekran kanıtı kaydet.
5. Öğrenme notunu, runbook'u, ölçüm koşullarını ve karşılaştırma sonucunu güncelle.

## Planlanan dosyalar

- `web/`
- `docs/frontend/css-responsive.md`
- `docs/evidence/day-05/` — secretsız komut, çıktı, sürüm ve ölçümler; bu yollar henüz implementation değildir.

## Commit sırası

1. `docs(day-05): scope ve sahiplik kararını tanımla`
2. `feat(day-05): temsilî çalışma ve adapterları uygula`
3. `test(day-05): başarı hata ve toparlanmayı doğrula`
4. `docs(day-05): actual evidence ve runbookları kapat`

Dosya ve sorumluluklar implementation sırasında incelenir; task yapılmadan boş commit oluşturulmaz.

## Kapanış ölçütleri

- [ ] Bu günün öğrenme konuları proje örneğiyle açıklanabiliyor.
- [ ] Gerekli build/CI başarılı; sonra local runtime/API/browser doğrulaması yapıldı.
- [ ] Yukarıdaki başarı/hata senaryoları gerçek runtime üzerinde gözlendi; expected/actual ve recovery kaydedildi.
- [ ] Secret/PII/anahtar ve gerçek ödeme bilgisi Git/evidence içine girmedi.
- [ ] Sürüm/lisans/uyumluluk ve RAM/CPU/disk bütçesi kaydedildi.
- [ ] İki proje coverage satırları gerçek duruma göre güncellendi; kanıt olmadan Verified işaretlenmedi.

Yerel emulator, benchmark ve toy lab sonucu production SLA/HA/scale kanıtı değildir. Ücretli cloud/model API zorunluluğu yoktur.


## Full Stack ek görevi — Tailwind CSS

CSS temellerinden sonra Tailwind CSS'i gerçek araç kiralama frontend'inde uygula. Minimal npm/package/Vite bootstrap bu gün yapılır; ayrıntılı package yönetimi Day 06'da öğrenilir. Sürümler resmi compatibility ile pin edilir; ücretli Tailwind UI/Plus gerekmez.

- Utility classes, theme tokens, responsive breakpoints ve hover/focus/disabled durumlarıyla araç kartı, arama formu ve reservation layout oluştur.
- Native CSS'teki grid/flex/spacing karşılıklarını açıkla; framework kullanımı CSS temelinin yerine geçmez.
- Üretilen CSS'in production build'de bulunduğunu, dynamic class seçimlerinin kaybolmadığını ve mobil/desktop/a11y durumlarını test et.
- Dosyalar: `web/package.json`, `web/package-lock.json`, `web/vite.config.ts`, `web/src/styles/`, `docs/frontend/tailwind.md`.
- Commit: `feat(frontend): Tailwind responsive bileşenlerini ve production CSS buildini ekle`; sonra ilgili test/evidence.
