# Day 76 — Cloud sağlayıcıları: kavramlar ve kapsam istisnası

Durum: **Planlandı**. Bu gün eğitim milestone'ıdır; tek takvim günü sınırı yoktur. Plan belgesi çalışan ürün/evidence değildir.

## Önkoşul ve kapsam

[Day 75](day-75.md) kapanır; birikimli implementation snapshot'ından `day/76` türetilir. Emlak repo/85 günlük planında değişiklik yapılmaz. [DevOps ortak kararları](../DEVOPS-ROADMAP-EXTENSION.md), [kapsam matrisi](../coverage/devops-coverage.md) ve [uygulama sözleşmesi](../coverage/mandatory-implementation-contract.md) geçerlidir.

## Öğrenme ve uygulama görevleri

Roadmap etiketleri: `Cloud Providers`, `AWS`, `Azure`, `Google Cloud`.

1. Önceki ücretli cloud yok ve AWS/Azure/GCP yerine local/self-hosted kararını koru. AWS/Azure/Google Cloud mor ürünlerinin gerçek provider uygulaması bu kararla karşılanmış değildir; matriste Açık istisna / provider runtime yok olarak göster.
2. IaaS/PaaS/SaaS, region/AZ, shared responsibility, IAM, network/storage, quotas ve cost/egress kavramlarını resmi provider kaynakları üzerinden karşılaştır. Free tier/trial'ı sınırsız ücretsiz ortam varsayma.
3. Day 62 local stamps/geodes, Day 68 network policy ve Day 72 identity/secrets üzerinde provider bağımsız responsibility lab'ını bağla. Bunlar Cloud Providers ürünlerinin yerine aynı ürün gibi sayılmaz.
4. Üç provider için Java Spring deploy tasarımını yalnız tasarım belgesi olarak çıkar: permission boundary, network flow, registry, managed DB, backup ve billable resource listesi. Terraform cloud apply veya hesap oluşturma yoktur.
5. Doğrudan provider deneyimi ileride ayrıca kullanıcı kararıyla açılırsa ücretsiz limit/ücret riski ve account kapsamı yeniden değerlendirilir. Bugünkü program Cloud Providers literal kullanımını tamamlandı ilan etmez.
6. Digital Ocean/Alibaba/Hetzner/Heroku/diğer managed alternatifleri comparison seviyesinde tut; satın alma veya ücretli altyapı kurulumu yoktur.

## Planlanan dosyalar

- `docs/architecture/cloud-provider-responsibility-comparison.md`
- `docs/coverage/devops-cloud-exceptions.md`
- `docs/evidence/day-76/` — exact komut, sürüm/edition, donanım, fixture, expected/actual sonuç ve recovery.

Bu yollar aday implementation dosyalarıdır; dosyanın varlığı Integration/Verified anlamına gelmez.

## Commit sırası

1. `docs(day-76): gereksinim sahiplik ve local kapsamı tanımla`
2. `feat(day-76): temsilî operasyon lab ve adapterlarını uygula`
3. `test(day-76): başarı hata ve toparlanmayı doğrula`
4. `docs(day-76): evidence runbook ve karşılaştırmayı kapat`

Var olan verified uygulama yeterliyse tekrar ürün veya boş feat commit oluşturulmaz; mevcut SHA/evidence ve gereken yeni testler bağlanır. Engellenen SaaS/provider için karşılaştırma commit'i literal runtime uygulaması gibi adlandırılmaz.

## Doğrulama ve kapanış

- [ ] Local network/identity/restore sözleşmeleri gerçek test evidence'ına bağlıdır; provider tasarımının uygulanmadığı açıkça yazılır.
- [ ] Cloud Providers/AWS/Azure/GCP status'ları full coverage hesabında istisna olarak görünür; ücretli kaynak oluşturulmaz.
- [ ] Required başlıklara owner/öğrenme/implementation/test evidence bağlandı; engeller explicit gap veya kapsam istisnası olarak kaldı.
- [ ] Yeni/değişen kod için uygun build/contract/integration check başarılı; ardından local runtime çalıştırıldı.
- [ ] Compatibility, sürüm, ücretsiz edition/lisans ve resource bütçesi gün başında kontrol edilip pin edildi.
- [ ] İzole namespace/VM/profile sahipliği, stop condition, cleanup ve recovery kaydedildi.
- [ ] Secret/key/token/PII Git'e girmedi; untrusted CI publishing/deploy yetkisine erişmedi.
- [ ] Matris gerçek duruma güncellendi; plan veya local emulator sonucu managed-service Verified yapılmadı.

Ücretli AWS/Azure/GCP/HCP/SaaS/trial şartı yoktur; cloud hesap/kaynakları otomatik oluşturulmaz. Yerel lab gerçek production SLA, coğrafi HA veya mesleki unvan kanıtı değildir.
