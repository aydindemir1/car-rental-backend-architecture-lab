# Day 75 — Serverless: Knative ve yerel provider runtime'ları

Durum: **Planlandı**. Bu gün eğitim milestone'ıdır; tek takvim günü sınırı yoktur. Plan belgesi çalışan ürün/evidence değildir.

## Önkoşul ve kapsam

[Day 74](day-74.md) kapanır; birikimli implementation snapshot'ından `day/75` türetilir. Emlak repo/85 günlük planında değişiklik yapılmaz. [DevOps ortak kararları](../DEVOPS-ROADMAP-EXTENSION.md), [kapsam matrisi](../coverage/devops-coverage.md) ve [uygulama sözleşmesi](../coverage/mandatory-implementation-contract.md) geçerlidir.

## Öğrenme ve uygulama görevleri

Roadmap etiketleri: `Serverless`, `Cloudflare`, `AWS Lambda`.

1. Araç Day 33 Knative gerçek Java scale-to-zero/cold-start lab'ını yeniden kullan; bu Serverless ana konusunun provider bağımsız uygulamasıdır.
2. Mor Cloudflare için resmi Wrangler/workerd yerel development modunda küçük stateless edge routing/header validation fixture'ı uygula. Remote binding/deploy yoktur; Node backend kullanılmaz, JavaScript yalnız Workers runtime kodu ve npm local tooling içindir.
3. Mor AWS Lambda için AWS SAM CLI + Docker ile Java handler'ın local invoke/start-api deneyini yap; payload/error/timeout ve idempotent fixture contract'ını test et. AWS credentials/deploy komutu şart değildir; real AWS integration eklenmez.
4. Cloudflare local runtime ve Lambda SAM local emülasyon kapsamını Partial/Local Lab olarak ayrı izle; gerçek managed provider, IAM, cold-start/performance veya bütün service parity doğrulaması sayma. Ücretsiz araç erişimi engellenirse ürün gap'i açık kalır.
5. Event/function lifecycle ve durable state sınırını Spring Cloud Function/Knative ile karşılaştır; function başarılı cevabını canonical booking mutation'sız fixture'da doğrula.
6. Azure/GCP Functions, Vercel/Netlify/Render/Railway alternatiflerini karşılaştır; cloud deploy/billing/trial zorunluluğu yoktur.

## Planlanan dosyalar

- `labs/serverless-provider-runtimes/`
- `docs/technology/serverless-local-vs-managed.md`
- `docs/evidence/day-75/` — exact komut, sürüm/edition, donanım, fixture, expected/actual sonuç ve recovery.

Bu yollar aday implementation dosyalarıdır; dosyanın varlığı Integration/Verified anlamına gelmez.

## Commit sırası

1. `docs(day-75): gereksinim sahiplik ve local kapsamı tanımla`
2. `feat(day-75): temsilî operasyon lab ve adapterlarını uygula`
3. `test(day-75): başarı hata ve toparlanmayı doğrula`
4. `docs(day-75): evidence runbook ve karşılaştırmayı kapat`

Var olan verified uygulama yeterliyse tekrar ürün veya boş feat commit oluşturulmaz; mevcut SHA/evidence ve gereken yeni testler bağlanır. Engellenen SaaS/provider için karşılaştırma commit'i literal runtime uygulaması gibi adlandırılmaz.

## Doğrulama ve kapanış

- [ ] Java Knative scale-to-zero/restart ve function failure gözlenir; local Java SAM input/error testi çalışır.
- [ ] Workers local request/validation ve cleanup doğrulanır; iki provider satırı managed-cloud Verified diye kapanmaz.
- [ ] Required başlıklara owner/öğrenme/implementation/test evidence bağlandı; engeller explicit gap veya kapsam istisnası olarak kaldı.
- [ ] Yeni/değişen kod için uygun build/contract/integration check başarılı; ardından local runtime çalıştırıldı.
- [ ] Compatibility, sürüm, ücretsiz edition/lisans ve resource bütçesi gün başında kontrol edilip pin edildi.
- [ ] İzole namespace/VM/profile sahipliği, stop condition, cleanup ve recovery kaydedildi.
- [ ] Secret/key/token/PII Git'e girmedi; untrusted CI publishing/deploy yetkisine erişmedi.
- [ ] Matris gerçek duruma güncellendi; plan veya local emulator sonucu managed-service Verified yapılmadı.

Ücretli AWS/Azure/GCP/HCP/SaaS/trial şartı yoktur; cloud hesap/kaynakları otomatik oluşturulmaz. Yerel lab gerçek production SLA, coğrafi HA veya mesleki unvan kanıtı değildir.
