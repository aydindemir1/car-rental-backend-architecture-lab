# Day 79 — Internet, semantic HTML ve erişilebilirlik temeli

Durum: **Planlandı**. Bu eğitim milestone'ı birden fazla takvim gününe yayılabilir. Kod/runtime evidence henüz oluşturulmadı.

## Önkoşul ve kapsam

[Day 78](day-78.md) kapanır; önceki birikimli implementation snapshot'ından `day/79` türetilir. Emlak repo/85 günlük planı değişmez. [Frontend ortak planı](../FRONTEND-ROADMAP-EXTENSION.md), [coverage matrisi](../coverage/frontend-coverage.md) ve [uygulama sözleşmesi](../coverage/mandatory-implementation-contract.md) esas alınır.

Desktop Apps/Mobile Apps ve ilgili native framework/runtime'lar kapsam dışıdır. Web PWA ve responsive browser deneyleri kapsamda kalır. Java/Spring business backend ve canonical veri sahipliği korunur.

## Öğrenme ve uygulama görevleri

Roadmap etiketleri: `Internet`, `How does the internet work?`, `What is HTTP?`, `What is Domain Name?`, `What is hosting?`, `DNS and how it works?`, `Browsers and how they work?`, `HTML`, `Accessibility`.

1. Day 02–04/52/68 internet, DNS, HTTP/TLS, hosting ve browser görevlerini kullan; araç arama sayfasının navigation→DNS→connection→response→DOM/CSSOM/layout/paint yolunu DevTools ile kaydet.
2. Semantic landmark/headings, link/button farkı, labelled form, input validation, table ve image alt metinlerini gerçek arama/teklif/iade ekranında uygula.
3. Keyboard-only navigation, focus order/visibility, zoom/reflow ve screen reader ile form/error/empty state'i doğrula. Otomatik accessibility taraması tek başına tam uygunluk kanıtı değildir.
4. Public katalog için title/meta/canonical/robots/sitemap ve SEO temelini ekle; authenticated/private sayfaları public index'e dahil etme. Local doğrulama arama motorunda sıralama garantisi değildir.

## Planlanan dosyalar

- `web/`
- `docs/frontend/browser-html-accessibility.md`
- `docs/evidence/day-79/` — sürüm/edition, exact komut, browser/runtime, fixture, expected/actual, ölçüm ve recovery.

Bunlar aday implementation çıktılarıdır; dosya/dependency varlığı Verified değildir.

## Commit sırası

1. `docs(day-79): frontend gereksinim ve sınırları tanımla`
2. `feat(day-79): temsilî UI ve eğitim profillerini uygula`
3. `test(day-79): browser contract hata ve toparlanmayı doğrula`
4. `docs(day-79): evidence runbook ve karşılaştırmayı kapat`

Mevcut verified uygulama yeterliyse aynı sorumluluğu tekrar kurma/boş feat commit üretme; actual SHA/evidence ve eksik testleri bağla. Green ürün profilleri ana app'in aynı state/build/controller kaynağına competing owner olmaz.

## Doğrulama ve kapanış

- [ ] Arama formu keyboard ve en az bir uygun screen reader akışında kullanılabilir; error doğru kontrolle ilişkilidir.
- [ ] Request/render waterfall ile semantik HTML ve private index/cache sınırı actual browser'da gözlenir.
- [ ] Konu/product/blue etiketleri öğrenme + gerçek temsilî uygulama + runtime evidence ile veya explicit erişim gap'inde izleniyor.
- [ ] Değişen kod için uygun type/lint/unit/integration/build check; ardından gerçek browser/API/local runtime doğrulaması yapıldı.
- [ ] Accessibility, auth/privacy, cancellation/cleanup ve bounded resource davranışı ilgili use-case'te test edildi.
- [ ] Sürüm/lisans/compatibility gün başında doğrulanıp pin edildi; source maps/env/artifact secret sızdırmıyor.
- [ ] Local/managed provider, mock/real API ve CSR/SSR/SSG/PWA kanıtları ayrı raporlandı.
- [ ] Coverage actual duruma güncellendi; yalnız comparison veya static export SSR implementation sayılmadı.

Ücretli cloud/model API/hosting zorunluluğu yoktur; hesap/billing/remote deployment bugün yapılmaz. Local lab production SLA/scale, arama sıralaması veya mesleki unvan kanıtı değildir.
