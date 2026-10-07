# Day 89 — Frontend authentication ve web security

Durum: **Planlandı**. Bu eğitim milestone'ı birden fazla takvim gününe yayılabilir. Kod/runtime evidence henüz oluşturulmadı.

## Önkoşul ve kapsam

[Day 88](day-88.md) kapanır; önceki birikimli implementation snapshot'ından `day/89` türetilir. Emlak repo/85 günlük planı değişmez. [Frontend ortak planı](../FRONTEND-ROADMAP-EXTENSION.md), [coverage matrisi](../coverage/frontend-coverage.md) ve [uygulama sözleşmesi](../coverage/mandatory-implementation-contract.md) esas alınır.

Desktop Apps/Mobile Apps ve ilgili native framework/runtime'lar kapsam dışıdır. Web PWA ve responsive browser deneyleri kapsamda kalır. Java/Spring business backend ve canonical veri sahipliği korunur.

## Öğrenme ve uygulama görevleri

Roadmap etiketleri: `Auth Strategies`, `Web Security`, `CORS`, `HTTPS`, `CSP`, `OWASP Risks`.

1. Day 14/16–18/38/63 backend security görevlerini browser threat modeliyle bağla: cookie session, token/JWT/OAuth2/OIDC ve public-client PKCE/BFF sorumluluklarını açıkla; backend owner değişmez.
2. Cookie HttpOnly/Secure/SameSite, CSRF, session expiry/logout ve redirect allowlist deneylerini yap; browser confidential client credential görmesin.
3. CORS preflight/credentials ve HTTPS wrong CA/hostname testlerini; CSP report/enforce ve XSS injection sahte fixture'larını local ortamda doğrula.
4. OWASP risklerini sistematik vaka matrisiyle gerçek UI/API invariant'ına bağla; IDOR/broken auth, DOM XSS, dependency trust ve sensitive data disclosure örneklerini test et.
5. SSR kullanıcı cache izolasyonu, token log redaction ve third-party resource politikasını Day 91–92'ye taşı; client guard authorization değildir.

## Planlanan dosyalar

- `docs/security/frontend-threat-model.md`
- `web/tests/security/`
- `docs/evidence/day-89/` — sürüm/edition, exact komut, browser/runtime, fixture, expected/actual, ölçüm ve recovery.

Bunlar aday implementation çıktılarıdır; dosya/dependency varlığı Verified değildir.

## Commit sırası

1. `docs(day-89): frontend gereksinim ve sınırları tanımla`
2. `feat(day-89): temsilî UI ve eğitim profillerini uygula`
3. `test(day-89): browser contract hata ve toparlanmayı doğrula`
4. `docs(day-89): evidence runbook ve karşılaştırmayı kapat`

Mevcut verified uygulama yeterliyse aynı sorumluluğu tekrar kurma/boş feat commit üretme; actual SHA/evidence ve eksik testleri bağla. Green ürün profilleri ana app'in aynı state/build/controller kaynağına competing owner olmaz.

## Doğrulama ve kapanış

- [ ] Unauthorized/expired session/CSRF/origin/XSS fixture'ları beklenen 401/403/block davranışını üretir.
- [ ] Cross-user cache/token disclosure oluşmaz; Java backend authorization browser guard bypass'ta da çalışır.
- [ ] Konu/product/blue etiketleri öğrenme + gerçek temsilî uygulama + runtime evidence ile veya explicit erişim gap'inde izleniyor.
- [ ] Değişen kod için uygun type/lint/unit/integration/build check; ardından gerçek browser/API/local runtime doğrulaması yapıldı.
- [ ] Accessibility, auth/privacy, cancellation/cleanup ve bounded resource davranışı ilgili use-case'te test edildi.
- [ ] Sürüm/lisans/compatibility gün başında doğrulanıp pin edildi; source maps/env/artifact secret sızdırmıyor.
- [ ] Local/managed provider, mock/real API ve CSR/SSR/SSG/PWA kanıtları ayrı raporlandı.
- [ ] Coverage actual duruma güncellendi; yalnız comparison veya static export SSR implementation sayılmadı.

Ücretli cloud/model API/hosting zorunluluğu yoktur; hesap/billing/remote deployment bugün yapılmaz. Local lab production SLA/scale, arama sıralaması veya mesleki unvan kanıtı değildir.
