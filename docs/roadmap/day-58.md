# Day 58 — On performance antipattern'i ölç ve düzelt

Durum: **Planlandı**. Bu gün eğitim milestone'ıdır; birden fazla takvim gününe yayılabilir. Çalışan kod veya doğrulanmış sonuç henüz yoktur.

## Önkoşul ve kapsam

[Day 57](day-57.md) kapanır; önceki günün birikimli implementation snapshot'ından `day/58` türetilir. Emlak repo/planı değiştirilmez. [System Design matrisi](../coverage/system-design-coverage.md) ve [uygulama sözleşmesi](../coverage/mandatory-implementation-contract.md) esas alınır.

## Öğrenme çıktısı

Her antipattern için kötü fixture, ölçülen belirti, düzeltme ve correctness regression evidence'ı oluştur.

Roadmap etiketleri: `Performance Antipatterns`, `Busy Database`, `Busy Frontend`, `Chatty I/O`, `Extraneous Fetching`, `Improper Instantiation`, `Monolithic Persistence`, `No Caching`, `Noisy Neighbor`, `Retry Storm`, `Synchronous I/O`.

## Görevler

1. Busy Database için pahalı/N+1 query; Monolithic Persistence için farklı erişim işlerinin tek hot storage yolunda rekabeti; No Caching için tekrar hesaplama fixture'ı oluştur. Query/ownership/cache düzeltmelerini ayrı değerlendir.
2. Busy Frontend için gereksiz render/iş; Extraneous Fetching için kullanılmayan geniş payload; Chatty I/O için çok sayıda küçük uzak çağrı oluştur. Browser ve backend trace ile önce/sonra ölç.
3. Improper Instantiation için her request'te expensive client; Synchronous I/O için bağımsız işi bloklayan yol kur. Bounded reuse/lifecycle ve async değişikliklerini doğrula.
4. Noisy Neighbor için sınırlı CPU/IO tüketen fixture; Retry Storm için kontrollü dependency failure + sınırlı kötü retry deneyi kur. Resource isolation, jitter, retry budget ve bulkhead ile düzelt.
5. Her on konu için workload, veri, donanım, duration, p95, error, CPU/heap/queue metriği ve domain invariant kontrolünü kaydet. Deneyler yalnız local namespace ve sınırlandırılmış sürede çalışır.

## Planlanan dosyalar

- `labs/system-design/antipatterns/`
- `docs/evidence/day-58/antipattern-matrix.md`
- `docs/evidence/day-58/` — exact komut, sürüm, fixture, ölçüm koşulları, expected/actual ve recovery.

Bunlar implementation sırasında oluşturulacak dosya/klasörlerdir; mevcut integration kanıtı değildir.

## Commit sırası

1. `docs(day-58): gereksinim sahiplik ve failure sözleşmesini tanımla`
2. `feat(day-58): temsilî lab ve gerekli adapterları uygula`
3. `test(day-58): başarı hata ve toparlanmayı doğrula`
4. `docs(day-58): ölçüm evidence ve runbookları kapat`

Mevcut verified implementation yeterliyse aynı sorumluluk için yeni ürün/boş feat commit oluşturulmaz; gerçek evidence ve eksik testler bağlanır. Test önce correctness/hata sözleşmesini, sonra anlamlı performance hipotezini doğrular.

## Doğrulama ve kapanış

- [ ] On antipattern'in her biri için gözlenebilir önce/sonra ve başarısızlık yolu vardır; iyileşmeyen ölçüm gizlenmez.
- [ ] Düzeltme sonucu booking correctness, API contract ve resource cleanup korunur; tek cold/warm farkı genel speedup diye sunulmaz.
- [ ] Her roadmap etiketine öğrenme + temsilî uygulama + runtime doğrulama kanıtı bağlandı; yalnız karşılaştırma tamamlanma sayılmadı.
- [ ] Yeni/değişen Java kodu için uygun build/contract/integration check başarılı; lab local runtime üzerinde çalıştırıldı.
- [ ] Kaynak limiti, stop condition, cleanup ve geri dönüş adımı kaydedildi.
- [ ] Secret/PII/gerçek ödeme bilgisi evidence'a girmedi; sürüm/lisans/uyumluluk uygulama gününde kontrol edilip pin edildi.
- [ ] Coverage gerçek duruma göre güncellendi; Planlandı/Implemented/Verified ayrımı korundu.

Ücretli AWS/Azure/GCP veya model API gerekmiyor. Yerel fault injection/replica/edge/namespace sonuçları production scale, coğrafi HA veya SLA kanıtı değildir.
