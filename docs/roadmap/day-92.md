# Day 92 — TanStack Start ile SSR/streaming karşılaştırması

Durum: **Planlandı**. Bu eğitim milestone'ı birden fazla takvim gününe yayılabilir. Kod/runtime evidence henüz oluşturulmadı.

## Önkoşul ve kapsam

[Day 91](day-91.md) kapanır; önceki birikimli implementation snapshot'ından `day/92` türetilir. Emlak repo/85 günlük planı değişmez. [Frontend ortak planı](../FRONTEND-ROADMAP-EXTENSION.md), [coverage matrisi](../coverage/frontend-coverage.md) ve [uygulama sözleşmesi](../coverage/mandatory-implementation-contract.md) esas alınır.

Desktop Apps/Mobile Apps ve ilgili native framework/runtime'lar kapsam dışıdır. Web PWA ve responsive browser deneyleri kapsamda kalır. Java/Spring business backend ve canonical veri sahipliği korunur.

## Öğrenme ve uygulama görevleri

Roadmap etiketleri: `Tanstack Start`, `Streamed Responses`.

1. Mor TanStack Start için ayrı React SSR profili kur; aynı Java read API ve public detail fixture'ını kullan. Next ve TanStack aynı route'un iki aktif renderer owner'ı olmaz.
2. Typed routing/loader, request-scoped query cache ve hydration dehydrate/re-hydrate sınırını uygula.
3. Streamed response, cancellation, dependency timeout ve partial shell/error davranışını gerçek browser'da test et; proxy buffering'i Day 91 ile aynı koşullarda incele.
4. Framework server function gerekiyorsa yalnız presentation/read composition rolünde kullan; canonical booking mutation ve business validation Java'da kalır.
5. Version/security/compatibility ve build/runtime kaynak bütçesini kaydet; SSR, RSC, SSG ve streaming birbirinin eşanlamlısı değildir.

## Planlanan dosyalar

- `labs/frontend/tanstack-start/`
- `docs/technology/react-ssr-framework-comparison.md`
- `docs/evidence/day-92/` — sürüm/edition, exact komut, browser/runtime, fixture, expected/actual, ölçüm ve recovery.

Bunlar aday implementation çıktılarıdır; dosya/dependency varlığı Verified değildir.

## Commit sırası

1. `docs(day-92): frontend gereksinim ve sınırları tanımla`
2. `feat(day-92): temsilî UI ve eğitim profillerini uygula`
3. `test(day-92): browser contract hata ve toparlanmayı doğrula`
4. `docs(day-92): evidence runbook ve karşılaştırmayı kapat`

Mevcut verified uygulama yeterliyse aynı sorumluluğu tekrar kurma/boş feat commit üretme; actual SHA/evidence ve eksik testleri bağla. Green ürün profilleri ana app'in aynı state/build/controller kaynağına competing owner olmaz.

## Doğrulama ve kapanış

- [ ] TanStack Start initial HTML/hydration/request-time read gerçek runtime'da çalışır.
- [ ] Client disconnect/upstream error sonrası renderer cleanup olur; streaming beklenen zaman/byte davranışını gösterir.
- [ ] Konu/product/blue etiketleri öğrenme + gerçek temsilî uygulama + runtime evidence ile veya explicit erişim gap'inde izleniyor.
- [ ] Değişen kod için uygun type/lint/unit/integration/build check; ardından gerçek browser/API/local runtime doğrulaması yapıldı.
- [ ] Accessibility, auth/privacy, cancellation/cleanup ve bounded resource davranışı ilgili use-case'te test edildi.
- [ ] Sürüm/lisans/compatibility gün başında doğrulanıp pin edildi; source maps/env/artifact secret sızdırmıyor.
- [ ] Local/managed provider, mock/real API ve CSR/SSR/SSG/PWA kanıtları ayrı raporlandı.
- [ ] Coverage actual duruma güncellendi; yalnız comparison veya static export SSR implementation sayılmadı.

Ücretli cloud/model API/hosting zorunluluğu yoktur; hesap/billing/remote deployment bugün yapılmaz. Local lab production SLA/scale, arama sıralaması veya mesleki unvan kanıtı değildir.
