# Day 85 — Vite, esbuild ve bundler/compiler lab'ı

Durum: **Planlandı**. Bu eğitim milestone'ı birden fazla takvim gününe yayılabilir. Kod/runtime evidence henüz oluşturulmadı.

## Önkoşul ve kapsam

[Day 84](day-84.md) kapanır; önceki birikimli implementation snapshot'ından `day/85` türetilir. Emlak repo/85 günlük planı değişmez. [Frontend ortak planı](../FRONTEND-ROADMAP-EXTENSION.md), [coverage matrisi](../coverage/frontend-coverage.md) ve [uygulama sözleşmesi](../coverage/mandatory-implementation-contract.md) esas alınır.

Desktop Apps/Mobile Apps ve ilgili native framework/runtime'lar kapsam dışıdır. Web PWA ve responsive browser deneyleri kapsamda kalır. Java/Spring business backend ve canonical veri sahipliği korunur.

## Öğrenme ve uygulama görevleri

Roadmap etiketleri: `Module Bundlers`, `Vite`, `esbuild`, `Parcel`, `Rollup`, `SWC`, `Rolldown`.

1. Vite production build/dev server, code splitting, asset hashing, source map ve environment boundary görevlerini ana React UI'da uygula.
2. Mor esbuild için doğrudan CLI/API ile ayrı TypeScript/browser fixture'ını gerçekten bundle et; Vite dependency'si var diye esbuild kullanıldı sayma.
3. Vite 8 Rolldown/Oxc tabanı nedeniyle seçilmiş sürümün actual bundler/compiler'ını doğrula. Green/tiksiz Rolldown direct fixture veya Vite actual output/config üzerinden evidence'a bağlanır; eski esbuild/Rollup varsayımı taşınmaz.
4. Yeşil Rollup ve Parcel'de aynı bounded fixture build'ini; SWC'de TS/JS transform deneyini çalıştır. Transpilation, type checking ve bundling farklı sorumluluklardır.
5. Dynamic import/chunk miss, unsupported syntax ve source-map disclosure testlerini yap; bütün bundler'lar main uygulamada aynı anda owner olmaz.

## Planlanan dosyalar

- `labs/frontend/build-tools/`
- `docs/technology/frontend-build-tool-comparison.md`
- `docs/evidence/day-85/` — sürüm/edition, exact komut, browser/runtime, fixture, expected/actual, ölçüm ve recovery.

Bunlar aday implementation çıktılarıdır; dosya/dependency varlığı Verified değildir.

## Commit sırası

1. `docs(day-85): frontend gereksinim ve sınırları tanımla`
2. `feat(day-85): temsilî UI ve eğitim profillerini uygula`
3. `test(day-85): browser contract hata ve toparlanmayı doğrula`
4. `docs(day-85): evidence runbook ve karşılaştırmayı kapat`

Mevcut verified uygulama yeterliyse aynı sorumluluğu tekrar kurma/boş feat commit üretme; actual SHA/evidence ve eksik testleri bağla. Green ürün profilleri ana app'in aynı state/build/controller kaynağına competing owner olmaz.

## Doğrulama ve kapanış

- [ ] Her seçilmiş araç için gerçek transform/bundle artifact ve browser runtime sonucu vardır.
- [ ] Broken chunk/env/source-map ve incompatible config testleri kontrollü hata üretir; build ölçüm koşulları sabittir.
- [ ] Konu/product/blue etiketleri öğrenme + gerçek temsilî uygulama + runtime evidence ile veya explicit erişim gap'inde izleniyor.
- [ ] Değişen kod için uygun type/lint/unit/integration/build check; ardından gerçek browser/API/local runtime doğrulaması yapıldı.
- [ ] Accessibility, auth/privacy, cancellation/cleanup ve bounded resource davranışı ilgili use-case'te test edildi.
- [ ] Sürüm/lisans/compatibility gün başında doğrulanıp pin edildi; source maps/env/artifact secret sızdırmıyor.
- [ ] Local/managed provider, mock/real API ve CSR/SSR/SSG/PWA kanıtları ayrı raporlandı.
- [ ] Coverage actual duruma güncellendi; yalnız comparison veya static export SSR implementation sayılmadı.

Ücretli cloud/model API/hosting zorunluluğu yoktur; hesap/billing/remote deployment bugün yapılmaz. Local lab production SLA/scale, arama sıralaması veya mesleki unvan kanıtı değildir.
