# Day 72 — Vault, ESO ve SOPS ile secret lifecycle

Durum: **Planlandı**. Bu gün eğitim milestone'ıdır; tek takvim günü sınırı yoktur. Plan belgesi çalışan ürün/evidence değildir.

## Önkoşul ve kapsam

[Day 71](day-71.md) kapanır; birikimli implementation snapshot'ından `day/72` türetilir. Emlak repo/85 günlük planında değişiklik yapılmaz. [DevOps ortak kararları](../DEVOPS-ROADMAP-EXTENSION.md), [kapsam matrisi](../coverage/devops-coverage.md) ve [uygulama sözleşmesi](../coverage/mandatory-implementation-contract.md) geçerlidir.

## Öğrenme ve uygulama görevleri

Roadmap etiketleri: `Secret Management`, `Vault`, `ESO`, `SOPs`.

1. Emlak Day 24/54 Vault policy/rotation ve Kubernetes auth/Agent görevleri ile araç mevcut secret görevlerini kullan; aynı secret için çift fetch sahibi oluşturma.
2. Bir servis credential'ını namespace/service identity scope'uyla al; expired lease, revocation, rotation ve Vault outage davranışını gerçek runtime'da test et.
3. Yeşil ESO (External Secrets Operator) için ayrı lab namespace'de Vault→Kubernetes Secret reconciliation uygula. İlgili namespace'de aynı credential'ı Agent Injector/Spring Cloud Vault ayrıca fetch etmez.
4. Roadmap'in 'SOPs' etiketini SOPS secret encryption aracı olarak yorumla; bu yorum snapshot etiketi korunarak belgelenir. age key ile yalnız lab bootstrap manifest'ini encrypt/decrypt et; private key Git dışındadır. ESO runtime credential ile aynı nesnenin competing lifecycle'ı kurulmaz.
5. RBAC, audit log redaction, mount/refresh ve restore sonrası credential invalidation testlerini yap. Sealed Secrets/cloud-specific tools alternatiflerini karşılaştır.

## Planlanan dosyalar

- `infra/labs/secret-lifecycle/`
- `docs/runbooks/secret-rotation-and-recovery.md`
- `docs/evidence/day-72/` — exact komut, sürüm/edition, donanım, fixture, expected/actual sonuç ve recovery.

Bu yollar aday implementation dosyalarıdır; dosyanın varlığı Integration/Verified anlamına gelmez.

## Commit sırası

1. `docs(day-72): gereksinim sahiplik ve local kapsamı tanımla`
2. `feat(day-72): temsilî operasyon lab ve adapterlarını uygula`
3. `test(day-72): başarı hata ve toparlanmayı doğrula`
4. `docs(day-72): evidence runbook ve karşılaştırmayı kapat`

Var olan verified uygulama yeterliyse tekrar ürün veya boş feat commit oluşturulmaz; mevcut SHA/evidence ve gereken yeni testler bağlanır. Engellenen SaaS/provider için karşılaştırma commit'i literal runtime uygulaması gibi adlandırılmaz.

## Doğrulama ve kapanış

- [ ] Yanlış identity secret okuyamaz; rotation uygulamaya doğru yansır; Vault outage policy'ye uygun fail-fast/degrade üretir.
- [ ] ESO reconcile/rotate ve SOPS yanlış key/tamper deneyleri kanıtlıdır; plaintext/key Git'e girmez.
- [ ] Required başlıklara owner/öğrenme/implementation/test evidence bağlandı; engeller explicit gap veya kapsam istisnası olarak kaldı.
- [ ] Yeni/değişen kod için uygun build/contract/integration check başarılı; ardından local runtime çalıştırıldı.
- [ ] Compatibility, sürüm, ücretsiz edition/lisans ve resource bütçesi gün başında kontrol edilip pin edildi.
- [ ] İzole namespace/VM/profile sahipliği, stop condition, cleanup ve recovery kaydedildi.
- [ ] Secret/key/token/PII Git'e girmedi; untrusted CI publishing/deploy yetkisine erişmedi.
- [ ] Matris gerçek duruma güncellendi; plan veya local emulator sonucu managed-service Verified yapılmadı.

Ücretli AWS/Azure/GCP/HCP/SaaS/trial şartı yoktur; cloud hesap/kaynakları otomatik oluşturulmaz. Yerel lab gerçek production SLA, coğrafi HA veya mesleki unvan kanıtı değildir.
