# Day 49 — System Design süreci ve sayısal hedefler

Durum: **Planlandı**. Bu gün eğitim milestone'ıdır; birden fazla takvim gününe yayılabilir. Çalışan kod veya doğrulanmış sonuç henüz yoktur.

## Önkoşul ve kapsam

[Day 48](day-48.md) kapanır; önceki günün birikimli implementation snapshot'ından `day/49` türetilir. Emlak repo/planı değiştirilmez. [System Design matrisi](../coverage/system-design-coverage.md) ve [uygulama sözleşmesi](../coverage/mandatory-implementation-contract.md) esas alınır.

## Öğrenme çıktısı

Gereksinimden kapasite modeline geç; latency/throughput, performance/scalability ve partition sırasında availability/consistency tercihlerini ayır.

Roadmap etiketleri: `Introduction`, `What is System Design?`, `How to approach System Design?`, `Performance vs Scalability`, `Latency vs Throughput`, `Availability vs Consistency`, `CAP Theorem`, `Availability in Numbers`.

## Görevler

1. Arama, rezervasyon ve iade için functional/non-functional requirements, veri büyümesi, RPS, payload ve concurrency varsayımları çıkar. Sayıları tahmin/ölçüm olarak ayrı işaretle.
2. Day 30 yük deneyini aynı veri ve donanımla tekrar kullan: p50/p95/p99 latency, throughput, hata ve saturation kaydet. Tek worker ile artan concurrency; ardından iki worker ile aynı trafik deneyini uygula.
3. SLO ve availability yüzdesinden pencere başına izin verilen kesinti/error budget hesaplayan Java testli bir araç yaz; request-based ve time-based availability farkını göster.
4. CAP için yerel iki bileşen arasındaki bağlantıyı kontrollü kes; booking komutunun doğruluk için reddedilmesi ile stale katalog okumasının sürdürülmesini göster. CAP'i normal işletimde 'üçünden herhangi ikisini seç' sloganına indirgeme.
5. İki mimari seçeneği capacity, maliyet yerine yerel resource bütçesi, correctness ve operasyon yüküyle değerlendir; ADR'de karar, alternatif ve kararın değişeceği koşulu yaz.

## Planlanan dosyalar

- `docs/architecture/system-design-requirements.md`
- `labs/system-design/capacity/`
- `docs/adr/system-design-baseline.md`
- `docs/evidence/day-49/` — exact komut, sürüm, fixture, ölçüm koşulları, expected/actual ve recovery.

Bunlar implementation sırasında oluşturulacak dosya/klasörlerdir; mevcut integration kanıtı değildir.

## Commit sırası

1. `docs(day-49): gereksinim sahiplik ve failure sözleşmesini tanımla`
2. `feat(day-49): temsilî lab ve gerekli adapterları uygula`
3. `test(day-49): başarı hata ve toparlanmayı doğrula`
4. `docs(day-49): ölçüm evidence ve runbookları kapat`

Mevcut verified implementation yeterliyse aynı sorumluluk için yeni ürün/boş feat commit oluşturulmaz; gerçek evidence ve eksik testler bağlanır. Test önce correctness/hata sözleşmesini, sonra anlamlı performance hipotezini doğrular.

## Doğrulama ve kapanış

- [ ] Yük eğrisi ve iki worker sonucu aynı koşullarda tekrar üretilebilir; hızlanma yoksa bottleneck açıkça raporlanır.
- [ ] Partition deneyinde kabul edilen/reddedilen işlemler ve toparlanma gözlenir; SLA sağlandı iddiası yerine ölçülen pencere yazılır.
- [ ] Her roadmap etiketine öğrenme + temsilî uygulama + runtime doğrulama kanıtı bağlandı; yalnız karşılaştırma tamamlanma sayılmadı.
- [ ] Yeni/değişen Java kodu için uygun build/contract/integration check başarılı; lab local runtime üzerinde çalıştırıldı.
- [ ] Kaynak limiti, stop condition, cleanup ve geri dönüş adımı kaydedildi.
- [ ] Secret/PII/gerçek ödeme bilgisi evidence'a girmedi; sürüm/lisans/uyumluluk uygulama gününde kontrol edilip pin edildi.
- [ ] Coverage gerçek duruma göre güncellendi; Planlandı/Implemented/Verified ayrımı korundu.

Ücretli AWS/Azure/GCP veya model API gerekmiyor. Yerel fault injection/replica/edge/namespace sonuçları production scale, coğrafi HA veya SLA kanıtı değildir.
