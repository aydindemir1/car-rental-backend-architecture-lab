# Day 94 — Frontend performance, cache ve Lighthouse

Durum: **Planlandı**. Bu eğitim milestone'ı birden fazla takvim gününe yayılabilir. Kod/runtime evidence henüz oluşturulmadı.

## Önkoşul ve kapsam

[Day 93](day-93.md) kapanır; önceki birikimli implementation snapshot'ından `day/94` türetilir. Emlak repo/85 günlük planı değişmez. [Frontend ortak planı](../FRONTEND-ROADMAP-EXTENSION.md), [coverage matrisi](../coverage/frontend-coverage.md) ve [uygulama sözleşmesi](../coverage/mandatory-implementation-contract.md) esas alınır.

Desktop Apps/Mobile Apps ve ilgili native framework/runtime'lar kapsam dışıdır. Web PWA ve responsive browser deneyleri kapsamda kalır. Java/Spring business backend ve canonical veri sahipliği korunur.

## Öğrenme ve uygulama görevleri

Roadmap etiketleri: `Performance`, `Lighthouse`, `DevTools Usage`, `Cache-Control`.

1. Lighthouse ve DevTools ile mevcut CSR/SSR/SSG fixture'larının LCP/CLS/INP ilgili lab sinyalleri, request waterfall, bundle size, CPU ve memory davranışını ölç.
2. Lab Lighthouse puanı ile gerçek kullanıcı field metric/p75 INP'yi ayır; local sentetik ölçüm production Core Web Vitals başarısı değildir.
3. Image/font optimization, lazy loading/code splitting, cache-control/ETag ve immutable hashed asset politikasını uygula; eski chunk→yeni release failure testini yap.
4. React render bottleneck, layout thrash, long task ve memory leak için controlled before/after fixture kur; worker/cancellation çözümünü doğrula.
5. Slow network/CPU throttle, warm/cold cache, viewport ve repeated run koşullarını kaydet; tek ölçüm genel framework üstünlüğü kanıtı değildir.

## Planlanan dosyalar

- `labs/frontend/performance/`
- `docs/evidence/day-94/performance-report.md`
- `docs/evidence/day-94/` — sürüm/edition, exact komut, browser/runtime, fixture, expected/actual, ölçüm ve recovery.

Bunlar aday implementation çıktılarıdır; dosya/dependency varlığı Verified değildir.

## Commit sırası

1. `docs(day-94): frontend gereksinim ve sınırları tanımla`
2. `feat(day-94): temsilî UI ve eğitim profillerini uygula`
3. `test(day-94): browser contract hata ve toparlanmayı doğrula`
4. `docs(day-94): evidence runbook ve karşılaştırmayı kapat`

Mevcut verified uygulama yeterliyse aynı sorumluluğu tekrar kurma/boş feat commit üretme; actual SHA/evidence ve eksik testleri bağla. Green ürün profilleri ana app'in aynı state/build/controller kaynağına competing owner olmaz.

## Doğrulama ve kapanış

- [ ] Seçilmiş performance hipotezi aynı koşullarda önce/sonra ölçülür; invariant/UI davranışı korunur.
- [ ] Stale chunk/cache/private response ve memory cleanup testleri çalışır; field/lab sınırı raporlanır.
- [ ] Konu/product/blue etiketleri öğrenme + gerçek temsilî uygulama + runtime evidence ile veya explicit erişim gap'inde izleniyor.
- [ ] Değişen kod için uygun type/lint/unit/integration/build check; ardından gerçek browser/API/local runtime doğrulaması yapıldı.
- [ ] Accessibility, auth/privacy, cancellation/cleanup ve bounded resource davranışı ilgili use-case'te test edildi.
- [ ] Sürüm/lisans/compatibility gün başında doğrulanıp pin edildi; source maps/env/artifact secret sızdırmıyor.
- [ ] Local/managed provider, mock/real API ve CSR/SSR/SSG/PWA kanıtları ayrı raporlandı.
- [ ] Coverage actual duruma güncellendi; yalnız comparison veya static export SSR implementation sayılmadı.

Ücretli cloud/model API/hosting zorunluluğu yoktur; hesap/billing/remote deployment bugün yapılmaz. Local lab production SLA/scale, arama sıralaması veya mesleki unvan kanıtı değildir.
