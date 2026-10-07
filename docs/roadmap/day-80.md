# Day 80 — CSS, responsive layout ve Tailwind

Durum: **Planlandı**. Bu eğitim milestone'ı birden fazla takvim gününe yayılabilir. Kod/runtime evidence henüz oluşturulmadı.

## Önkoşul ve kapsam

[Day 79](day-79.md) kapanır; önceki birikimli implementation snapshot'ından `day/80` türetilir. Emlak repo/85 günlük planı değişmez. [Frontend ortak planı](../FRONTEND-ROADMAP-EXTENSION.md), [coverage matrisi](../coverage/frontend-coverage.md) ve [uygulama sözleşmesi](../coverage/mandatory-implementation-contract.md) esas alınır.

Desktop Apps/Mobile Apps ve ilgili native framework/runtime'lar kapsam dışıdır. Web PWA ve responsive browser deneyleri kapsamda kalır. Java/Spring business backend ve canonical veri sahipliği korunur.

## Öğrenme ve uygulama görevleri

Roadmap etiketleri: `CSS`, `CSS Frameworks`, `Tailwind`.

1. Day 05 Tailwind/CSS görevlerini genişlet: cascade/specificity/inheritance, box model, flex/grid, positioning ve overflow'u kontrollü layout fixture'larında uygula.
2. Responsive catalog/filter/detail ve teslim ekranını viewport, container ölçüsü, typography, spacing, renk/contrast token'larıyla kur.
3. Reduced-motion, hover/focus/touch ve browser uyumluluğunu test et; minimum viewport'ta içerik/klavye erişimi kaybolmasın.
4. Tailwind build/purge/safelisting ihtiyacını seçilmiş sürümde doğrula; plain CSS ile aynı component'in bounded alternatifini karşılaştır. İkinci kalıcı styling owner kurma.

## Planlanan dosyalar

- `web/styles/`
- `labs/frontend/css-layout/`
- `docs/evidence/day-80/` — sürüm/edition, exact komut, browser/runtime, fixture, expected/actual, ölçüm ve recovery.

Bunlar aday implementation çıktılarıdır; dosya/dependency varlığı Verified değildir.

## Commit sırası

1. `docs(day-80): frontend gereksinim ve sınırları tanımla`
2. `feat(day-80): temsilî UI ve eğitim profillerini uygula`
3. `test(day-80): browser contract hata ve toparlanmayı doğrula`
4. `docs(day-80): evidence runbook ve karşılaştırmayı kapat`

Mevcut verified uygulama yeterliyse aynı sorumluluğu tekrar kurma/boş feat commit üretme; actual SHA/evidence ve eksik testleri bağla. Green ürün profilleri ana app'in aynı state/build/controller kaynağına competing owner olmaz.

## Doğrulama ve kapanış

- [ ] Dar/geniş viewport, zoom, uzun Türkçe metin ve keyboard focus'ta layout kullanılabilir.
- [ ] CSS production build beklenen sınıfları korur; gereksiz CSS ve contrast sorunları ölçülür.
- [ ] Konu/product/blue etiketleri öğrenme + gerçek temsilî uygulama + runtime evidence ile veya explicit erişim gap'inde izleniyor.
- [ ] Değişen kod için uygun type/lint/unit/integration/build check; ardından gerçek browser/API/local runtime doğrulaması yapıldı.
- [ ] Accessibility, auth/privacy, cancellation/cleanup ve bounded resource davranışı ilgili use-case'te test edildi.
- [ ] Sürüm/lisans/compatibility gün başında doğrulanıp pin edildi; source maps/env/artifact secret sızdırmıyor.
- [ ] Local/managed provider, mock/real API ve CSR/SSR/SSG/PWA kanıtları ayrı raporlandı.
- [ ] Coverage actual duruma güncellendi; yalnız comparison veya static export SSR implementation sayılmadı.

Ücretli cloud/model API/hosting zorunluluğu yoktur; hesap/billing/remote deployment bugün yapılmaz. Local lab production SLA/scale, arama sıralaması veya mesleki unvan kanıtı değildir.
