# Day 77 — Container, supply chain ve recovery uçtan uca

Durum: **Planlandı**. Bu gün eğitim milestone'ıdır; tek takvim günü sınırı yoktur. Plan belgesi çalışan ürün/evidence değildir.

## Önkoşul ve kapsam

[Day 76](day-76.md) kapanır; birikimli implementation snapshot'ından `day/77` türetilir. Emlak repo/85 günlük planında değişiklik yapılmaz. [DevOps ortak kararları](../DEVOPS-ROADMAP-EXTENSION.md), [kapsam matrisi](../coverage/devops-coverage.md) ve [uygulama sözleşmesi](../coverage/mandatory-implementation-contract.md) geçerlidir.

## Öğrenme ve uygulama görevleri

Roadmap etiketleri: `Containers`, `Docker`, `Container Orchestration`, `Kubernetes`, `Cloud Design Patterns`, `Availability`, `Data Management`, `Design and Implementation`, `Management and Monitoring`, `Backend`.

1. Emlak Docker/Kubernetes/BuildKit/security Day 47–62 ve araç Day 31–32 görev/evidence'ını bağla; image digest, non-root, resource/probes/network/storage/config sınırlarını çalışan Spring use-case üzerinde denetle.
2. Emlak Jenkins/SonarQube/Nexus/Harbor/Trivy/SBOM/Cosign Day 66–73 ile araç Day 34 release contract'ını kullan. Aynı image digest için build→test→scan/sign→registry→GitOps→runtime zincirini çalıştır.
3. Untrusted build, secret leak redaction, forbidden deploy/publish, missing signature veya kasıtlı failed gate fixture'ını uygula; kaynak kapasitesi nedeniyle platformları faz profilleriyle sırayla aç.
4. Argo/Flux sahibi ayrılmış ortamda promotion/drift/rollback ve schema uyumluluğu testini çalıştır; backend API/domain invariant recovery sonrası korunur.
5. Backup/restore/upgrade/failure tatbikatları için emlak Day 83–85 veya araç Day 46/62 actual evidence bağla; resource YAML restore tek başına canonical DB restore sayılmaz.
6. Cloud Design Patterns dört alt konusunu araç Day 51/57/59/61/62'ye bağla; generic migration YAML'ı veya chart kurulumu pattern correctness evidence'ı yerine geçmez.
7. Eksik zorunlu baseline görevi varsa araçta gerçek implementation/runtime test ile tamamla. Mevcut ürünlerin aynı role ikinci mandatory kurulumu yapılmaz.
8. Spring uygulamasının seçilmiş embedded servlet container'ı Tomcat ise dependency/version, connector limit ve graceful shutdown evidence'ını bağla. Tomcat sadece dependency adıyla tamamlanmış sayılmaz; farklı servlet container seçildiyse Tomcat yeşil Comparison kalır.

## Planlanan dosyalar

- `labs/devops-end-to-end/`
- `docs/evidence/day-77/release-and-recovery-report.md`
- `docs/evidence/day-77/` — exact komut, sürüm/edition, donanım, fixture, expected/actual sonuç ve recovery.

Bu yollar aday implementation dosyalarıdır; dosyanın varlığı Integration/Verified anlamına gelmez.

## Commit sırası

1. `docs(day-77): gereksinim sahiplik ve local kapsamı tanımla`
2. `feat(day-77): temsilî operasyon lab ve adapterlarını uygula`
3. `test(day-77): başarı hata ve toparlanmayı doğrula`
4. `docs(day-77): evidence runbook ve karşılaştırmayı kapat`

Var olan verified uygulama yeterliyse tekrar ürün veya boş feat commit oluşturulmaz; mevcut SHA/evidence ve gereken yeni testler bağlanır. Engellenen SaaS/provider için karşılaştırma commit'i literal runtime uygulaması gibi adlandırılmaz.

## Doğrulama ve kapanış

- [ ] Release zinciri digest/commit ile izlenebilir; failed gate deploy'u durdurur; uygulama E2E başarılıdır.
- [ ] Restore sonrası canonical booking ve projection invariant'ları doğrulanır; resource budget ve fiziksel HA sınırı raporlanır.
- [ ] Required başlıklara owner/öğrenme/implementation/test evidence bağlandı; engeller explicit gap veya kapsam istisnası olarak kaldı.
- [ ] Yeni/değişen kod için uygun build/contract/integration check başarılı; ardından local runtime çalıştırıldı.
- [ ] Compatibility, sürüm, ücretsiz edition/lisans ve resource bütçesi gün başında kontrol edilip pin edildi.
- [ ] İzole namespace/VM/profile sahipliği, stop condition, cleanup ve recovery kaydedildi.
- [ ] Secret/key/token/PII Git'e girmedi; untrusted CI publishing/deploy yetkisine erişmedi.
- [ ] Matris gerçek duruma güncellendi; plan veya local emulator sonucu managed-service Verified yapılmadı.

Ücretli AWS/Azure/GCP/HCP/SaaS/trial şartı yoktur; cloud hesap/kaynakları otomatik oluşturulmaz. Yerel lab gerçek production SLA, coğrafi HA veya mesleki unvan kanıtı değildir.
