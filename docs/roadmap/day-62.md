# Day 62 — Availability, deployment stamps ve geodes

Durum: **Planlandı**. Bu gün eğitim milestone'ıdır; birden fazla takvim gününe yayılabilir. Çalışan kod veya doğrulanmış sonuç henüz yoktur.

## Önkoşul ve kapsam

[Day 61](day-61.md) kapanır; önceki günün birikimli implementation snapshot'ından `day/62` türetilir. Emlak repo/planı değiştirilmez. [System Design matrisi](../coverage/system-design-coverage.md) ve [uygulama sözleşmesi](../coverage/mandatory-implementation-contract.md) esas alınır.

## Öğrenme çıktısı

Bağımsız tenant/capacity stamp'i ile aynı veriyi sunabilen geode arasındaki farkı yerel iki kurulumla uygula.

Roadmap etiketleri: `Availability`, `High Availability`, `Deployment Stamps`, `Geodes`.

## Görevler

1. İki local namespace/profile'da stamp-a/stamp-b kur; her stamp ayrı tenant fixture, kendi app/data/config/resource budget'ına sahip olsun. Tenant→stamp routing ve bir stamp'in kesintisini uygula.
2. Geode lab profilinde aynı read dataset'ini iki bağımsız app/data kümesine replicate et; her read node aynı read işlevini sunabilsin. Gecikme, stale version ve node seçimini göster.
3. Mutation için tek canonical home owner koru; diğer node command'ı owner'a route etsin. Owner erişilemezken correctness gerektiren write fail closed; read-only fallback freshness sözleşmesine uysun. Multi-region active-active write consensus uygulandı iddiası yoktur.
4. Bir app/data namespace kesintisi ve replica feed partition'ında routing, error window, convergence ve recovery ölç. Stamp/geode arasında trafik/veri sahipliği değişimini ADR ile açıkla.
5. Deployment ve fixture cleanup/restore komutlarını yaz. Tek host veya aynı cluster namespace'leri gerçek bağımsız fiziksel/geographic fault domain değildir; local demo ile production HA/SLA kanıtlanmaz.

## Planlanan dosyalar

- `infra/labs/deployment-stamps/`
- `infra/labs/geodes/`
- `docs/architecture/availability-topologies.md`
- `docs/evidence/day-62/` — exact komut, sürüm, fixture, ölçüm koşulları, expected/actual ve recovery.

Bunlar implementation sırasında oluşturulacak dosya/klasörlerdir; mevcut integration kanıtı değildir.

## Commit sırası

1. `docs(day-62): gereksinim sahiplik ve failure sözleşmesini tanımla`
2. `feat(day-62): temsilî lab ve gerekli adapterları uygula`
3. `test(day-62): başarı hata ve toparlanmayı doğrula`
4. `docs(day-62): ölçüm evidence ve runbookları kapat`

Mevcut verified implementation yeterliyse aynı sorumluluk için yeni ürün/boş feat commit oluşturulmaz; gerçek evidence ve eksik testler bağlanır. Test önce correctness/hata sözleşmesini, sonra anlamlı performance hipotezini doğrular.

## Doğrulama ve kapanış

- [ ] Bir tenant stamp hatası diğer tenant'ı etkilemez; misrouting testi veri sızıntısını engeller.
- [ ] İki geode read dataset'i converge eder; owner kesintisinde çakışan write kabul edilmez; RPO/RTO ve freshness sınırı ölçülür.
- [ ] Her roadmap etiketine öğrenme + temsilî uygulama + runtime doğrulama kanıtı bağlandı; yalnız karşılaştırma tamamlanma sayılmadı.
- [ ] Yeni/değişen Java kodu için uygun build/contract/integration check başarılı; lab local runtime üzerinde çalıştırıldı.
- [ ] Kaynak limiti, stop condition, cleanup ve geri dönüş adımı kaydedildi.
- [ ] Secret/PII/gerçek ödeme bilgisi evidence'a girmedi; sürüm/lisans/uyumluluk uygulama gününde kontrol edilip pin edildi.
- [ ] Coverage gerçek duruma göre güncellendi; Planlandı/Implemented/Verified ayrımı korundu.

Ücretli AWS/Azure/GCP veya model API gerekmiyor. Yerel fault injection/replica/edge/namespace sonuçları production scale, coğrafi HA veya SLA kanıtı değildir.
