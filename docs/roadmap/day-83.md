# Day 83 — React uygulama mimarisi ve route/state tasarımı

Durum: **Planlandı**. Bu eğitim milestone'ı birden fazla takvim gününe yayılabilir. Kod/runtime evidence henüz oluşturulmadı.

## Önkoşul ve kapsam

[Day 82](day-82.md) kapanır; önceki birikimli implementation snapshot'ından `day/83` türetilir. Emlak repo/85 günlük planı değişmez. [Frontend ortak planı](../FRONTEND-ROADMAP-EXTENSION.md), [coverage matrisi](../coverage/frontend-coverage.md) ve [uygulama sözleşmesi](../coverage/mandatory-implementation-contract.md) esas alınır.

Desktop Apps/Mobile Apps ve ilgili native framework/runtime'lar kapsam dışıdır. Web PWA ve responsive browser deneyleri kapsamda kalır. Java/Spring business backend ve canonical veri sahipliği korunur.

## Öğrenme ve uygulama görevleri

Roadmap etiketleri: `Learn a Framework`, `React`, `react-router`.

1. Day 06 React portalını feature/component/hooks/data adapter sınırlarıyla düzenle; canonical state Java backend'de kalır.
2. React Router ile search/detail/booking route'ları, nested layout, navigation/error boundary ve URL state uygula.
3. Controlled form, validation, loading/error/empty, stale request cancellation ve server state cache için TanStack Query gibi seçilmiş tek yaklaşımı kullan.
4. UI state/server state ayrımı, effect lifecycle, stable keys ve render davranışını gerçek form/list üzerinden test et; gereksiz global store ekleme.
5. Keyboard focus, route transition ve authorized/unauthorized UI testlerini yap; client route guard backend authorization yerine geçmez.

## Planlanan dosyalar

- `web/features/`
- `docs/frontend/component-and-state-boundaries.md`
- `docs/evidence/day-83/` — sürüm/edition, exact komut, browser/runtime, fixture, expected/actual, ölçüm ve recovery.

Bunlar aday implementation çıktılarıdır; dosya/dependency varlığı Verified değildir.

## Commit sırası

1. `docs(day-83): frontend gereksinim ve sınırları tanımla`
2. `feat(day-83): temsilî UI ve eğitim profillerini uygula`
3. `test(day-83): browser contract hata ve toparlanmayı doğrula`
4. `docs(day-83): evidence runbook ve karşılaştırmayı kapat`

Mevcut verified uygulama yeterliyse aynı sorumluluğu tekrar kurma/boş feat commit üretme; actual SHA/evidence ve eksik testleri bağla. Green ürün profilleri ana app'in aynı state/build/controller kaynağına competing owner olmaz.

## Doğrulama ve kapanış

- [ ] Deep link/back/forward ve hızlı filtre değişimi tutarlı state üretir.
- [ ] Route/error/unmount ve yetkisiz akışlarda resource cleanup ve backend authorization korunur.
- [ ] Konu/product/blue etiketleri öğrenme + gerçek temsilî uygulama + runtime evidence ile veya explicit erişim gap'inde izleniyor.
- [ ] Değişen kod için uygun type/lint/unit/integration/build check; ardından gerçek browser/API/local runtime doğrulaması yapıldı.
- [ ] Accessibility, auth/privacy, cancellation/cleanup ve bounded resource davranışı ilgili use-case'te test edildi.
- [ ] Sürüm/lisans/compatibility gün başında doğrulanıp pin edildi; source maps/env/artifact secret sızdırmıyor.
- [ ] Local/managed provider, mock/real API ve CSR/SSR/SSG/PWA kanıtları ayrı raporlandı.
- [ ] Coverage actual duruma güncellendi; yalnız comparison veya static export SSR implementation sayılmadı.

Ücretli cloud/model API/hosting zorunluluğu yoktur; hesap/billing/remote deployment bugün yapılmaz. Local lab production SLA/scale, arama sıralaması veya mesleki unvan kanıtı değildir.
