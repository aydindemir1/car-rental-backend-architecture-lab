# Day 87 — Vitest, Playwright ve test alternatifleri

Durum: **Planlandı**. Bu eğitim milestone'ı birden fazla takvim gününe yayılabilir. Kod/runtime evidence henüz oluşturulmadı.

## Önkoşul ve kapsam

[Day 86](day-86.md) kapanır; önceki birikimli implementation snapshot'ından `day/87` türetilir. Emlak repo/85 günlük planı değişmez. [Frontend ortak planı](../FRONTEND-ROADMAP-EXTENSION.md), [coverage matrisi](../coverage/frontend-coverage.md) ve [uygulama sözleşmesi](../coverage/mandatory-implementation-contract.md) esas alınır.

Desktop Apps/Mobile Apps ve ilgili native framework/runtime'lar kapsam dışıdır. Web PWA ve responsive browser deneyleri kapsamda kalır. Java/Spring business backend ve canonical veri sahipliği korunur.

## Öğrenme ve uygulama görevleri

Roadmap etiketleri: `Testing`, `Vitest`, `Playwright`, `Jest`, `Cypress`.

1. Vitest ile meaningful form validation/state/cancellation testleri; component integration'da kullanıcı davranışı ve API hata senaryolarını test et.
2. Playwright ile gerçek browser→Java API search/quote/booking success, invalid auth, stale cache ve double-submit senaryolarını çalıştır; mock test ve actual integration'ı ayrı raporla.
3. Yeşil Jest'te aynı bounded unit/integration fixture; Cypress'te bir search/detail ve API error browser akışını gerçekten uygula. Main regression owner Vitest/Playwright kalır.
4. Deterministik fixture, isolation, parallel run, retry/flaky policy, trace/screenshot redaction ve cross-browser test kapsamını tanımla.
5. Testin implementation satırlarını aynalaması yerine contract/invariant ve failure behavior doğrulamasını şart koş.

## Planlanan dosyalar

- `web/tests/`
- `labs/frontend/test-alternatives/`
- `docs/testing/frontend-test-strategy.md`
- `docs/evidence/day-87/` — sürüm/edition, exact komut, browser/runtime, fixture, expected/actual, ölçüm ve recovery.

Bunlar aday implementation çıktılarıdır; dosya/dependency varlığı Verified değildir.

## Commit sırası

1. `docs(day-87): frontend gereksinim ve sınırları tanımla`
2. `feat(day-87): temsilî UI ve eğitim profillerini uygula`
3. `test(day-87): browser contract hata ve toparlanmayı doğrula`
4. `docs(day-87): evidence runbook ve karşılaştırmayı kapat`

Mevcut verified uygulama yeterliyse aynı sorumluluğu tekrar kurma/boş feat commit üretme; actual SHA/evidence ve eksik testleri bağla. Green ürün profilleri ana app'in aynı state/build/controller kaynağına competing owner olmaz.

## Doğrulama ve kapanış

- [ ] Kasıtlı validation/auth/idempotency regression testleri kırar; gerçek Java integration ayrı evidence'a sahiptir.
- [ ] Dört ürünün seçilmiş gerçek test koşusu kayıtlıdır; flaky retry bug'ı sessiz gizlemez.
- [ ] Konu/product/blue etiketleri öğrenme + gerçek temsilî uygulama + runtime evidence ile veya explicit erişim gap'inde izleniyor.
- [ ] Değişen kod için uygun type/lint/unit/integration/build check; ardından gerçek browser/API/local runtime doğrulaması yapıldı.
- [ ] Accessibility, auth/privacy, cancellation/cleanup ve bounded resource davranışı ilgili use-case'te test edildi.
- [ ] Sürüm/lisans/compatibility gün başında doğrulanıp pin edildi; source maps/env/artifact secret sızdırmıyor.
- [ ] Local/managed provider, mock/real API ve CSR/SSR/SSG/PWA kanıtları ayrı raporlandı.
- [ ] Coverage actual duruma güncellendi; yalnız comparison veya static export SSR implementation sayılmadı.

Ücretli cloud/model API/hosting zorunluluğu yoktur; hesap/billing/remote deployment bugün yapılmaz. Local lab production SLA/scale, arama sıralaması veya mesleki unvan kanıtı değildir.
