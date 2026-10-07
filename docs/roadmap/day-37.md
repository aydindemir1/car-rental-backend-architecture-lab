# Day 37 — DB indeks, replication ve partition lab

Durum: **Planlandı**. Day bir milestone'dır; takvim günü sınırı yoktur.

## Önkoşul ve scope

[Day 36](day-36.md) kapanır; cumulative implementation branch'inden `day/37` türetilir. Bu gün başka datastore'ların sahipliğini devralmaz. Ortak kararlar [Project Decisions](../PROJECT-DECISIONS.md) belgesindedir.

## Görevler

1. MariaDB index/EXPLAIN/N+1 deneylerini tamamla; izole replica failover lab ve bounded partition demo kur; gerçek scale sınırlarını açık yaz.
2. Requirement, alternatif, data/resource ownership, failure mode ve version compatibility kararını ADR'ye kaydet.
3. Mevcut dosya yapısında minimal gerçek use-case'i uygula; ihtiyaç yoksa aynı responsibility için ikinci ürün ekleme.
4. Replica lag/failover/lost-write varsayımları ve hotspot testleri; real production sharding verified at scale iddia etme.
5. Öğrenme notunu, runbook'u, ölçüm koşullarını ve karşılaştırma sonucunu güncelle.

## Planlanan dosyalar

- `labs/database-scale/`
- `docs/labs/db-scale.md`
- `docs/evidence/day-37/` — secretsız komut, çıktı, sürüm ve ölçümler; bu yollar henüz implementation değildir.

## Commit sırası

1. `docs(day-37): scope ve sahiplik kararını tanımla`
2. `feat(day-37): temsilî çalışma ve adapterları uygula`
3. `test(day-37): başarı hata ve toparlanmayı doğrula`
4. `docs(day-37): actual evidence ve runbookları kapat`

Dosya ve sorumluluklar implementation sırasında incelenir; task yapılmadan boş commit oluşturulmaz.

## Kapanış ölçütleri

- [ ] Bu günün öğrenme konuları proje örneğiyle açıklanabiliyor.
- [ ] Gerekli build/CI başarılı; sonra local runtime/API/browser doğrulaması yapıldı.
- [ ] Yukarıdaki başarı/hata senaryoları gerçek runtime üzerinde gözlendi; expected/actual ve recovery kaydedildi.
- [ ] Secret/PII/anahtar ve gerçek ödeme bilgisi Git/evidence içine girmedi.
- [ ] Sürüm/lisans/uyumluluk ve RAM/CPU/disk bütçesi kaydedildi.
- [ ] İki proje coverage satırları gerçek duruma göre güncellendi; kanıt olmadan Verified işaretlenmedi.

Yerel emulator, benchmark ve toy lab sonucu production SLA/HA/scale kanıtı değildir. Ücretli cloud/model API zorunluluğu yoktur.


## Yeşil alternatif uygulaması — SQLite

İzole bakım aracı/CLI lab'ında embedded SQLite ile migration, prepared statements, transaction rollback, foreign key enforcement ve concurrent writer davranışını uygula. MariaDB Booking canonical store olarak kalır. SQLite serverless embedded DB kavramı Knative serverless execution ile karıştırılmaz. File ownership/backup ve restart persistence testi kaydedilir; aynı veritabanı dosyasını cluster pod'ları arasında paylaşımlı OLTP store yapma. Aday dosya `labs/sqlite-maintenance/`; commit `feat(lab): SQLite embedded persistence ve concurrency davranışını doğrula`.
