# Day 74 — Consul service mesh ve GitOps sınırları

Durum: **Planlandı**. Bu gün eğitim milestone'ıdır; tek takvim günü sınırı yoktur. Plan belgesi çalışan ürün/evidence değildir.

## Önkoşul ve kapsam

[Day 73](day-73.md) kapanır; birikimli implementation snapshot'ından `day/74` türetilir. Emlak repo/85 günlük planında değişiklik yapılmaz. [DevOps ortak kararları](../DEVOPS-ROADMAP-EXTENSION.md), [kapsam matrisi](../coverage/devops-coverage.md) ve [uygulama sözleşmesi](../coverage/mandatory-implementation-contract.md) geçerlidir.

## Öğrenme ve uygulama görevleri

Roadmap etiketleri: `Service Mesh`, `Consul`, `Istio`, `Linkerd`, `Envoy`, `GitOps`, `ArgoCD`, `FluxCD`.

1. Emlak Day 74–79 Argo CD/Istio ve araç Day 35–36 Flux/Linkerd planlarını gerçek evidence ile bağla; aynı cluster resource'u iki GitOps controller yönetmez.
2. Mor Consul service mesh için ayrı local iki Spring workload profili kur. Discovery tek başına mesh uygulaması değildir; Consul connect + Envoy sidecar, service identity/mTLS ve intentions policy gerçekten çalışsın.
3. Allowed/denied service call, certificate lifecycle ve control-plane outage davranışını test et. Enterprise/HCP özelliği veya paid distribution gerekmez; sürüm/lisans uygulama başında doğrulanır.
4. Istio/Linkerd/Consul aynı namespace/service için competing mesh sahibi olmaz; profilleri sırayla aç. Retry/timeout app/mesh responsibility'lerini ayır.
5. Flux reconcile/drift/rollback ve Argo CD mevcut promotion evidence'ını doğrula. Eksik zorunlu ürün evidence'ı varsa araçta izole temsilî profile sahip işi uygula; comparison tek başına kapatmaz.
6. Yeşil Envoy Consul data plane üzerinden gerçekten kullanılmışsa config/stats ve failure evidence bağla; diğer green mesh/platform seçeneklerini karşılaştır.

## Planlanan dosyalar

- `infra/labs/consul-mesh/`
- `docs/technology/mesh-and-gitops-comparison.md`
- `docs/evidence/day-74/` — exact komut, sürüm/edition, donanım, fixture, expected/actual sonuç ve recovery.

Bu yollar aday implementation dosyalarıdır; dosyanın varlığı Integration/Verified anlamına gelmez.

## Commit sırası

1. `docs(day-74): gereksinim sahiplik ve local kapsamı tanımla`
2. `feat(day-74): temsilî operasyon lab ve adapterlarını uygula`
3. `test(day-74): başarı hata ve toparlanmayı doğrula`
4. `docs(day-74): evidence runbook ve karşılaştırmayı kapat`

Var olan verified uygulama yeterliyse tekrar ürün veya boş feat commit oluşturulmaz; mevcut SHA/evidence ve gereken yeni testler bağlanır. Engellenen SaaS/provider için karşılaştırma commit'i literal runtime uygulaması gibi adlandırılmaz.

## Doğrulama ve kapanış

- [ ] Consul workload trafiği identity/mTLS/intentions üzerinden izin/verme testiyle doğrulanır; plain discovery yeterli değildir.
- [ ] GitOps drift/recovery ve baseline mesh identity testleri kanıtlıdır; competing controller yoktur.
- [ ] Required başlıklara owner/öğrenme/implementation/test evidence bağlandı; engeller explicit gap veya kapsam istisnası olarak kaldı.
- [ ] Yeni/değişen kod için uygun build/contract/integration check başarılı; ardından local runtime çalıştırıldı.
- [ ] Compatibility, sürüm, ücretsiz edition/lisans ve resource bütçesi gün başında kontrol edilip pin edildi.
- [ ] İzole namespace/VM/profile sahipliği, stop condition, cleanup ve recovery kaydedildi.
- [ ] Secret/key/token/PII Git'e girmedi; untrusted CI publishing/deploy yetkisine erişmedi.
- [ ] Matris gerçek duruma güncellendi; plan veya local emulator sonucu managed-service Verified yapılmadı.

Ücretli AWS/Azure/GCP/HCP/SaaS/trial şartı yoktur; cloud hesap/kaynakları otomatik oluşturulmaz. Yerel lab gerçek production SLA, coğrafi HA veya mesleki unvan kanıtı değildir.
