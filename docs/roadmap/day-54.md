# Day 54 — Cache katmanları ve yazma stratejileri

Durum: **Planlandı**. Bu gün eğitim milestone'ıdır; birden fazla takvim gününe yayılabilir. Çalışan kod veya doğrulanmış sonuç henüz yoktur.

## Önkoşul ve kapsam

[Day 53](day-53.md) kapanır; önceki günün birikimli implementation snapshot'ından `day/54` türetilir. Emlak repo/planı değiştirilmez. [System Design matrisi](../coverage/system-design-coverage.md) ve [uygulama sözleşmesi](../coverage/mandatory-implementation-contract.md) esas alınır.

## Öğrenme çıktısı

Cache-aside, write-through, write-behind ve refresh-ahead hata/tutarlılık sözleşmelerini aynı non-critical read use-case üzerinde karşılaştır.

Roadmap etiketleri: `Caching`, `Refresh Ahead`, `Write-behind`, `Write-through`, `Cache Aside`, `Cache-Aside`, `Client Caching`, `Web Server Caching`, `Database Caching`, `Application Caching`.

## Görevler

1. Day 15 Memcached/HTTP cache lab'ını genişlet; ayrı profillerde cache-aside, write-through ve refresh-ahead uygula. TTL, eviction, invalidation, stampede ve negative caching testleri ekle.
2. Write-behind yalnız türetilmiş eğitim sayacı için kullanılsın. Accepted cevabından önce durable queue'ya yaz; pending ile persisted durumunu ayır. Booking correctness kaynağı cache olmaz.
3. Consumer crash, duplicate/reordered delivery ve retry sonrası write-behind replay/idempotency uygula; queue retention ve kalıcı hata davranışını kaydet.
4. Client cache: ETag/304/Cache-Control; web server cache: Nginx; application cache: Memcached; database cache: MariaDB buffer pool cold/warm gözlemi. Database buffer'ını application cache ile eşitleme.
5. Day 52 CDN cache evidence'ını bağla; private içerik, freshness isteyen request ve cache outage için doğru fallback/rejection seç.

## Planlanan dosyalar

- `labs/system-design/cache-strategies/`
- `docs/architecture/cache-contracts.md`
- `docs/evidence/day-54/` — exact komut, sürüm, fixture, ölçüm koşulları, expected/actual ve recovery.

Bunlar implementation sırasında oluşturulacak dosya/klasörlerdir; mevcut integration kanıtı değildir.

## Commit sırası

1. `docs(day-54): gereksinim sahiplik ve failure sözleşmesini tanımla`
2. `feat(day-54): temsilî lab ve gerekli adapterları uygula`
3. `test(day-54): başarı hata ve toparlanmayı doğrula`
4. `docs(day-54): ölçüm evidence ve runbookları kapat`

Mevcut verified implementation yeterliyse aynı sorumluluk için yeni ürün/boş feat commit oluşturulmaz; gerçek evidence ve eksik testler bağlanır. Test önce correctness/hata sözleşmesini, sonra anlamlı performance hipotezini doğrular.

## Doğrulama ve kapanış

- [ ] Her strateji için success, cache loss, stale read ve invalidation sonucu ayrı ölçülür.
- [ ] Write-behind durable kabulü crash sonrası geri gelir; booking invariant cache kaybında korunur; private response sızmaz.
- [ ] Her roadmap etiketine öğrenme + temsilî uygulama + runtime doğrulama kanıtı bağlandı; yalnız karşılaştırma tamamlanma sayılmadı.
- [ ] Yeni/değişen Java kodu için uygun build/contract/integration check başarılı; lab local runtime üzerinde çalıştırıldı.
- [ ] Kaynak limiti, stop condition, cleanup ve geri dönüş adımı kaydedildi.
- [ ] Secret/PII/gerçek ödeme bilgisi evidence'a girmedi; sürüm/lisans/uyumluluk uygulama gününde kontrol edilip pin edildi.
- [ ] Coverage gerçek duruma göre güncellendi; Planlandı/Implemented/Verified ayrımı korundu.

Ücretli AWS/Azure/GCP veya model API gerekmiyor. Yerel fault injection/replica/edge/namespace sonuçları production scale, coğrafi HA veya SLA kanıtı değildir.
