# Day 81 — JavaScript ve browser Web APIs

Durum: **Planlandı**. Bu eğitim milestone'ı birden fazla takvim gününe yayılabilir. Kod/runtime evidence henüz oluşturulmadı.

## Önkoşul ve kapsam

[Day 80](day-80.md) kapanır; önceki birikimli implementation snapshot'ından `day/81` türetilir. Emlak repo/85 günlük planı değişmez. [Frontend ortak planı](../FRONTEND-ROADMAP-EXTENSION.md), [coverage matrisi](../coverage/frontend-coverage.md) ve [uygulama sözleşmesi](../coverage/mandatory-implementation-contract.md) esas alınır.

Desktop Apps/Mobile Apps ve ilgili native framework/runtime'lar kapsam dışıdır. Web PWA ve responsive browser deneyleri kapsamda kalır. Java/Spring business backend ve canonical veri sahipliği korunur.

## Öğrenme ve uygulama görevleri

Roadmap etiketleri: `JavaScript`, `Web APIs`.

1. Scope/closure, module, event loop/microtask, promise/async ve DOM event delegation'ı küçük gerçek filtre/form davranışında uygula; event cleanup ve duplicate listener riskini göster.
2. Fetch + AbortController ile stale arama sonucunu engelle; error/timeout/cancel response'larını ayır. URL/history ve browser navigation durumunu filtrelerle senkronize et.
3. Storage/IndexedDB'yi yalnız sahte offline taslak için kullan; credential veya canonical booking state'i browser storage'a taşınmaz.
4. Intersection/ResizeObserver ve Web Worker gibi Web APIs için en az bir gerçek kullanım kur: görünürlük/lazy render ve ağır non-critical fixture hesabı. Feature detection/fallback/worker cleanup yap.
5. Browser izinleri ve API availability farklarını test et; gereksiz device/location erişimi isteme.

## Planlanan dosyalar

- `labs/frontend/javascript-web-apis/`
- `web/features/search/`
- `docs/evidence/day-81/` — sürüm/edition, exact komut, browser/runtime, fixture, expected/actual, ölçüm ve recovery.

Bunlar aday implementation çıktılarıdır; dosya/dependency varlığı Verified değildir.

## Commit sırası

1. `docs(day-81): frontend gereksinim ve sınırları tanımla`
2. `feat(day-81): temsilî UI ve eğitim profillerini uygula`
3. `test(day-81): browser contract hata ve toparlanmayı doğrula`
4. `docs(day-81): evidence runbook ve karşılaştırmayı kapat`

Mevcut verified uygulama yeterliyse aynı sorumluluğu tekrar kurma/boş feat commit üretme; actual SHA/evidence ve eksik testleri bağla. Green ürün profilleri ana app'in aynı state/build/controller kaynağına competing owner olmaz.

## Doğrulama ve kapanış

- [ ] Eski/cancelled request yeni UI sonucunu ezmez; event/observer/worker unmount sonrası temizlenir.
- [ ] Storage quota/permission/unsupported API ve offline durumunda kontrollü fallback vardır.
- [ ] Konu/product/blue etiketleri öğrenme + gerçek temsilî uygulama + runtime evidence ile veya explicit erişim gap'inde izleniyor.
- [ ] Değişen kod için uygun type/lint/unit/integration/build check; ardından gerçek browser/API/local runtime doğrulaması yapıldı.
- [ ] Accessibility, auth/privacy, cancellation/cleanup ve bounded resource davranışı ilgili use-case'te test edildi.
- [ ] Sürüm/lisans/compatibility gün başında doğrulanıp pin edildi; source maps/env/artifact secret sızdırmıyor.
- [ ] Local/managed provider, mock/real API ve CSR/SSR/SSG/PWA kanıtları ayrı raporlandı.
- [ ] Coverage actual duruma güncellendi; yalnız comparison veya static export SSR implementation sayılmadı.

Ücretli cloud/model API/hosting zorunluluğu yoktur; hesap/billing/remote deployment bugün yapılmaz. Local lab production SLA/scale, arama sıralaması veya mesleki unvan kanıtı değildir.
