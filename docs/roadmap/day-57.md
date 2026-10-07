# Day 57 — Datastore modelleri, sharding ve federation

Durum: **Planlandı**. Bu gün eğitim milestone'ıdır; birden fazla takvim gününe yayılabilir. Çalışan kod veya doğrulanmış sonuç henüz yoktur.

## Önkoşul ve kapsam

[Day 56](day-56.md) kapanır; önceki günün birikimli implementation snapshot'ından `day/57` türetilir. Emlak repo/planı değiştirilmez. [System Design matrisi](../coverage/system-design-coverage.md) ve [uygulama sözleşmesi](../coverage/mandatory-implementation-contract.md) esas alınır.

## Öğrenme çıktısı

Datastore sınıfını sorgu/invariant gereksinimine göre seç; federation, replication ve sharding farklı topolojilerdir.

Roadmap etiketleri: `Databases`, `SQL vs NoSQL`, `Sharding`, `Federation`, `Denormalization`, `SQL Tuning`, `Key-Value Store`, `Document Store`, `Wide Column Store`, `Graph Databases`, `Materialized View`, `Index Table`.

## Görevler

1. Mevcut key-value (emlak Redis/araç Memcached), document (emlak MongoDB/araç CouchDB), wide-column (emlak Cassandra Day 10/20) ve graph (araç Neo4j Day 19) görev/evidence'ını kontrol et. Wide-column sorgu/partition deneyinin evidence'ı yoksa araçta izole Cassandra fixture'ı gerçekten uygula; karşılaştırma yeterli değildir.
2. Day 11/37 query planlarını kullan; EXPLAIN, indeks, N+1 ve denormalized projection önce/sonra ölç. MariaDB booking canonical kalır; türetilmiş modelin repair/rebuild yolunu test et.
3. İzole iki MariaDB shard ve Java router ile immutable fixture rental ID'sinden shard ownership seç; hot shard, route miss ve bir shard kesintisini çalıştır. Cross-shard transaction vaat etme; gerçek booking sistemini bu lab'a sessiz taşıma.
4. Database federation için şube metadata + ayrı rental aggregate owner'larını bir read aggregator ile birleştir; latency/failure/partial result sözleşmesini açıkla. Bu GraphQL federation özelliği değildir.
5. Index Table ile arama anahtarından owner ID'ye lookup; Materialized View ile rental summary oluştur. Update lag, delete ve rebuild deneylerini çalıştır; Day 60 event log ile gerekirse aynı fixture'ı paylaş.
6. SQL/NoSQL ve store seçim tablosunu sadece ürün adıyla değil consistency, transaction boundary, query, işletim ve resource gerekçeleriyle tamamla.

## Planlanan dosyalar

- `labs/system-design/sharding/`
- `labs/system-design/federation/`
- `docs/architecture/data-topology.md`
- `docs/evidence/day-57/` — exact komut, sürüm, fixture, ölçüm koşulları, expected/actual ve recovery.

Bunlar implementation sırasında oluşturulacak dosya/klasörlerdir; mevcut integration kanıtı değildir.

## Commit sırası

1. `docs(day-57): gereksinim sahiplik ve failure sözleşmesini tanımla`
2. `feat(day-57): temsilî lab ve gerekli adapterları uygula`
3. `test(day-57): başarı hata ve toparlanmayı doğrula`
4. `docs(day-57): ölçüm evidence ve runbookları kapat`

Mevcut verified implementation yeterliyse aynı sorumluluk için yeni ürün/boş feat commit oluşturulmaz; gerçek evidence ve eksik testler bağlanır. Test önce correctness/hata sözleşmesini, sonra anlamlı performance hipotezini doğrular.

## Doğrulama ve kapanış

- [ ] Yanlış shard'a yazı ve cross-owner mutable state oluşmaz; shard outage davranışı belgelenir.
- [ ] Index/view canonical veriden rebuild olur; federation kısmi hata cevabı sözleşmeye uyar; dört datastore sınıfı için runtime evidence vardır.
- [ ] Her roadmap etiketine öğrenme + temsilî uygulama + runtime doğrulama kanıtı bağlandı; yalnız karşılaştırma tamamlanma sayılmadı.
- [ ] Yeni/değişen Java kodu için uygun build/contract/integration check başarılı; lab local runtime üzerinde çalıştırıldı.
- [ ] Kaynak limiti, stop condition, cleanup ve geri dönüş adımı kaydedildi.
- [ ] Secret/PII/gerçek ödeme bilgisi evidence'a girmedi; sürüm/lisans/uyumluluk uygulama gününde kontrol edilip pin edildi.
- [ ] Coverage gerçek duruma göre güncellendi; Planlandı/Implemented/Verified ayrımı korundu.

Ücretli AWS/Azure/GCP veya model API gerekmiyor. Yerel fault injection/replica/edge/namespace sonuçları production scale, coğrafi HA veya SLA kanıtı değildir.
