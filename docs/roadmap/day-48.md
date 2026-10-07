# Day 48 — Backend/Full Stack ara coverage audit

Durum: **Planlandı**. Day bir milestone'dır; takvim günü sınırı yoktur.

## Önkoşul ve scope

[Day 47](day-47.md) kapanır; cumulative implementation branch'inden `day/48` türetilir. Bu gün başka datastore'ların sahipliğini devralmaz. Ortak kararlar [Project Decisions](../PROJECT-DECISIONS.md) belgesindedir.

## Görevler

1. Roadmap snapshot içindeki her sarı/mor/mavi başlığa evidence bağla; Gri/yeşil comparison seviyelerini açık tut; açık gap varsa kapanışı tam ilan etme.
2. Requirement, alternatif, data/resource ownership, failure mode ve version compatibility kararını ADR'ye kaydet.
3. Mevcut dosya yapısında minimal gerçek use-case'i uygula; ihtiyaç yoksa aynı responsibility için ikinci ürün ekleme.
4. Planlanan≠implemented≠verified; snapshot diff ve karşılaştırma raporu; mesleki unvan otomatik kazanıldı iddiası yok.
5. Öğrenme notunu, runbook'u, ölçüm koşullarını ve karşılaştırma sonucunu güncelle.

## Planlanan dosyalar

- `docs/coverage/backend-full-stack-checkpoint.md`
- `docs/coverage/capability-status.md`
- `docs/evidence/day-48/` — secretsız komut, çıktı, sürüm ve ölçümler; bu yollar henüz implementation değildir.

## Commit sırası

1. `docs(day-48): scope ve sahiplik kararını tanımla`
2. `feat(day-48): temsilî çalışma ve adapterları uygula`
3. `test(day-48): başarı hata ve toparlanmayı doğrula`
4. `docs(day-48): actual evidence ve runbookları kapat`

Dosya ve sorumluluklar implementation sırasında incelenir; task yapılmadan boş commit oluşturulmaz.

## Kapanış ölçütleri

- [ ] Bu günün öğrenme konuları proje örneğiyle açıklanabiliyor.
- [ ] Gerekli build/CI başarılı; sonra local runtime/API/browser doğrulaması yapıldı.
- [ ] Yukarıdaki başarı/hata senaryoları gerçek runtime üzerinde gözlendi; expected/actual ve recovery kaydedildi.
- [ ] Secret/PII/anahtar ve gerçek ödeme bilgisi Git/evidence içine girmedi.
- [ ] Sürüm/lisans/uyumluluk ve RAM/CPU/disk bütçesi kaydedildi.
- [ ] İki proje coverage satırları gerçek duruma göre güncellendi; kanıt olmadan Verified işaretlenmedi.

Yerel emulator, benchmark ve toy lab sonucu production SLA/HA/scale kanıtı değildir. Ücretli cloud/model API zorunluluğu yoktur.


## Zorunlu kapsam denetimi

- Emlak Day 1–85 planı değiştirilmeden, iki proje matrisindeki her sarı/mor/mavi konu için en az bir gerçek implementation ve runtime test kanıtı bulunur.
- Başlık yalnız comparison/ADR/dependency üzerinden tamamlandı sayılamaz. Eksik satır varsa gap ve milestone owner belirlenir; ara kapanış tamamlandı ilan edilmez.
- “Bir dil seç” gibi seçim semantiği ve mavi linked roadmap scope sınırı uygulanır; [uygulama sözleşmesi](../coverage/mandatory-implementation-contract.md) esas alınır.
- Claude Code yerel uygulaması ve ek TimescaleDB/CouchDB/SQLite alternatifleri özellikle kontrol edilir.


## Full Stack kapsam audit'i

[Full Stack matrisi](../coverage/full-stack-coverage.md) ve snapshot'ındaki 17 uygulanabilir ana konu, checkpoint'ler ve mavi Frontend/Backend/DevOps için evidence kontrol edilir. Emlak baseline PostgreSQL ve planlı Redis/Linux/Ansible/Terraform uygulama kanıtlarına link verilir; sadece plan varlığı yeterli değildir. Eksik owner görevi araç kiralamada kalır. Node.js backend ve Basic AWS Services/Route53/SES/EC2/VPC/S3/mavi AWS açık istisnadır. npm ve Tailwind için local build araçları bu istisnayı server-side Node scope'una dönüştürmez.


## System Design fazına geçiş

Bu gün Backend/Full Stack kapsamının ara audit'idir; bütün programın final audit'i [Day 64](day-64.md) olarak yapılır. [Day 49](day-49.md) ile System Design genişletmesi başlar. Day 48'de System Design tamamlandı iddiası yapılmaz; açık gap'ler yeni günlük owner'lara aktarılır.
