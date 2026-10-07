# Day 70 — Terraform, Ansible ve kaynak sahipliği

Durum: **Planlandı**. Bu gün eğitim milestone'ıdır; tek takvim günü sınırı yoktur. Plan belgesi çalışan ürün/evidence değildir.

## Önkoşul ve kapsam

[Day 69](day-69.md) kapanır; birikimli implementation snapshot'ından `day/70` türetilir. Emlak repo/85 günlük planında değişiklik yapılmaz. [DevOps ortak kararları](../DEVOPS-ROADMAP-EXTENSION.md), [kapsam matrisi](../coverage/devops-coverage.md) ve [uygulama sözleşmesi](../coverage/mandatory-implementation-contract.md) geçerlidir.

## Öğrenme ve uygulama görevleri

Roadmap etiketleri: `Provisioning`, `Terraform`, `Configuration Management`, `Ansible`.

1. Emlak Day 63–65 Terraform/Ansible görevlerini ve gerçek evidence'ı bağla. Seçim Terraform Community CLI'dir; OpenTofu zorunlu ikinci uygulama değildir.
2. Evidence/görev eksikse araç local ayrılmış Docker network/volume/test container provisioning'ini Terraform ile uygula; provider lock/state/plan/apply/destroy sürecini test et. Compose/GitOps kaynaklarını ikinci kez sahiplenme.
3. Day 66 eğitim VM'sinde host kullanıcı/paket/service config'ini Ansible idempotent playbook ile yönet; ikinci run değişiklik üretmesin. FreeBSD/RHEL farklarını inventory role/condition ile sınırlı tut.
4. Manual drift, failed apply/task, partial setup ve reconcile deneylerini çalıştır; state secret'larını Git dışında tut, state backup/recovery ve destroy guard'larını yaz.
5. Pulumi/AWS CDK/CloudFormation, Chef/Puppet/Salt alternatiflerini scope/state/host responsibility açısından karşılaştır; cloud account ve ücretli provisioning yoktur.

## Planlanan dosyalar

- `infra/labs/provisioning/`
- `infra/labs/configuration-management/`
- `docs/runbooks/iac-state-and-drift.md`
- `docs/evidence/day-70/` — exact komut, sürüm/edition, donanım, fixture, expected/actual sonuç ve recovery.

Bu yollar aday implementation dosyalarıdır; dosyanın varlığı Integration/Verified anlamına gelmez.

## Commit sırası

1. `docs(day-70): gereksinim sahiplik ve local kapsamı tanımla`
2. `feat(day-70): temsilî operasyon lab ve adapterlarını uygula`
3. `test(day-70): başarı hata ve toparlanmayı doğrula`
4. `docs(day-70): evidence runbook ve karşılaştırmayı kapat`

Var olan verified uygulama yeterliyse tekrar ürün veya boş feat commit oluşturulmaz; mevcut SHA/evidence ve gereken yeni testler bağlanır. Engellenen SaaS/provider için karşılaştırma commit'i literal runtime uygulaması gibi adlandırılmaz.

## Doğrulama ve kapanış

- [ ] Aynı playbook ikinci run'da beklenmeyen değişiklik yapmaz; Terraform ayrılmış kaynakları plan/apply/destroy eder.
- [ ] Drift ve partial failure sonrası kontrollü reconcile doğrulanır; başka controller'ın kaynağı silinmez.
- [ ] Required başlıklara owner/öğrenme/implementation/test evidence bağlandı; engeller explicit gap veya kapsam istisnası olarak kaldı.
- [ ] Yeni/değişen kod için uygun build/contract/integration check başarılı; ardından local runtime çalıştırıldı.
- [ ] Compatibility, sürüm, ücretsiz edition/lisans ve resource bütçesi gün başında kontrol edilip pin edildi.
- [ ] İzole namespace/VM/profile sahipliği, stop condition, cleanup ve recovery kaydedildi.
- [ ] Secret/key/token/PII Git'e girmedi; untrusted CI publishing/deploy yetkisine erişmedi.
- [ ] Matris gerçek duruma güncellendi; plan veya local emulator sonucu managed-service Verified yapılmadı.

Ücretli AWS/Azure/GCP/HCP/SaaS/trial şartı yoktur; cloud hesap/kaynakları otomatik oluşturulmaz. Yerel lab gerçek production SLA, coğrafi HA veya mesleki unvan kanıtı değildir.
