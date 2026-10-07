# Day 64 — Üç roadmap ve iki proje final audit

Durum: **Planlandı**. Bu gün eğitim milestone'ıdır; birden fazla takvim gününe yayılabilir. Çalışan kod veya doğrulanmış sonuç henüz yoktur.

## Önkoşul ve kapsam

[Day 63](day-63.md) kapanır; önceki günün birikimli implementation snapshot'ından `day/64` türetilir. Emlak repo/planı değiştirilmez. [System Design matrisi](../coverage/system-design-coverage.md) ve [uygulama sözleşmesi](../coverage/mandatory-implementation-contract.md) esas alınır.

## Öğrenme çıktısı

Planlanan kapsam ile uygulanmış/doğrulanmış kapsamı ayrı tut; bütün zorunlu başlıklara evidence bağla.

Roadmap etiketleri: `Backend`, `Software Architect`, `DevOps`.

## Görevler

1. Backend, Full Stack ve System Design snapshot/matrislerini birlikte denetle. Kullanıcının Node.js backend/Basic AWS istisnaları korunur; emlak planında değişiklik yapılmaz.
2. Her required node için owner, öğrenme notu, implementation commit, version, exact command, başarı/hata/recovery evidence'ını kaydet. Emlak plan satırı tek başına Verified değildir; eksik görev araç kiralamada açık kalır.
3. System Design tekrar eden etiketleri node ID bazında kontrol et; aynı pattern evidence'ı farklı occurrence'lara bağlanabilir, ürün sayısını artırmak gerekmez.
4. Backend için Java domain/API/persistence; Software Architect için requirement→ADR→pattern→failure/capacity değerlendirmesi; DevOps için build/deploy/monitor/restore gerçek uçtan uca evidence'ı birleştir. Mavi linkler başka roadmap'in bütün dallarını otomatik scope yapmaz.
5. Arama→booking→teslim/iade→async sonuç→projection→monitor→failure→restore akışını çalıştır; canonical ownership, SLO ölçüm koşulları ve veri doğruluğunu raporla.
6. Yeşil alternatiflerde chosen implementation/comparison ve gerekçeyi koru; her ürünü kurmak yerine farklı responsibility ve öğrenme çıktısını izle.
7. Snapshot diff, açık gap'ler, local/production sınırı ve sonraki eğitim önerilerini completion report'a yaz. Bu audit unvan veya production yetkinlik sertifikası değildir.

## Planlanan dosyalar

- `docs/coverage/completion-report.md`
- `docs/coverage/capability-status.md`
- `docs/evidence/day-64/`
- `docs/evidence/day-64/` — exact komut, sürüm, fixture, ölçüm koşulları, expected/actual ve recovery.

Bunlar implementation sırasında oluşturulacak dosya/klasörlerdir; mevcut integration kanıtı değildir.

## Commit sırası

1. `docs(day-64): gereksinim sahiplik ve failure sözleşmesini tanımla`
2. `feat(day-64): audit ve evidence doğrulama araçlarını uygula`
3. `test(day-64): başarı hata ve toparlanmayı doğrula`
4. `docs(day-64): ölçüm evidence ve runbookları kapat`

Mevcut verified implementation yeterliyse aynı sorumluluk için yeni ürün/boş feat commit oluşturulmaz; gerçek evidence ve eksik testler bağlanır. Test önce correctness/hata sözleşmesini, sonra anlamlı performance hipotezini doğrular.

## Doğrulama ve kapanış

- [ ] Her zorunlu kapsam satırının implementation/runtime kanıtı vardır ya da explicit gap'tir; gap varken tamamlama iddiası yapılmaz.
- [ ] E2E ve restore sonrası domain invariant korunur; deployment, versiyon ve ölçüm tekrar üretilebilir.
- [ ] Her roadmap etiketine öğrenme + temsilî uygulama + runtime doğrulama kanıtı bağlandı; yalnız karşılaştırma tamamlanma sayılmadı.
- [ ] Yeni/değişen Java kodu için uygun build/contract/integration check başarılı; lab local runtime üzerinde çalıştırıldı.
- [ ] Kaynak limiti, stop condition, cleanup ve geri dönüş adımı kaydedildi.
- [ ] Secret/PII/gerçek ödeme bilgisi evidence'a girmedi; sürüm/lisans/uyumluluk uygulama gününde kontrol edilip pin edildi.
- [ ] Coverage gerçek duruma göre güncellendi; Planlandı/Implemented/Verified ayrımı korundu.

Ücretli AWS/Azure/GCP veya model API gerekmiyor. Yerel fault injection/replica/edge/namespace sonuçları production scale, coğrafi HA veya SLA kanıtı değildir.
