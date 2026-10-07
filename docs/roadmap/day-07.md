# Day 07 — Java Spring build ve sınır standardı

Durum: **Planlandı**. Day bir milestone'dır; takvim günü sınırı yoktur.

## Önkoşul ve scope

[Day 6](day-06.md) kapanır; cumulative implementation branch'inden `day/07` türetilir. Bu gün başka datastore'ların sahipliğini devralmaz. Ortak kararlar [Project Decisions](../PROJECT-DECISIONS.md) belgesindedir.

## Görevler

1. Java/Spring Boot/Spring Cloud BOM ve Gradle sürümlerini resmi uyumluluğa göre pin et; package/dependency/test düzenini kur.
2. Requirement, alternatif, data/resource ownership, failure mode ve version compatibility kararını ADR'ye kaydet.
3. Mevcut dosya yapısında minimal gerçek use-case'i uygula; ihtiyaç yoksa aynı responsibility için ikinci ürün ekleme.
4. CI build/test ve architecture boundary kontrolü geçmeden runtime tamamlandı sayma.
5. Öğrenme notunu, runbook'u, ölçüm koşullarını ve karşılaştırma sonucunu güncelle.

## Planlanan dosyalar

- `settings.gradle`
- `build.gradle`
- `docs/standards/build.md`
- `docs/evidence/day-07/` — secretsız komut, çıktı, sürüm ve ölçümler; bu yollar henüz implementation değildir.

## Commit sırası

1. `docs(day-07): scope ve sahiplik kararını tanımla`
2. `feat(day-07): temsilî çalışma ve adapterları uygula`
3. `test(day-07): başarı hata ve toparlanmayı doğrula`
4. `docs(day-07): actual evidence ve runbookları kapat`

Dosya ve sorumluluklar implementation sırasında incelenir; task yapılmadan boş commit oluşturulmaz.

## Kapanış ölçütleri

- [ ] Bu günün öğrenme konuları proje örneğiyle açıklanabiliyor.
- [ ] Gerekli build/CI başarılı; sonra local runtime/API/browser doğrulaması yapıldı.
- [ ] Yukarıdaki başarı/hata senaryoları gerçek runtime üzerinde gözlendi; expected/actual ve recovery kaydedildi.
- [ ] Secret/PII/anahtar ve gerçek ödeme bilgisi Git/evidence içine girmedi.
- [ ] Sürüm/lisans/uyumluluk ve RAM/CPU/disk bütçesi kaydedildi.
- [ ] İki proje coverage satırları gerçek duruma göre güncellendi; kanıt olmadan Verified işaretlenmedi.

Yerel emulator, benchmark ve toy lab sonucu production SLA/HA/scale kanıtı değildir. Ücretli cloud/model API zorunluluğu yoktur.


## Full Stack ek görevi — collaborative work ve Java CLI

Git branch/merge/rebase farklarını disposable fixture üzerinde öğren; küçük PR, diff review ve conflict resolution senaryosu yap. Başka katkıcı yoksa solo simülasyon olduğunu açık yaz; sahte insan review kanıtı üretme. GitHub Actions check sonuçlarına PR'dan erişim göster.

CLI checkpoint'i için Java veya kısa ömürlü Spring Boot non-web maintenance CLI oluştur: synthetic fleet fixture validate/report, argüman/help, exit code, stdout/stderr ve invalid input testleri. Booking API'sini bypass eden direct canonical DB mutation aracı olmaz; Node.js CLI implementation eklenmez. Dosyalar: `labs/java-maintenance-cli/`, `docs/learning/git-collaboration.md`; commit: `feat(lab): Java bakım CLIsi ve collaborative Git deneyi ekle`.
