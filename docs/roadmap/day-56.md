# Day 56 — TCP/UDP, RPC ve API iletişim sözleşmeleri

Durum: **Planlandı**. Bu gün eğitim milestone'ıdır; birden fazla takvim gününe yayılabilir. Çalışan kod veya doğrulanmış sonuç henüz yoktur.

## Önkoşul ve kapsam

[Day 55](day-55.md) kapanır; önceki günün birikimli implementation snapshot'ından `day/56` türetilir. Emlak repo/planı değiştirilmez. [System Design matrisi](../coverage/system-design-coverage.md) ve [uygulama sözleşmesi](../coverage/mandatory-implementation-contract.md) esas alınır.

## Öğrenme çıktısı

Transport garantileri, framing, API modeli ve business idempotency farklı katmanlardır.

Roadmap etiketleri: `Communication`, `HTTP`, `TCP`, `UDP`, `RPC`, `REST`, `gRPC`, `GraphQL`, `Idempotent Operations`.

## Görevler

1. Java sockets ile bounded TCP client/server yaz; framing, partial read, timeout, connection close ve payload limit uygula.
2. Java UDP fixture'ında duplicate/loss/reorder enjekte et; uygulama-level sequence/timeout ile etkilerini göster. UDP için güvenilir teslim varsayma.
3. Mevcut REST/gRPC/GraphQL read API'lerini aynı araç görünümüne bağla; deadline, status/error mapping, pagination ve authorization sözleşmelerini test et. Yeni canonical owner yaratma.
4. Bir rezervasyon komutunda durable Idempotency-Key + request hash uygula/yeniden kullan; tekrar, eşzamanlı tekrar, farklı payload ve cevap kaybı sonrası retry deneylerini çalıştır.
5. Protocol-specific ölçümlerde bağlantı maliyeti, byte ve latency koşullarını açıkla; tek benchmark'tan genel ürün üstünlüğü çıkarma.

## Planlanan dosyalar

- `labs/system-design/protocols/`
- `docs/architecture/communication-contracts.md`
- `docs/evidence/day-56/` — exact komut, sürüm, fixture, ölçüm koşulları, expected/actual ve recovery.

Bunlar implementation sırasında oluşturulacak dosya/klasörlerdir; mevcut integration kanıtı değildir.

## Commit sırası

1. `docs(day-56): gereksinim sahiplik ve failure sözleşmesini tanımla`
2. `feat(day-56): temsilî lab ve gerekli adapterları uygula`
3. `test(day-56): başarı hata ve toparlanmayı doğrula`
4. `docs(day-56): ölçüm evidence ve runbookları kapat`

Mevcut verified implementation yeterliyse aynı sorumluluk için yeni ürün/boş feat commit oluşturulmaz; gerçek evidence ve eksik testler bağlanır. Test önce correctness/hata sözleşmesini, sonra anlamlı performance hipotezini doğrular.

## Doğrulama ve kapanış

- [ ] TCP frame sınırları/partial read ve UDP kayıp sırası gözlenir; public port veya dış hedef gerekmez.
- [ ] Retry booking'i çoğaltmaz; farklı payload aynı key ile reddedilir; her API'de yetkisiz/timeout isteği doğru sonlanır.
- [ ] Her roadmap etiketine öğrenme + temsilî uygulama + runtime doğrulama kanıtı bağlandı; yalnız karşılaştırma tamamlanma sayılmadı.
- [ ] Yeni/değişen Java kodu için uygun build/contract/integration check başarılı; lab local runtime üzerinde çalıştırıldı.
- [ ] Kaynak limiti, stop condition, cleanup ve geri dönüş adımı kaydedildi.
- [ ] Secret/PII/gerçek ödeme bilgisi evidence'a girmedi; sürüm/lisans/uyumluluk uygulama gününde kontrol edilip pin edildi.
- [ ] Coverage gerçek duruma göre güncellendi; Planlandı/Implemented/Verified ayrımı korundu.

Ücretli AWS/Azure/GCP veya model API gerekmiyor. Yerel fault injection/replica/edge/namespace sonuçları production scale, coğrafi HA veya SLA kanıtı değildir.
