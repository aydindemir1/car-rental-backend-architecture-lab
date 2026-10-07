# Day 73 — Elastic, Loki ve observability ürünleri

Durum: **Planlandı**. Bu gün eğitim milestone'ıdır; tek takvim günü sınırı yoktur. Plan belgesi çalışan ürün/evidence değildir.

## Önkoşul ve kapsam

[Day 72](day-72.md) kapanır; birikimli implementation snapshot'ından `day/73` türetilir. Emlak repo/85 günlük planında değişiklik yapılmaz. [DevOps ortak kararları](../DEVOPS-ROADMAP-EXTENSION.md), [kapsam matrisi](../coverage/devops-coverage.md) ve [uygulama sözleşmesi](../coverage/mandatory-implementation-contract.md) geçerlidir.

## Öğrenme ve uygulama görevleri

Roadmap etiketleri: `Infrastructure Monitoring`, `Prometheus`, `Grafana`, `Datadog`, `Logs Management`, `Elastic Stack`, `Loki`, `Observability`, `OpenTelemetry`, `Jaeger`.

1. Emlak Day 29–30/81 Prometheus/Grafana/Loki/Tempo ve araç Day 36/61 monitoring görevlerini gerçek evidence ile yeniden kullan; topic closure için dashboard/alert/tracing actual testleri gereklidir.
2. Mor Elastic Stack için izole local Elasticsearch + Kibana ve desteklenen ücretsiz ingestion bileşeni kur. Structured Spring log fixture'ını ingest/search et; mapping, retention, redaction, drop/retry ve storage bütçesini test et. Paid security/ML özellikleri varsayılmaz.
3. Loki ile aynı redakte fixture'ın query/cardinality/retention farkını ayrı profillerde ölç. İki kalıcı logging owner zorunlu değildir; baseline korunur.
4. Yeşil OpenTelemetry exporter/collector gerçek trace/metric pipeline; Jaeger'i ayrı trace backend profiliyle uygula ve HTTP→broker→consumer correlation'ını doğrula. OTel collector'ı storage backend sanma.
5. Datadog için ürün/agent/collector/SaaS ayrımını incele. İstenirse local agent/DogStatsD fixture'ında metrik kabulünü gözle; bunu Datadog SaaS dashboard/monitor doğrulaması sayma.
6. Ücretsiz, ücret riski olmayan Datadog ürün erişimi uygulama gününde doğrulanır ve kullanıcı erişimi mevcutsa küçük sahte workload için gerçek monitor/alert çalıştırılır. Yoksa mor Datadog literal ürün gap'i açık kalır; paid/trial zorunluluğu yoktur.
7. Collector/log backend outage, disk pressure, cardinality ve recovery deneylerini yap; observability business request'i bozmasın.

## Planlanan dosyalar

- `infra/labs/elastic-stack/`
- `infra/labs/observability-comparison/`
- `docs/runbooks/telemetry-failure-and-retention.md`
- `docs/evidence/day-73/` — exact komut, sürüm/edition, donanım, fixture, expected/actual sonuç ve recovery.

Bu yollar aday implementation dosyalarıdır; dosyanın varlığı Integration/Verified anlamına gelmez.

## Commit sırası

1. `docs(day-73): gereksinim sahiplik ve local kapsamı tanımla`
2. `feat(day-73): temsilî operasyon lab ve adapterlarını uygula`
3. `test(day-73): başarı hata ve toparlanmayı doğrula`
4. `docs(day-73): evidence runbook ve karşılaştırmayı kapat`

Var olan verified uygulama yeterliyse tekrar ürün veya boş feat commit oluşturulmaz; mevcut SHA/evidence ve gereken yeni testler bağlanır. Engellenen SaaS/provider için karşılaştırma commit'i literal runtime uygulaması gibi adlandırılmaz.

## Doğrulama ve kapanış

- [ ] Elastic ingestion/search ve Loki query gerçek fixture ile çalışır; malformed/redacted log ve outage sonrası davranış kaydedilir.
- [ ] Trace correlation ve Prometheus/Grafana alert firing/resolution kanıtlıdır; Datadog SaaS evidence olmadan ürün Verified değildir.
- [ ] Required başlıklara owner/öğrenme/implementation/test evidence bağlandı; engeller explicit gap veya kapsam istisnası olarak kaldı.
- [ ] Yeni/değişen kod için uygun build/contract/integration check başarılı; ardından local runtime çalıştırıldı.
- [ ] Compatibility, sürüm, ücretsiz edition/lisans ve resource bütçesi gün başında kontrol edilip pin edildi.
- [ ] İzole namespace/VM/profile sahipliği, stop condition, cleanup ve recovery kaydedildi.
- [ ] Secret/key/token/PII Git'e girmedi; untrusted CI publishing/deploy yetkisine erişmedi.
- [ ] Matris gerçek duruma güncellendi; plan veya local emulator sonucu managed-service Verified yapılmadı.

Ücretli AWS/Azure/GCP/HCP/SaaS/trial şartı yoktur; cloud hesap/kaynakları otomatik oluşturulmaz. Yerel lab gerçek production SLA, coğrafi HA veya mesleki unvan kanıtı değildir.
