# Day 61 — Reliability, resiliency ve gözlemlenebilirlik

Durum: **Planlandı**. Bu gün eğitim milestone'ıdır; birden fazla takvim gününe yayılabilir. Çalışan kod veya doğrulanmış sonuç henüz yoktur.

## Önkoşul ve kapsam

[Day 60](day-60.md) kapanır; önceki günün birikimli implementation snapshot'ından `day/61` türetilir. Emlak repo/planı değiştirilmez. [System Design matrisi](../coverage/system-design-coverage.md) ve [uygulama sözleşmesi](../coverage/mandatory-implementation-contract.md) esas alınır.

## Öğrenme çıktısı

Retry/circuit/bulkhead/compensation ile ölçüm ve alert'i aynı failure senaryosunda doğrula; health başarıyla domain doğruluğu aynı değildir.

Roadmap etiketleri: `Reliability Patterns`, `Resiliency`, `Health Endpoint Monitoring`, `Throttling`, `Bulkhead`, `Circuit Breaker`, `Compensating Transaction`, `Retry`, `Monitoring`, `Health Monitoring`, `Availability Monitoring`, `Performance Monitoring`, `Security Monitoring`, `Usage Monitoring`, `Instrumentation`, `Visualization & Alerts`.

## Görevler

1. Spring Cloud CircuitBreaker/Resilience4j mevcut yaklaşımını kullan; booking owner ve non-critical rapor dependency'lerini ayrı bulkhead/budget ile sınırla. Deadline, bounded retry+jitter, circuit half-open ve throttling uygula.
2. Day 55/60 queue load leveling ve supervisor; Day 51 leader recovery evidence'larını bağla. Non-idempotent komutu blind retry yapma; durable command/result reconciliation kullan.
3. Rezervasyon ile sahte depozito authorization saga'sında ikinci adımı başarısız yap; idempotent compensation ve retry, compensation failure/manual intervention yolunu uygula. Gerçek ödeme ve her işlemin geri alınabilir olduğu varsayımı yoktur.
4. Health Endpoint Monitoring'de startup/readiness/liveness rolünü ayır; dependency outage sırasında yanlış restart storm/false healthy üretimini test et.
5. Day 36 OTel/Prometheus/Grafana üzerine health, availability, performance, security ve usage dashboard/alert ekle. User ID gibi yüksek cardinality/PII label kullanma; sampling ve retention budget belirt.
6. Sentetik arama/booking probe, reject/error, saturation, projection lag ve auth denial ölç; alert firing/resolution ile runbook action'ını çalıştır. Day 46 Monit yalnız kendi local worker kapsamını korur.
7. Failure injection hipotezi, stop condition, beklenen/gerçek davranış ve toparlanma ölçümünü kaydet.

## Planlanan dosyalar

- `labs/system-design/reliability/`
- `infra/labs/system-design-monitoring/`
- `docs/runbooks/pattern-failure-drills.md`
- `docs/evidence/day-61/` — exact komut, sürüm, fixture, ölçüm koşulları, expected/actual ve recovery.

Bunlar implementation sırasında oluşturulacak dosya/klasörlerdir; mevcut integration kanıtı değildir.

## Commit sırası

1. `docs(day-61): gereksinim sahiplik ve failure sözleşmesini tanımla`
2. `feat(day-61): temsilî lab ve gerekli adapterları uygula`
3. `test(day-61): başarı hata ve toparlanmayı doğrula`
4. `docs(day-61): ölçüm evidence ve runbookları kapat`

Mevcut verified implementation yeterliyse aynı sorumluluk için yeni ürün/boş feat commit oluşturulmaz; gerçek evidence ve eksik testler bağlanır. Test önce correctness/hata sözleşmesini, sonra anlamlı performance hipotezini doğrular.

## Doğrulama ve kapanış

- [ ] Bulkhead bir dependency hatasını sınırlar; retry budget/circuit recovery ölçülür; compensation tekrarında çift yan etki yoktur.
- [ ] Beş monitoring türü için gerçek sinyal ve test alert'i oluşur/çözülür; probe sonucu domain invariant testiyle birlikte değerlendirilir.
- [ ] Her roadmap etiketine öğrenme + temsilî uygulama + runtime doğrulama kanıtı bağlandı; yalnız karşılaştırma tamamlanma sayılmadı.
- [ ] Yeni/değişen Java kodu için uygun build/contract/integration check başarılı; lab local runtime üzerinde çalıştırıldı.
- [ ] Kaynak limiti, stop condition, cleanup ve geri dönüş adımı kaydedildi.
- [ ] Secret/PII/gerçek ödeme bilgisi evidence'a girmedi; sürüm/lisans/uyumluluk uygulama gününde kontrol edilip pin edildi.
- [ ] Coverage gerçek duruma göre güncellendi; Planlandı/Implemented/Verified ayrımı korundu.

Ücretli AWS/Azure/GCP veya model API gerekmiyor. Yerel fault injection/replica/edge/namespace sonuçları production scale, coğrafi HA veya SLA kanıtı değildir.
