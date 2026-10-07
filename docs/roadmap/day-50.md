# Day 50 — Weak, eventual ve strong consistency deneyleri

Durum: **Planlandı**. Bu gün eğitim milestone'ıdır; birden fazla takvim gününe yayılabilir. Çalışan kod veya doğrulanmış sonuç henüz yoktur.

## Önkoşul ve kapsam

[Day 49](day-49.md) kapanır; önceki günün birikimli implementation snapshot'ından `day/50` türetilir. Emlak repo/planı değiştirilmez. [System Design matrisi](../coverage/system-design-coverage.md) ve [uygulama sözleşmesi](../coverage/mandatory-implementation-contract.md) esas alınır.

## Öğrenme çıktısı

Tutarlılığı işlem ve veri sahibi bazında tanımla; transaction isolation, read-after-write ve replica freshness farklı garantilerdir.

Roadmap etiketleri: `Consistency Patterns`, `Weak Consistency`, `Eventual Consistency`, `Strong Consistency`.

## Görevler

1. Kayıp tolere edilen geçici görüntülenme sayacını weak consistency örneği yap; reset/kayıp ile canonical rezervasyon kaybını karıştırma.
2. Day 24 projection'ını geciktir; API'de version/as-of bilgisi ve stale read davranışını ölç. Out-of-order/duplicate event kontrolü ve eventual convergence uygula.
3. Day 10–11 canonical booking owner üzerinde aynı araç/tarih için eşzamanlı iki komutu transaction/constraint ile koru. Onaylanmış yazmadan sonra owner'dan okumanın garantisini belgelerle ve concurrency testiyle sınırla.
4. Replica lag sırasında read-after-write isteyen isteği owner'a yönlendir ya da açıkça reddet; replica ve cache üzerinden strong/linearizable distributed read garantisi iddia etme.
5. Partition ve iyileşmede beklenen sonuç, elapsed time ve invariant ihlali sayısını kaydet.

## Planlanan dosyalar

- `labs/system-design/consistency/`
- `docs/architecture/consistency-contracts.md`
- `docs/evidence/day-50/` — exact komut, sürüm, fixture, ölçüm koşulları, expected/actual ve recovery.

Bunlar implementation sırasında oluşturulacak dosya/klasörlerdir; mevcut integration kanıtı değildir.

## Commit sırası

1. `docs(day-50): gereksinim sahiplik ve failure sözleşmesini tanımla`
2. `feat(day-50): temsilî lab ve gerekli adapterları uygula`
3. `test(day-50): başarı hata ve toparlanmayı doğrula`
4. `docs(day-50): ölçüm evidence ve runbookları kapat`

Mevcut verified implementation yeterliyse aynı sorumluluk için yeni ürün/boş feat commit oluşturulmaz; gerçek evidence ve eksik testler bağlanır. Test önce correctness/hata sözleşmesini, sonra anlamlı performance hipotezini doğrular.

## Doğrulama ve kapanış

- [ ] Weak sayaç kaybı yalnız izin verilen non-critical veride görülür.
- [ ] Aynı araca çakışan iki kesinleşmiş booking oluşmaz; stale projection toparlanır; freshness isteyen read stale replica'ya sessiz yönlenmez.
- [ ] Her roadmap etiketine öğrenme + temsilî uygulama + runtime doğrulama kanıtı bağlandı; yalnız karşılaştırma tamamlanma sayılmadı.
- [ ] Yeni/değişen Java kodu için uygun build/contract/integration check başarılı; lab local runtime üzerinde çalıştırıldı.
- [ ] Kaynak limiti, stop condition, cleanup ve geri dönüş adımı kaydedildi.
- [ ] Secret/PII/gerçek ödeme bilgisi evidence'a girmedi; sürüm/lisans/uyumluluk uygulama gününde kontrol edilip pin edildi.
- [ ] Coverage gerçek duruma göre güncellendi; Planlandı/Implemented/Verified ayrımı korundu.

Ücretli AWS/Azure/GCP veya model API gerekmiyor. Yerel fault injection/replica/edge/namespace sonuçları production scale, coğrafi HA veya SLA kanıtı değildir.
