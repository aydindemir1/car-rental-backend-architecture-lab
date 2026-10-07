# Day 51 — Failover, replication ve leader election

Durum: **Planlandı**. Bu gün eğitim milestone'ıdır; birden fazla takvim gününe yayılabilir. Çalışan kod veya doğrulanmış sonuç henüz yoktur.

## Önkoşul ve kapsam

[Day 50](day-50.md) kapanır; önceki günün birikimli implementation snapshot'ından `day/51` türetilir. Emlak repo/planı değiştirilmez. [System Design matrisi](../coverage/system-design-coverage.md) ve [uygulama sözleşmesi](../coverage/mandatory-implementation-contract.md) esas alınır.

## Öğrenme çıktısı

Replica, failover, leader seçimi ve fencing farklı sorumluluklardır; tek makine tatbikatı fiziksel HA kanıtı değildir.

Roadmap etiketleri: `Availability Patterns`, `Fail-Over`, `Replication`, `Leader Election`.

## Görevler

1. Day 37 replica lab'ını kullan; gecikme, primary kesintisi, promote ve yeniden katılım adımlarını explicit RPO/RTO ile uygula. Eski primary yazmaya kapatılmadan iki writable owner bırakma; otomatik failover iddiası gerekmez.
2. İki rapor coordinator'ı Kubernetes Lease üzerinden leader seçsin. Lease yenileme, timeout ve minimum RBAC'i uygula.
3. MariaDB'de monoton epoch/fencing token oluştur; protected sink daha eski token'ın yan etkisini transaction içinde reddetsin. Lease tek başına tüm split-brain risklerini çözmüş sayılmaz.
4. Lideri öldür; sonra eski lideri pause/partition sonrası geri getir. Duplicate schedule ve eski token'ın reddini gerçek sink kayıtlarından doğrula.
5. Endpoint health ile veri doğruluğunu ayrı izle; yeniden katılım ve rollback runbook'u yaz.

## Planlanan dosyalar

- `labs/system-design/failover/`
- `labs/system-design/leader-election/`
- `docs/runbooks/leader-and-replica-recovery.md`
- `docs/evidence/day-51/` — exact komut, sürüm, fixture, ölçüm koşulları, expected/actual ve recovery.

Bunlar implementation sırasında oluşturulacak dosya/klasörlerdir; mevcut integration kanıtı değildir.

## Commit sırası

1. `docs(day-51): gereksinim sahiplik ve failure sözleşmesini tanımla`
2. `feat(day-51): temsilî lab ve gerekli adapterları uygula`
3. `test(day-51): başarı hata ve toparlanmayı doğrula`
4. `docs(day-51): ölçüm evidence ve runbookları kapat`

Mevcut verified implementation yeterliyse aynı sorumluluk için yeni ürün/boş feat commit oluşturulmaz; gerçek evidence ve eksik testler bağlanır. Test önce correctness/hata sözleşmesini, sonra anlamlı performance hipotezini doğrular.

## Doğrulama ve kapanış

- [ ] Yeni lider devralır; stale liderin fenced işi kabul edilmez.
- [ ] Promotion sırasında acknowledged veri kaybı/lag ve downtime ölçülür; seçilen asynchronous replication için RPO=0 varsayılmaz.
- [ ] Her roadmap etiketine öğrenme + temsilî uygulama + runtime doğrulama kanıtı bağlandı; yalnız karşılaştırma tamamlanma sayılmadı.
- [ ] Yeni/değişen Java kodu için uygun build/contract/integration check başarılı; lab local runtime üzerinde çalıştırıldı.
- [ ] Kaynak limiti, stop condition, cleanup ve geri dönüş adımı kaydedildi.
- [ ] Secret/PII/gerçek ödeme bilgisi evidence'a girmedi; sürüm/lisans/uyumluluk uygulama gününde kontrol edilip pin edildi.
- [ ] Coverage gerçek duruma göre güncellendi; Planlandı/Implemented/Verified ayrımı korundu.

Ücretli AWS/Azure/GCP veya model API gerekmiyor. Yerel fault injection/replica/edge/namespace sonuçları production scale, coğrafi HA veya SLA kanıtı değildir.
