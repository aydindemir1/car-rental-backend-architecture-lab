# Day 59 — Design ve implementation pattern'leri

Durum: **Planlandı**. Bu gün eğitim milestone'ıdır; birden fazla takvim gününe yayılabilir. Çalışan kod veya doğrulanmış sonuç henüz yoktur.

## Önkoşul ve kapsam

[Day 58](day-58.md) kapanır; önceki günün birikimli implementation snapshot'ından `day/59` türetilir. Emlak repo/planı değiştirilmez. [System Design matrisi](../coverage/system-design-coverage.md) ve [uygulama sözleşmesi](../coverage/mandatory-implementation-contract.md) esas alınır.

## Öğrenme çıktısı

Cloud design pattern'lerinin sağlayıcıdan bağımsız rollerini mevcut Spring/Kubernetes sisteminde gerçek istek akışıyla göster.

Roadmap etiketleri: `Application Layer`, `Microservices`, `Service Discovery`, `Cloud Design Patterns`, `Design & Implementation`, `Strangler Fig`, `Sidecar`, `Gateway Routing`, `Gateway Offloading`, `Gateway Aggregation`, `External Config Store`, `Compute Resource Consolidation`, `Backends for Frontend`, `Anti-Corruption Layer`, `Ambassador`.

## Görevler

1. Day 12 extraction'ı Strangler Fig olarak route cutover/rollback ile doğrula; Day 27 legacy adapter'ının Anti-Corruption Layer mapping ve hata semantiğini yeniden kullan. Emlak karşılığı varsa evidence bağla.
2. Day 13 service discovery ve Day 36 Linkerd Sidecar'ının discovery/telemetry davranışını doğrula. Ambassador için ayrı local outbound Nginx proxy profiliyle endpoint/timeout soyutlaması uygula; Linkerd ile aynı trafiğe iki sahip zorlamaz.
3. Mevcut Spring Cloud Gateway'de routing ve TLS/auth gibi offloading sınırını kur; downstream kendi authorization kontrolünü sürdürsün.
4. Web teslim paneline BFF ve gateway aggregation endpoint'i bağla; parallel fetch deadline, partial response ve downstream outage testlerini uygula.
5. External Config Store için mevcut Spring Cloud config/Consul seçimini kullan; config değişimi, version, unavailable startup/runtime davranışını test et.
6. Compute Resource Consolidation için iki farklı bounded workload'u aynı local worker üzerinde requests/limits ile yerleştir; contention ve isolation ölç. Day 52 static hosting, Day 51 leader, Day 60 CQRS/pipes evidence'ını bağla.
7. Her pattern'in domain tetikleyicisi, sahibi ve failure mode'u yaz; Azure pattern kaynakları ücretli Azure deployment zorunluluğu değildir.

## Planlanan dosyalar

- `labs/system-design/application-patterns/`
- `docs/architecture/application-patterns.md`
- `docs/evidence/day-59/` — exact komut, sürüm, fixture, ölçüm koşulları, expected/actual ve recovery.

Bunlar implementation sırasında oluşturulacak dosya/klasörlerdir; mevcut integration kanıtı değildir.

## Commit sırası

1. `docs(day-59): gereksinim sahiplik ve failure sözleşmesini tanımla`
2. `feat(day-59): temsilî lab ve gerekli adapterları uygula`
3. `test(day-59): başarı hata ve toparlanmayı doğrula`
4. `docs(day-59): ölçüm evidence ve runbookları kapat`

Mevcut verified implementation yeterliyse aynı sorumluluk için yeni ürün/boş feat commit oluşturulmaz; gerçek evidence ve eksik testler bağlanır. Test önce correctness/hata sözleşmesini, sonra anlamlı performance hipotezini doğrular.

## Doğrulama ve kapanış

- [ ] Cutover/rollback, legacy mapping ve discovery gerçek çağrılarla doğrulanır.
- [ ] BFF/gateway/config/ambassador hata deneyleri contract'a uyar; consolidation'da resource sınırları ve contention ölçülür.
- [ ] Her roadmap etiketine öğrenme + temsilî uygulama + runtime doğrulama kanıtı bağlandı; yalnız karşılaştırma tamamlanma sayılmadı.
- [ ] Yeni/değişen Java kodu için uygun build/contract/integration check başarılı; lab local runtime üzerinde çalıştırıldı.
- [ ] Kaynak limiti, stop condition, cleanup ve geri dönüş adımı kaydedildi.
- [ ] Secret/PII/gerçek ödeme bilgisi evidence'a girmedi; sürüm/lisans/uyumluluk uygulama gününde kontrol edilip pin edildi.
- [ ] Coverage gerçek duruma göre güncellendi; Planlandı/Implemented/Verified ayrımı korundu.

Ücretli AWS/Azure/GCP veya model API gerekmiyor. Yerel fault injection/replica/edge/namespace sonuçları production scale, coğrafi HA veya SLA kanıtı değildir.
