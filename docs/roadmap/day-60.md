# Day 60 — Data management ve messaging pattern'leri

Durum: **Planlandı**. Bu gün eğitim milestone'ıdır; birden fazla takvim gününe yayılabilir. Çalışan kod veya doğrulanmış sonuç henüz yoktur.

## Önkoşul ve kapsam

[Day 59](day-59.md) kapanır; önceki günün birikimli implementation snapshot'ından `day/60` türetilir. Emlak repo/planı değiştirilmez. [System Design matrisi](../coverage/system-design-coverage.md) ve [uygulama sözleşmesi](../coverage/mandatory-implementation-contract.md) esas alınır.

## Öğrenme çıktısı

Mesaj sırası, consumer sahipliği, event log ve projection sorumluluklarını birbirine karıştırmadan uygula.

Roadmap etiketleri: `Data Management`, `Messaging`, `Sequential Convoy`, `Queue-Based Load Leveling`, `Publisher/Subscriber`, `Priority Queue`, `Pipes and Filters`, `Pipes & Filters`, `Competing Consumers`, `Choreography`, `Claim Check`, `Event Sourcing`, `CQRS`.

## Görevler

1. Emlak Day 35–36 Event Sourcing/CQRS gerçek append/concurrency/replay evidence'ını bağla; yoksa araçta izole inspection aggregate için durable append-only event log + expected-version + replay/projection uygula. Canonical booking tablo sahipliğini bu fixture değiştirmez.
2. Day 24 broker'ında pub/sub iki bağımsız subscription; competing consumers tek queue üzerinde paylaşım; queue-based load leveling producer burst/consumer sabit hız deneyleri yap.
3. Sequential Convoy için aynı rental ID işlemlerini sequence/partition ile sırala; farklı ID'ler parallel kalsın. Duplicate/out-of-order input ve uzun süren bir ID'nin head-of-line etkisini doğrula.
4. RabbitMQ priority queue'yu izole lab profili yap; starvation ve aging/quota önlemini ölç. Emlakta aynı pattern'in verified örneği varsa tekrar ürün kurulumu gerekmez.
5. Pipes and Filters için inspection validate→normalize→route akışı; Choreography için rental-return event'ine bağımsız projection/notification tepkisi kur. Correlation, poison message ve DLQ/recovery uygula.
6. Claim Check için büyük sahte inspection dosyasını local file/blob service'e koy; mesaj yalnız opaque reference/hash taşısın. Authorization, missing blob, retention, orphan cleanup ve replay süresini test et. Day 63 Valet Key aynı storage fixture'ını kullanabilir.

## Planlanan dosyalar

- `labs/system-design/messaging-patterns/`
- `labs/system-design/inspection-event-log/`
- `docs/architecture/messaging-patterns.md`
- `docs/evidence/day-60/` — exact komut, sürüm, fixture, ölçüm koşulları, expected/actual ve recovery.

Bunlar implementation sırasında oluşturulacak dosya/klasörlerdir; mevcut integration kanıtı değildir.

## Commit sırası

1. `docs(day-60): gereksinim sahiplik ve failure sözleşmesini tanımla`
2. `feat(day-60): temsilî lab ve gerekli adapterları uygula`
3. `test(day-60): başarı hata ve toparlanmayı doğrula`
4. `docs(day-60): ölçüm evidence ve runbookları kapat`

Mevcut verified implementation yeterliyse aynı sorumluluk için yeni ürün/boş feat commit oluşturulmaz; gerçek evidence ve eksik testler bağlanır. Test önce correctness/hata sözleşmesini, sonra anlamlı performance hipotezini doğrular.

## Doğrulama ve kapanış

- [ ] Aynı ID sırası ve farklı ID parallel işleme gözlenir; duplicate yan etki yaratmaz.
- [ ] Priority starvation önlemi, blob lifecycle ve poison mesaj recovery kanıtlıdır; event log optimistic concurrency ve replay projection'ı doğru üretir.
- [ ] Her roadmap etiketine öğrenme + temsilî uygulama + runtime doğrulama kanıtı bağlandı; yalnız karşılaştırma tamamlanma sayılmadı.
- [ ] Yeni/değişen Java kodu için uygun build/contract/integration check başarılı; lab local runtime üzerinde çalıştırıldı.
- [ ] Kaynak limiti, stop condition, cleanup ve geri dönüş adımı kaydedildi.
- [ ] Secret/PII/gerçek ödeme bilgisi evidence'a girmedi; sürüm/lisans/uyumluluk uygulama gününde kontrol edilip pin edildi.
- [ ] Coverage gerçek duruma göre güncellendi; Planlandı/Implemented/Verified ayrımı korundu.

Ücretli AWS/Azure/GCP veya model API gerekmiyor. Yerel fault injection/replica/edge/namespace sonuçları production scale, coğrafi HA veya SLA kanıtı değildir.
