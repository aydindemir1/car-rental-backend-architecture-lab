# Day 71 — Artifactory ve artifact lifecycle

Durum: **Planlandı**. Bu gün eğitim milestone'ıdır; tek takvim günü sınırı yoktur. Plan belgesi çalışan ürün/evidence değildir.

## Önkoşul ve kapsam

[Day 70](day-70.md) kapanır; birikimli implementation snapshot'ından `day/71` türetilir. Emlak repo/85 günlük planında değişiklik yapılmaz. [DevOps ortak kararları](../DEVOPS-ROADMAP-EXTENSION.md), [kapsam matrisi](../coverage/devops-coverage.md) ve [uygulama sözleşmesi](../coverage/mandatory-implementation-contract.md) geçerlidir.

## Öğrenme ve uygulama görevleri

Roadmap etiketleri: `Artifact Management`, `Artifactory`, `Nexus`.

1. Emlak Day 70 Nexus ve Day 71 Harbor canonical artifact/image kararları korunur. Mor Artifactory'yi sırf Nexus var diye uygulanmış sayma; ayrı geçici local reference profile kullan.
2. Resmi ücretsiz self-hosted Artifactory OSS Java artifact dağıtımını ve güncel download/license/support şartlarını doğrula. Ücretsiz uygun dağıtım erişimi yoksa ürün gap'i açık kalır; paid edition/trial veya güvensiz eski sürüm zorunlu değildir.
3. Uygun dağıtımda aynı sahte Java library'yi ayrı namespace/repository'de publish/resolve et; version/checksum, dependency proxy, credentials, retention ve forbidden publish deneylerini çalıştır.
4. Nexus ile format/ACL/cache/recovery işletim farkını gerçek ölçümlerle karşılaştır. Release pipeline için tek canonical artifact repository owner sürer; aynı production artifact iki registry'ye paralel mandatory publish edilmez.
5. Artifact corruption/missing version/repository outage ve backup/restore davranışını doğrula; OCI image owner Harbor'da kalır.

## Planlanan dosyalar

- `infra/labs/artifactory/`
- `labs/artifact-lifecycle/`
- `docs/technology/artifact-repository-comparison.md`
- `docs/evidence/day-71/` — exact komut, sürüm/edition, donanım, fixture, expected/actual sonuç ve recovery.

Bu yollar aday implementation dosyalarıdır; dosyanın varlığı Integration/Verified anlamına gelmez.

## Commit sırası

1. `docs(day-71): gereksinim sahiplik ve local kapsamı tanımla`
2. `feat(day-71): temsilî operasyon lab ve adapterlarını uygula`
3. `test(day-71): başarı hata ve toparlanmayı doğrula`
4. `docs(day-71): evidence runbook ve karşılaştırmayı kapat`

Var olan verified uygulama yeterliyse tekrar ürün veya boş feat commit oluşturulmaz; mevcut SHA/evidence ve gereken yeni testler bağlanır. Engellenen SaaS/provider için karşılaştırma commit'i literal runtime uygulaması gibi adlandırılmaz.

## Doğrulama ve kapanış

- [ ] Artifactory publish→clean consumer resolve gerçek JAR ve checksum ile doğrulanır; yetkisiz publish reddedilir.
- [ ] Repository failure/recovery ve retention sınırı gözlenir; uygun ücretsiz ürün yoksa literal Artifactory Verified olmaz.
- [ ] Required başlıklara owner/öğrenme/implementation/test evidence bağlandı; engeller explicit gap veya kapsam istisnası olarak kaldı.
- [ ] Yeni/değişen kod için uygun build/contract/integration check başarılı; ardından local runtime çalıştırıldı.
- [ ] Compatibility, sürüm, ücretsiz edition/lisans ve resource bütçesi gün başında kontrol edilip pin edildi.
- [ ] İzole namespace/VM/profile sahipliği, stop condition, cleanup ve recovery kaydedildi.
- [ ] Secret/key/token/PII Git'e girmedi; untrusted CI publishing/deploy yetkisine erişmedi.
- [ ] Matris gerçek duruma güncellendi; plan veya local emulator sonucu managed-service Verified yapılmadı.

Ücretli AWS/Azure/GCP/HCP/SaaS/trial şartı yoktur; cloud hesap/kaynakları otomatik oluşturulmaz. Yerel lab gerçek production SLA, coğrafi HA veya mesleki unvan kanıtı değildir.
