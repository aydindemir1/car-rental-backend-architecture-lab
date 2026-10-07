# Day 91 — Next.js ile gerçek SSR ve Node render sınırı

Durum: **Planlandı**. Bu eğitim milestone'ı birden fazla takvim gününe yayılabilir. Kod/runtime evidence henüz oluşturulmadı.

## Önkoşul ve kapsam

[Day 90](day-90.md) kapanır; önceki birikimli implementation snapshot'ından `day/91` türetilir. Emlak repo/85 günlük planı değişmez. [Frontend ortak planı](../FRONTEND-ROADMAP-EXTENSION.md), [coverage matrisi](../coverage/frontend-coverage.md) ve [uygulama sözleşmesi](../coverage/mandatory-implementation-contract.md) esas alınır.

Desktop Apps/Mobile Apps ve ilgili native framework/runtime'lar kapsam dışıdır. Web PWA ve responsive browser deneyleri kapsamda kalır. Java/Spring business backend ve canonical veri sahipliği korunur.

## Öğrenme ve uygulama görevleri

Roadmap etiketleri: `SSR`, `Next.js`, `Nodejs`.

1. Ana Day 06/45 CSR+statik portal korunur. İzole Next.js profilinde Java read API'dan request-time veriyle public vehicle detail SSR uygula; build-time static export SSR yerine geçmez.
2. Node.js process/env/module/HTTP lifecycle, event loop ve graceful shutdown konularını frontend renderer üzerinden öğren. Node business backend/Express/Nest veya datastore canonical owner eklenmez.
3. Initial response HTML, hydration, server/client component sınırı, loading/error ve streaming davranışını browser/network testleriyle göster.
4. Nginx reverse proxy arkasında local renderer çalıştır; proxy buffering, timeout ve shutdown etkisini test et. Framework rendering cache'i Java booking correctness kaynağı değildir.
5. Server-only credential/browser env boundary, private response cache ve iki kullanıcı izolasyonunu doğrula. Static export ile SSR'in deploy/runtime farkını ayrı not et.
6. Önceki Node.js backend eğitim istisnası korunur; Frontend talebinin Nodejs mavi konusuna scope'lu render görevi eklenmiştir. Linked Node roadmap'in tüm backend dalları otomatik scope olmaz.

## Planlanan dosyalar

- `labs/frontend/next-ssr/`
- `docs/architecture/frontend-rendering-boundary.md`
- `docs/evidence/day-91/` — sürüm/edition, exact komut, browser/runtime, fixture, expected/actual, ölçüm ve recovery.

Bunlar aday implementation çıktılarıdır; dosya/dependency varlığı Verified değildir.

## Commit sırası

1. `docs(day-91): frontend gereksinim ve sınırları tanımla`
2. `feat(day-91): temsilî UI ve eğitim profillerini uygula`
3. `test(day-91): browser contract hata ve toparlanmayı doğrula`
4. `docs(day-91): evidence runbook ve karşılaştırmayı kapat`

Mevcut verified uygulama yeterliyse aynı sorumluluğu tekrar kurma/boş feat commit üretme; actual SHA/evidence ve eksik testleri bağla. Green ürün profilleri ana app'in aynı state/build/controller kaynağına competing owner olmaz.

## Doğrulama ve kapanış

- [ ] Java read fixture request-time değişince SSR initial HTML değişir; JS kapalıyken public veri görünür.
- [ ] Hydration/streaming ve SSR failure/recovery gerçek runtime'da gözlenir; cross-user credential/cache sızıntısı yoktur.
- [ ] Konu/product/blue etiketleri öğrenme + gerçek temsilî uygulama + runtime evidence ile veya explicit erişim gap'inde izleniyor.
- [ ] Değişen kod için uygun type/lint/unit/integration/build check; ardından gerçek browser/API/local runtime doğrulaması yapıldı.
- [ ] Accessibility, auth/privacy, cancellation/cleanup ve bounded resource davranışı ilgili use-case'te test edildi.
- [ ] Sürüm/lisans/compatibility gün başında doğrulanıp pin edildi; source maps/env/artifact secret sızdırmıyor.
- [ ] Local/managed provider, mock/real API ve CSR/SSR/SSG/PWA kanıtları ayrı raporlandı.
- [ ] Coverage actual duruma güncellendi; yalnız comparison veya static export SSR implementation sayılmadı.

Ücretli cloud/model API/hosting zorunluluğu yoktur; hesap/billing/remote deployment bugün yapılmaz. Local lab production SLA/scale, arama sıralaması veya mesleki unvan kanıtı değildir.
