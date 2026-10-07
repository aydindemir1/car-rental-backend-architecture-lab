# Day 84 — npm, pnpm, yarn ve Bun paket deneyleri

Durum: **Planlandı**. Bu eğitim milestone'ı birden fazla takvim gününe yayılabilir. Kod/runtime evidence henüz oluşturulmadı.

## Önkoşul ve kapsam

[Day 83](day-83.md) kapanır; önceki birikimli implementation snapshot'ından `day/84` türetilir. Emlak repo/85 günlük planı değişmez. [Frontend ortak planı](../FRONTEND-ROADMAP-EXTENSION.md), [coverage matrisi](../coverage/frontend-coverage.md) ve [uygulama sözleşmesi](../coverage/mandatory-implementation-contract.md) esas alınır.

Desktop Apps/Mobile Apps ve ilgili native framework/runtime'lar kapsam dışıdır. Web PWA ve responsive browser deneyleri kapsamda kalır. Java/Spring business backend ve canonical veri sahipliği korunur.

## Öğrenme ve uygulama görevleri

Roadmap etiketleri: `Package Managers`, `npm`, `pnpm`, `yarn`, `Bun`, `Version Control`, `Git`, `VCS Hosting`, `GitHub`, `GitLab`.

1. Day 06 npm, Day 07 Git/GitHub ve Day 69 local GitLab görevlerini evidence ile kullan; lockfile/script/lifecycle/dependency/license kararlarını doğrula.
2. Aynı küçük UI fixture'ını ayrı çalışma dizinlerinde npm, pnpm ve yarn ile clean install/build/test et; lockfile'ları aynı app'in aktif owner'ı yapma.
3. Yeşil Bun için izole package/build tooling profili uygula; lifecycle/dependency/Node compatibility farkını ölç. Ana backend Bun/Node'a taşınmaz.
4. Lock mismatch, transitive dependency, install script trust ve offline/cache miss senaryolarını test et. Hız ölçümünde warm/cold cache koşullarını yaz.
5. Canonical frontend package manager npm kalır; farklı ürünlerin temiz checkout sonuçlarını ve migration maliyetini Git diff/PR incelemesine bağla.

## Planlanan dosyalar

- `labs/frontend/package-managers/`
- `docs/technology/frontend-package-manager-comparison.md`
- `docs/evidence/day-84/` — sürüm/edition, exact komut, browser/runtime, fixture, expected/actual, ölçüm ve recovery.

Bunlar aday implementation çıktılarıdır; dosya/dependency varlığı Verified değildir.

## Commit sırası

1. `docs(day-84): frontend gereksinim ve sınırları tanımla`
2. `feat(day-84): temsilî UI ve eğitim profillerini uygula`
3. `test(day-84): browser contract hata ve toparlanmayı doğrula`
4. `docs(day-84): evidence runbook ve karşılaştırmayı kapat`

Mevcut verified uygulama yeterliyse aynı sorumluluğu tekrar kurma/boş feat commit üretme; actual SHA/evidence ve eksik testleri bağla. Green ürün profilleri ana app'in aynı state/build/controller kaynağına competing owner olmaz.

## Doğrulama ve kapanış

- [ ] Dört uygun profil fixture'ı build eder veya explicit compatibility gap kaydeder; geçerli lockfile ve clean install testlidir.
- [ ] Hatalı lock/dependency CI gate'ini kırar; secret veya generated dependency tree Git'e taşınmaz.
- [ ] Konu/product/blue etiketleri öğrenme + gerçek temsilî uygulama + runtime evidence ile veya explicit erişim gap'inde izleniyor.
- [ ] Değişen kod için uygun type/lint/unit/integration/build check; ardından gerçek browser/API/local runtime doğrulaması yapıldı.
- [ ] Accessibility, auth/privacy, cancellation/cleanup ve bounded resource davranışı ilgili use-case'te test edildi.
- [ ] Sürüm/lisans/compatibility gün başında doğrulanıp pin edildi; source maps/env/artifact secret sızdırmıyor.
- [ ] Local/managed provider, mock/real API ve CSR/SSR/SSG/PWA kanıtları ayrı raporlandı.
- [ ] Coverage actual duruma güncellendi; yalnız comparison veya static export SSR implementation sayılmadı.

Ücretli cloud/model API/hosting zorunluluğu yoktur; hesap/billing/remote deployment bugün yapılmaz. Local lab production SLA/scale, arama sıralaması veya mesleki unvan kanıtı değildir.
