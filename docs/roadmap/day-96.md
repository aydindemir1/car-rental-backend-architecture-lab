# Day 96 — Frontend deployment ve hosting kapsamı

Durum: **Planlandı**. Bu eğitim milestone'ı birden fazla takvim gününe yayılabilir. Kod/runtime evidence henüz oluşturulmadı.

## Önkoşul ve kapsam

[Day 95](day-95.md) kapanır; önceki birikimli implementation snapshot'ından `day/96` türetilir. Emlak repo/85 günlük planı değişmez. [Frontend ortak planı](../FRONTEND-ROADMAP-EXTENSION.md), [coverage matrisi](../coverage/frontend-coverage.md) ve [uygulama sözleşmesi](../coverage/mandatory-implementation-contract.md) esas alınır.

Desktop Apps/Mobile Apps ve ilgili native framework/runtime'lar kapsam dışıdır. Web PWA ve responsive browser deneyleri kapsamda kalır. Java/Spring business backend ve canonical veri sahipliği korunur.

## Öğrenme ve uygulama görevleri

Roadmap etiketleri: `Deployment`, `GitHub Pages`, `Cloudflare`.

1. Day 14/52/77 local Nginx/Docker/CI release zincirini frontend CSR/SSG ve local SSR profillerine bağla; hash/digest/build-once promotion korunur.
2. Mor GitHub Pages için küçük sahte public SSG docs/demo artifact'ı ve deployment workflow'u hazırla; ücretsiz repo/settings şartları uygulama gününde kontrol edilir. Gerçek Pages deploy/link/assets/rollback evidence'ı olmadan literal ürün Verified olmaz.
3. GitHub Pages'e private booking/PII/auth secret veya Java API credential koyma; gerçek uygulama local backend'e sahip kalır. Public demo fake dataset kullanır.
4. Mor Cloudflare için Day 75 Wrangler/workerd temelinde local Pages/Workers static asset/routing fixture'ını çalıştır. Gerçek managed Cloudflare deployment bu local deneyle tamamlanmış sayılmaz; erişim/no-cloud sınırı Partial olarak korunur.
5. Uygun ücretsiz/ücret riski olmayan kullanıcı erişimi yoksa GitHub Pages/Cloudflare actual deploy gap'i açık tutulur; hesap/billing/paid/trial otomatik oluşturulmaz.
6. Vercel/Netlify/Railway/Render seçeneklerini static/SSR/runtime/domain/cache/recovery sorumluluklarıyla karşılaştır; ücretli hosting zorunlu değildir.

## Planlanan dosyalar

- `labs/frontend/deployment/`
- `docs/runbooks/frontend-release-and-hosting.md`
- `docs/evidence/day-96/` — sürüm/edition, exact komut, browser/runtime, fixture, expected/actual, ölçüm ve recovery.

Bunlar aday implementation çıktılarıdır; dosya/dependency varlığı Verified değildir.

## Commit sırası

1. `docs(day-96): frontend gereksinim ve sınırları tanımla`
2. `feat(day-96): temsilî UI ve eğitim profillerini uygula`
3. `test(day-96): browser contract hata ve toparlanmayı doğrula`
4. `docs(day-96): evidence runbook ve karşılaştırmayı kapat`

Mevcut verified uygulama yeterliyse aynı sorumluluğu tekrar kurma/boş feat commit üretme; actual SHA/evidence ve eksik testleri bağla. Green ürün profilleri ana app'in aynı state/build/controller kaynağına competing owner olmaz.

## Doğrulama ve kapanış

- [ ] Local static/SSR deploy, deep link/asset/cache/rollback gerçek browser'da doğrulanır.
- [ ] Pages actual deploy varsa public URL evidence kaydedilir; Cloudflare local/managed ve erişim gap'leri birbirine karıştırılmaz.
- [ ] Konu/product/blue etiketleri öğrenme + gerçek temsilî uygulama + runtime evidence ile veya explicit erişim gap'inde izleniyor.
- [ ] Değişen kod için uygun type/lint/unit/integration/build check; ardından gerçek browser/API/local runtime doğrulaması yapıldı.
- [ ] Accessibility, auth/privacy, cancellation/cleanup ve bounded resource davranışı ilgili use-case'te test edildi.
- [ ] Sürüm/lisans/compatibility gün başında doğrulanıp pin edildi; source maps/env/artifact secret sızdırmıyor.
- [ ] Local/managed provider, mock/real API ve CSR/SSR/SSG/PWA kanıtları ayrı raporlandı.
- [ ] Coverage actual duruma güncellendi; yalnız comparison veya static export SSR implementation sayılmadı.

Ücretli cloud/model API/hosting zorunluluğu yoktur; hesap/billing/remote deployment bugün yapılmaz. Local lab production SLA/scale, arama sıralaması veya mesleki unvan kanıtı değildir.
