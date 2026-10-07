# Day 90 — GraphQL: Apollo ve Relay Modern

Durum: **Planlandı**. Bu eğitim milestone'ı birden fazla takvim gününe yayılabilir. Kod/runtime evidence henüz oluşturulmadı.

## Önkoşul ve kapsam

[Day 89](day-89.md) kapanır; önceki birikimli implementation snapshot'ından `day/90` türetilir. Emlak repo/85 günlük planı değişmez. [Frontend ortak planı](../FRONTEND-ROADMAP-EXTENSION.md), [coverage matrisi](../coverage/frontend-coverage.md) ve [uygulama sözleşmesi](../coverage/mandatory-implementation-contract.md) esas alınır.

Desktop Apps/Mobile Apps ve ilgili native framework/runtime'lar kapsam dışıdır. Web PWA ve responsive browser deneyleri kapsamda kalır. Java/Spring business backend ve canonical veri sahipliği korunur.

## Öğrenme ve uygulama görevleri

Roadmap etiketleri: `GraphQL`, `Apollo`, `Relay Modern`.

1. Mevcut araç Day 38 GraphQL Java read API'sini Apollo Client ile gerçek search/detail UI'ına bağla; pagination, variables, normalized cache ve error/loading state uygula.
2. Auth propagation, query cost, stale entity/update invalidation ve partial data/error contract'ını test et. Booking canonical write API'si Java owner'da kalır.
3. Yeşil Relay Modern için ayrı bounded read fixture ve compile-time query artifact'ları kur; gerekli node ID/connection/pagination read contract'ını Java adapter'da uygula.
4. Apollo/Relay aynı ana UI state cache'inin competing sahibi olmaz; ayrı profile kullan. Schema drift/generated type, forbidden field ve malformed response testlerini yap.
5. REST/gRPC/GraphQL modellerini bandwidth/fan-out ve owner boundary üzerinden karşılaştır; GraphQL her frontend isteği için zorunlu değildir.

## Planlanan dosyalar

- `web/features/graphql/`
- `labs/frontend/relay/`
- `docs/frontend/graphql-client-contracts.md`
- `docs/evidence/day-90/` — sürüm/edition, exact komut, browser/runtime, fixture, expected/actual, ölçüm ve recovery.

Bunlar aday implementation çıktılarıdır; dosya/dependency varlığı Verified değildir.

## Commit sırası

1. `docs(day-90): frontend gereksinim ve sınırları tanımla`
2. `feat(day-90): temsilî UI ve eğitim profillerini uygula`
3. `test(day-90): browser contract hata ve toparlanmayı doğrula`
4. `docs(day-90): evidence runbook ve karşılaştırmayı kapat`

Mevcut verified uygulama yeterliyse aynı sorumluluğu tekrar kurma/boş feat commit üretme; actual SHA/evidence ve eksik testleri bağla. Green ürün profilleri ana app'in aynı state/build/controller kaynağına competing owner olmaz.

## Doğrulama ve kapanış

- [ ] Apollo pagination/cache/auth ve server error gerçek Java API'da doğrulanır.
- [ ] Relay compiler/read UI runtime ve schema drift gate'i actual evidence'a sahiptir.
- [ ] Konu/product/blue etiketleri öğrenme + gerçek temsilî uygulama + runtime evidence ile veya explicit erişim gap'inde izleniyor.
- [ ] Değişen kod için uygun type/lint/unit/integration/build check; ardından gerçek browser/API/local runtime doğrulaması yapıldı.
- [ ] Accessibility, auth/privacy, cancellation/cleanup ve bounded resource davranışı ilgili use-case'te test edildi.
- [ ] Sürüm/lisans/compatibility gün başında doğrulanıp pin edildi; source maps/env/artifact secret sızdırmıyor.
- [ ] Local/managed provider, mock/real API ve CSR/SSR/SSG/PWA kanıtları ayrı raporlandı.
- [ ] Coverage actual duruma güncellendi; yalnız comparison veya static export SSR implementation sayılmadı.

Ücretli cloud/model API/hosting zorunluluğu yoktur; hesap/billing/remote deployment bugün yapılmaz. Local lab production SLA/scale, arama sıralaması veya mesleki unvan kanıtı değildir.
