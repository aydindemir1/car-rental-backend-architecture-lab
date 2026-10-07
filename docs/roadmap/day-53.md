# Day 53 — L4/L7 load balancing ve horizontal scaling

Durum: **Planlandı**. Bu gün eğitim milestone'ıdır; birden fazla takvim gününe yayılabilir. Çalışan kod veya doğrulanmış sonuç henüz yoktur.

## Önkoşul ve kapsam

[Day 52](day-52.md) kapanır; önceki günün birikimli implementation snapshot'ından `day/53` türetilir. Emlak repo/planı değiştirilmez. [System Design matrisi](../coverage/system-design-coverage.md) ve [uygulama sözleşmesi](../coverage/mandatory-implementation-contract.md) esas alınır.

## Öğrenme çıktısı

Reverse proxy rolü ile load balancing işlevini ayır; TCP connection ve HTTP request dağıtımı aynı ölçüm değildir.

Roadmap etiketleri: `Load Balancers`, `LB vs Reverse Proxy`, `Load Balancing Algorithms`, `Layer 7 Load Balancing`, `Layer 4 Load Balancing`, `Horizontal Scaling`.

## Görevler

1. İzole HAProxy TCP profili ile L4; mevcut Nginx HTTP profili ile L7 dağıtımı uygula. Bunlar ayrı protocol deneyleri; aynı giriş üzerinde competing proxy/controller kurulmaz.
2. Round robin, least connections ve ağırlıklı dağıtımı destekleyen profilleri dene; backend kimliği, connection/request sayısını ölç. Sticky session'ın stateless tasarıma etkisini açıkla.
3. HTTP host/path routing ile TCP passthrough farkını göster; TLS termination sorumluluğunu Day 14 ile bağla.
4. Birden üçe replica değiştir; keep-alive, connection reuse ve uneven load etkilerini ölç. Kapasiteyi yalnız replica sayısı ile kanıtlanmış sayma.
5. Backend'i durdur, drain et ve geri al; health detection, yeniden dağıtım ve error window kaydet.

## Planlanan dosyalar

- `infra/labs/load-balancing/`
- `labs/system-design/load-distribution/`
- `docs/evidence/day-53/` — exact komut, sürüm, fixture, ölçüm koşulları, expected/actual ve recovery.

Bunlar implementation sırasında oluşturulacak dosya/klasörlerdir; mevcut integration kanıtı değildir.

## Commit sırası

1. `docs(day-53): gereksinim sahiplik ve failure sözleşmesini tanımla`
2. `feat(day-53): temsilî lab ve gerekli adapterları uygula`
3. `test(day-53): başarı hata ve toparlanmayı doğrula`
4. `docs(day-53): ölçüm evidence ve runbookları kapat`

Mevcut verified implementation yeterliyse aynı sorumluluk için yeni ürün/boş feat commit oluşturulmaz; gerçek evidence ve eksik testler bağlanır. Test önce correctness/hata sözleşmesini, sonra anlamlı performance hipotezini doğrular.

## Doğrulama ve kapanış

- [ ] Her algoritmada backend dağılımı gerçek sayımla raporlanır; eşit trafik beklentisinin koşulları yazılır.
- [ ] Unhealthy backend çıkarılır; session ve in-flight istek davranışı, toparlanma ve kaynak bütçesi belgelenir.
- [ ] Her roadmap etiketine öğrenme + temsilî uygulama + runtime doğrulama kanıtı bağlandı; yalnız karşılaştırma tamamlanma sayılmadı.
- [ ] Yeni/değişen Java kodu için uygun build/contract/integration check başarılı; lab local runtime üzerinde çalıştırıldı.
- [ ] Kaynak limiti, stop condition, cleanup ve geri dönüş adımı kaydedildi.
- [ ] Secret/PII/gerçek ödeme bilgisi evidence'a girmedi; sürüm/lisans/uyumluluk uygulama gününde kontrol edilip pin edildi.
- [ ] Coverage gerçek duruma göre güncellendi; Planlandı/Implemented/Verified ayrımı korundu.

Ücretli AWS/Azure/GCP veya model API gerekmiyor. Yerel fault injection/replica/edge/namespace sonuçları production scale, coğrafi HA veya SLA kanıtı değildir.
