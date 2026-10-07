# Day 52 — DNS, pull/push CDN ve static hosting

Durum: **Planlandı**. Bu gün eğitim milestone'ıdır; birden fazla takvim gününe yayılabilir. Çalışan kod veya doğrulanmış sonuç henüz yoktur.

## Önkoşul ve kapsam

[Day 51](day-51.md) kapanır; önceki günün birikimli implementation snapshot'ından `day/52` türetilir. Emlak repo/planı değiştirilmez. [System Design matrisi](../coverage/system-design-coverage.md) ve [uygulama sözleşmesi](../coverage/mandatory-implementation-contract.md) esas alınır.

## Öğrenme çıktısı

DNS çözümleme ile içerik dağıtımını ayır; pull origin fetch ve push önceden içerik dağıtımını yerel edge lab'ında uygula.

Roadmap etiketleri: `Domain Name System`, `Content Delivery Networks`, `Pull CDNs`, `Push CDNs`, `Static Content Hosting`, `CDN Caching`.

## Görevler

1. Day 02–03 temeli üzerine CoreDNS yerel zone kur; A/CNAME, TTL, NXDOMAIN, resolver cache ve endpoint değişimi deneylerini kaydet. Domain satın alma gerekmez.
2. Day 14 Nginx origin ve iki Nginx edge instance kur. Pull profilinde cache miss origin'e gitsin; hit origin'e gitmesin; cache key/TTL/invalidation açıklansın.
3. Push profilinde build'in hash'li statik artifact'larını iki edge'e önceden dağıt; manifest/version doğrula. Yeni içerik rollout ve eski içerik cleanup adımlarını uygula.
4. Public immutable static asset'ler ile authenticated/private API response'larını ayır; kullanıcılar arası cache sızıntısını negatif test et.
5. Origin kesintisi, eski asset referansı ve yanlış DNS hedefinden toparlanmayı göster. Bu yerel edge simülasyonudur; global CDN/geographic latency kanıtı değildir.

## Planlanan dosyalar

- `infra/labs/dns/`
- `infra/labs/cdn/`
- `docs/runbooks/static-content-distribution.md`
- `docs/evidence/day-52/` — exact komut, sürüm, fixture, ölçüm koşulları, expected/actual ve recovery.

Bunlar implementation sırasında oluşturulacak dosya/klasörlerdir; mevcut integration kanıtı değildir.

## Commit sırası

1. `docs(day-52): gereksinim sahiplik ve failure sözleşmesini tanımla`
2. `feat(day-52): temsilî lab ve gerekli adapterları uygula`
3. `test(day-52): başarı hata ve toparlanmayı doğrula`
4. `docs(day-52): ölçüm evidence ve runbookları kapat`

Mevcut verified implementation yeterliyse aynı sorumluluk için yeni ürün/boş feat commit oluşturulmaz; gerçek evidence ve eksik testler bağlanır. Test önce correctness/hata sözleşmesini, sonra anlamlı performance hipotezini doğrular.

## Doğrulama ve kapanış

- [ ] Pull cold/hot isteklerinde origin hit sayısı değişir; push edge doğru hash'li artifact'ı sunar.
- [ ] TTL/NXDOMAIN ve private response testleri beklenen sonucu verir; rollout sonrası eski/yeni asset davranışı kaydedilir.
- [ ] Her roadmap etiketine öğrenme + temsilî uygulama + runtime doğrulama kanıtı bağlandı; yalnız karşılaştırma tamamlanma sayılmadı.
- [ ] Yeni/değişen Java kodu için uygun build/contract/integration check başarılı; lab local runtime üzerinde çalıştırıldı.
- [ ] Kaynak limiti, stop condition, cleanup ve geri dönüş adımı kaydedildi.
- [ ] Secret/PII/gerçek ödeme bilgisi evidence'a girmedi; sürüm/lisans/uyumluluk uygulama gününde kontrol edilip pin edildi.
- [ ] Coverage gerçek duruma göre güncellendi; Planlandı/Implemented/Verified ayrımı korundu.

Ücretli AWS/Azure/GCP veya model API gerekmiyor. Yerel fault injection/replica/edge/namespace sonuçları production scale, coğrafi HA veya SLA kanıtı değildir.
