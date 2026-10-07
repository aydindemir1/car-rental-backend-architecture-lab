# Day 88 — Design System ve Web Components

Durum: **Planlandı**. Bu eğitim milestone'ı birden fazla takvim gününe yayılabilir. Kod/runtime evidence henüz oluşturulmadı.

## Önkoşul ve kapsam

[Day 87](day-87.md) kapanır; önceki birikimli implementation snapshot'ından `day/88` türetilir. Emlak repo/85 günlük planı değişmez. [Frontend ortak planı](../FRONTEND-ROADMAP-EXTENSION.md), [coverage matrisi](../coverage/frontend-coverage.md) ve [uygulama sözleşmesi](../coverage/mandatory-implementation-contract.md) esas alınır.

Desktop Apps/Mobile Apps ve ilgili native framework/runtime'lar kapsam dışıdır. Web PWA ve responsive browser deneyleri kapsamda kalır. Java/Spring business backend ve canonical veri sahipliği korunur.

## Öğrenme ve uygulama görevleri

Roadmap etiketleri: `Design Systems`, `Design System`, `Web Components`, `Custom Elements`, `HTML Templates`, `Shadow DOM`.

1. Typography/spacing/color/motion token'ları, semantic component API, variants ve controlled state sınırlarıyla küçük design system kur.
2. Button/input/dialog/feedback component'leri için keyboard, focus management, contrast ve screen reader sözleşmesi tanımla; accessibility failure fixture'ını düzelt.
3. Custom Element + HTML template + Shadow DOM ile bağımsız rental status badge veya inspection widget'ı gerçekten uygula; attribute/property/event ve lifecycle cleanup'ını göster.
4. React wrapper üzerinden component'i aynı sayfaya entegre et; style isolation, slot, composed event, form/accessibility ve SSR/hydration sınırlarını test et.
5. Local component package/version/deprecation ve visual regression koşullarını kaydet; farklı framework component API'lerini Day 97'de karşılaştır.

## Planlanan dosyalar

- `web/design-system/`
- `labs/frontend/web-components/`
- `docs/frontend/design-system-contracts.md`
- `docs/evidence/day-88/` — sürüm/edition, exact komut, browser/runtime, fixture, expected/actual, ölçüm ve recovery.

Bunlar aday implementation çıktılarıdır; dosya/dependency varlığı Verified değildir.

## Commit sırası

1. `docs(day-88): frontend gereksinim ve sınırları tanımla`
2. `feat(day-88): temsilî UI ve eğitim profillerini uygula`
3. `test(day-88): browser contract hata ve toparlanmayı doğrula`
4. `docs(day-88): evidence runbook ve karşılaştırmayı kapat`

Mevcut verified uygulama yeterliyse aynı sorumluluğu tekrar kurma/boş feat commit üretme; actual SHA/evidence ve eksik testleri bağla. Green ürün profilleri ana app'in aynı state/build/controller kaynağına competing owner olmaz.

## Doğrulama ve kapanış

- [ ] Design system component'leri keyboard/screen reader testine sahiptir.
- [ ] Web Component template/shadow/style/event/lifecycle davranışı gerçek React browser integration'da çalışır.
- [ ] Konu/product/blue etiketleri öğrenme + gerçek temsilî uygulama + runtime evidence ile veya explicit erişim gap'inde izleniyor.
- [ ] Değişen kod için uygun type/lint/unit/integration/build check; ardından gerçek browser/API/local runtime doğrulaması yapıldı.
- [ ] Accessibility, auth/privacy, cancellation/cleanup ve bounded resource davranışı ilgili use-case'te test edildi.
- [ ] Sürüm/lisans/compatibility gün başında doğrulanıp pin edildi; source maps/env/artifact secret sızdırmıyor.
- [ ] Local/managed provider, mock/real API ve CSR/SSR/SSG/PWA kanıtları ayrı raporlandı.
- [ ] Coverage gerçek duruma güncellendi; yalnız comparison veya static export SSR implementation sayılmadı.

Ücretli cloud/model API/hosting zorunluluğu yoktur; hesap/billing/remote deployment bugün yapılmaz. Local lab production SLA/scale, arama sıralaması veya mesleki unvan kanıtı değildir.


## Design System explicit genişleme ile ilişki

Bu gün token/temel component/Web Components foundation'ıdır; [Design System kapsamının](../coverage/design-system-coverage.md) tamamını tek başına bitirmez. Yeni [Day132–143 programı](../DESIGN-SYSTEM-ROADMAP-EXTENSION.md) visual audit, design language/brand/microcopy, geniş token/typography/iconography,20 core component, Storybook/test/release, local Penpot editor/plugin, pilot/UX/regional/A-B ve governance/adoption/communication çalışmalarını tamamlar. Bu gün doğrulanmış kanıt üretirse sonraki günler aynı component'i yeniden kurmak yerine SHA/test/browser kanıtını bağlar. Canonical token kaynağı ve artifact/version sınırı korunur; native app veya Node business backend scope'u yeniden açılmaz.
