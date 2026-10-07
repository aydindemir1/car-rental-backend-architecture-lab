# Day 93 — Astro, SSG ve statik içerik modelleri

Durum: **Planlandı**. Bu eğitim milestone'ı birden fazla takvim gününe yayılabilir. Kod/runtime evidence henüz oluşturulmadı.

## Önkoşul ve kapsam

[Day 92](day-92.md) kapanır; önceki birikimli implementation snapshot'ından `day/93` türetilir. Emlak repo/85 günlük planı değişmez. [Frontend ortak planı](../FRONTEND-ROADMAP-EXTENSION.md), [coverage matrisi](../coverage/frontend-coverage.md) ve [uygulama sözleşmesi](../coverage/mandatory-implementation-contract.md) esas alınır.

Desktop Apps/Mobile Apps ve ilgili native framework/runtime'lar kapsam dışıdır. Web PWA ve responsive browser deneyleri kapsamda kalır. Java/Spring business backend ve canonical veri sahipliği korunur.

## Öğrenme ve uygulama görevleri

Roadmap etiketleri: `SSG`, `Astro`, `Vuepress`, `Eleventy`.

1. Astro ile public şube/araç rehberi veya kullanım dokümanı build-time generate et; islands/client hydration gereken alanları seç.
2. Day 91 Next.js profilinde ayrı static export config/fixture ile SSG davranışını gerçekten karşılaştır; static artifact Nginx'ten sunulsun.
3. Yeşil Eleventy ve VuePress için küçük aynı içerik fixture'ını ayrı output dizinlerinde generate/serve et; local build source/output/version evidence'ı kaydet.
4. Metadata/sitemap/robots, internal link, missing route ve asset base-path testlerini uygula. Generated content stale olabilir; public içerik freshness/yeniden build sorumluluğunu yaz.
5. SSG private booking/kimlik bilgisi üretmesin; static içerik Java backend'in güncel fiyat/availability kararı yerine geçmez.

6. Astro'nun SSR alternatif occurrence'ı için ayrı uyumlu local Node adapter profilinde Java read API'dan request-time HTML üret; Astro SSG output'u tek başına Astro SSR evidence değildir.

## Planlanan dosyalar

- `labs/frontend/static-generation/`
- `docs/frontend/rendering-model-comparison.md`
- `docs/evidence/day-93/` — sürüm/edition, exact komut, browser/runtime, fixture, expected/actual, ölçüm ve recovery.

Bunlar aday implementation çıktılarıdır; dosya/dependency varlığı Verified değildir.

## Commit sırası

1. `docs(day-93): frontend gereksinim ve sınırları tanımla`
2. `feat(day-93): temsilî UI ve eğitim profillerini uygula`
3. `test(day-93): browser contract hata ve toparlanmayı doğrula`
4. `docs(day-93): evidence runbook ve karşılaştırmayı kapat`

Mevcut verified uygulama yeterliyse aynı sorumluluğu tekrar kurma/boş feat commit üretme; actual SHA/evidence ve eksik testleri bağla. Green ürün profilleri ana app'in aynı state/build/controller kaynağına competing owner olmaz.

## Doğrulama ve kapanış

- [ ] Astro/Next export/Eleventy/VuePress artifact'ı clean build ve local web server'da çalışır.
- [ ] Build sonrası API verisi değişince statik içerik otomatik güncelmiş gibi davranmaz; private veri artifact'a girmez.
- [ ] Konu/product/blue etiketleri öğrenme + gerçek temsilî uygulama + runtime evidence ile veya explicit erişim gap'inde izleniyor.
- [ ] Değişen kod için uygun type/lint/unit/integration/build check; ardından gerçek browser/API/local runtime doğrulaması yapıldı.
- [ ] Accessibility, auth/privacy, cancellation/cleanup ve bounded resource davranışı ilgili use-case'te test edildi.
- [ ] Sürüm/lisans/compatibility gün başında doğrulanıp pin edildi; source maps/env/artifact secret sızdırmıyor.
- [ ] Local/managed provider, mock/real API ve CSR/SSR/SSG/PWA kanıtları ayrı raporlandı.
- [ ] Coverage actual duruma güncellendi; yalnız comparison veya static export SSR implementation sayılmadı.

Ücretli cloud/model API/hosting zorunluluğu yoktur; hesap/billing/remote deployment bugün yapılmaz. Local lab production SLA/scale, arama sıralaması veya mesleki unvan kanıtı değildir.
