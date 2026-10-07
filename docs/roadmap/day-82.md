# Day 82 — TypeScript ve runtime contract sınırları

Durum: **Planlandı**. Bu eğitim milestone'ı birden fazla takvim gününe yayılabilir. Kod/runtime evidence henüz oluşturulmadı.

## Önkoşul ve kapsam

[Day 81](day-81.md) kapanır; önceki birikimli implementation snapshot'ından `day/82` türetilir. Emlak repo/85 günlük planı değişmez. [Frontend ortak planı](../FRONTEND-ROADMAP-EXTENSION.md), [coverage matrisi](../coverage/frontend-coverage.md) ve [uygulama sözleşmesi](../coverage/mandatory-implementation-contract.md) esas alınır.

Desktop Apps/Mobile Apps ve ilgili native framework/runtime'lar kapsam dışıdır. Web PWA ve responsive browser deneyleri kapsamda kalır. Java/Spring business backend ve canonical veri sahipliği korunur.

## Öğrenme ve uygulama görevleri

Roadmap etiketleri: `Type Checkers`, `TypeScript`.

1. Strict TypeScript configuration; union/discriminated union, generics, narrowing, readonly ve unknown kullanarak API/UI state'lerini modelle.
2. API JSON'unu runtime schema validation ile doğrula; TypeScript type assertion'ın untrusted payload'ı doğrulamadığını gerçek malformed fixture ile göster.
3. Type-only imports, declaration/module resolution ve tsconfig project boundary'sini kur; tsc --noEmit CI gate'i olsun.
4. Public env ve server-only secret sınırını tanımla; browser bundle'da credential olmadığını artifact incelemesiyle test et.

## Planlanan dosyalar

- `web/tsconfig.json`
- `web/contracts/`
- `labs/frontend/type-checking/`
- `docs/evidence/day-82/` — sürüm/edition, exact komut, browser/runtime, fixture, expected/actual, ölçüm ve recovery.

Bunlar aday implementation çıktılarıdır; dosya/dependency varlığı Verified değildir.

## Commit sırası

1. `docs(day-82): frontend gereksinim ve sınırları tanımla`
2. `feat(day-82): temsilî UI ve eğitim profillerini uygula`
3. `test(day-82): browser contract hata ve toparlanmayı doğrula`
4. `docs(day-82): evidence runbook ve karşılaştırmayı kapat`

Mevcut verified uygulama yeterliyse aynı sorumluluğu tekrar kurma/boş feat commit üretme; actual SHA/evidence ve eksik testleri bağla. Green ürün profilleri ana app'in aynı state/build/controller kaynağına competing owner olmaz.

## Doğrulama ve kapanış

- [ ] Kasıtlı type error gate'i kırar; malformed API payload runtime'da reddedilir.
- [ ] Loading/success/error union'ları exhaustiveness kontrolüne sahiptir; browser artifact'ta server credential yoktur.
- [ ] Konu/product/blue etiketleri öğrenme + gerçek temsilî uygulama + runtime evidence ile veya explicit erişim gap'inde izleniyor.
- [ ] Değişen kod için uygun type/lint/unit/integration/build check; ardından gerçek browser/API/local runtime doğrulaması yapıldı.
- [ ] Accessibility, auth/privacy, cancellation/cleanup ve bounded resource davranışı ilgili use-case'te test edildi.
- [ ] Sürüm/lisans/compatibility gün başında doğrulanıp pin edildi; source maps/env/artifact secret sızdırmıyor.
- [ ] Local/managed provider, mock/real API ve CSR/SSR/SSG/PWA kanıtları ayrı raporlandı.
- [ ] Coverage actual duruma güncellendi; yalnız comparison veya static export SSR implementation sayılmadı.

Ücretli cloud/model API/hosting zorunluluğu yoktur; hesap/billing/remote deployment bugün yapılmaz. Local lab production SLA/scale, arama sıralaması veya mesleki unvan kanıtı değildir.
