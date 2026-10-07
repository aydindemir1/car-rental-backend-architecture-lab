# Day 65 — Python ve Go ile operasyon araçları

Durum: **Planlandı**. Bu gün eğitim milestone'ıdır; tek takvim günü sınırı yoktur. Plan belgesi çalışan ürün/evidence değildir.

## Önkoşul ve kapsam

[Day 64](day-64.md) kapanır; birikimli implementation snapshot'ından `day/65` türetilir. Emlak repo/85 günlük planında değişiklik yapılmaz. [DevOps ortak kararları](../DEVOPS-ROADMAP-EXTENSION.md), [kapsam matrisi](../coverage/devops-coverage.md) ve [uygulama sözleşmesi](../coverage/mandatory-implementation-contract.md) geçerlidir.

## Öğrenme ve uygulama görevleri

Roadmap etiketleri: `Learn a Programming Language`, `Python`, `Go`.

1. Backend Java/Spring olarak kalır. Python ile deployment manifest/evidence envanteri okuyup schema/required field doğrulayan, secretsız JSON raporu ve anlamlı exit code üreten CLI yaz.
2. Go ile HTTP health/readiness hedeflerini context deadline, bounded concurrency ve cancellation ile yoklayan CLI yaz. Hedefler sadece izin verilen local endpoint listesinden gelsin.
3. Dosya/HTTP hatası, malformed input, unreachable endpoint, timeout, shutdown ve kaynak cleanup testlerini çalıştır. Dependency lock/versiyon, Python venv ve Go module dosyalarını kaydet.
4. Bu iki mor dil DevOps araçlarında gerçekten uygulanır; Java backend'in başka dile taşınması gerekmez. Ruby/Rust ve server-side Node seçeneklerini requirement bazında karşılaştır; önceki Node backend istisnasını koru.

## Planlanan dosyalar

- `tools/ops/python-inventory/`
- `tools/ops/go-probe/`
- `docs/evidence/day-65/` — exact komut, sürüm/edition, donanım, fixture, expected/actual sonuç ve recovery.

Bu yollar aday implementation dosyalarıdır; dosyanın varlığı Integration/Verified anlamına gelmez.

## Commit sırası

1. `docs(day-65): gereksinim sahiplik ve local kapsamı tanımla`
2. `feat(day-65): temsilî operasyon lab ve adapterlarını uygula`
3. `test(day-65): başarı hata ve toparlanmayı doğrula`
4. `docs(day-65): evidence runbook ve karşılaştırmayı kapat`

Var olan verified uygulama yeterliyse tekrar ürün veya boş feat commit oluşturulmaz; mevcut SHA/evidence ve gereken yeni testler bağlanır. Engellenen SaaS/provider için karşılaştırma commit'i literal runtime uygulaması gibi adlandırılmaz.

## Doğrulama ve kapanış

- [ ] Python malformed/eksik input için hatalı exit code, geçerli fixture için deterministik rapor üretir.
- [ ] Go timeout/cancel sırasında goroutine/connection sızıntısı üretmez; concurrency limiti gerçek ölçümle doğrulanır.
- [ ] Required başlıklara owner/öğrenme/implementation/test evidence bağlandı; engeller explicit gap veya kapsam istisnası olarak kaldı.
- [ ] Yeni/değişen kod için uygun build/contract/integration check başarılı; ardından local runtime çalıştırıldı.
- [ ] Compatibility, sürüm, ücretsiz edition/lisans ve resource bütçesi gün başında kontrol edilip pin edildi.
- [ ] İzole namespace/VM/profile sahipliği, stop condition, cleanup ve recovery kaydedildi.
- [ ] Secret/key/token/PII Git'e girmedi; untrusted CI publishing/deploy yetkisine erişmedi.
- [ ] Matris gerçek duruma güncellendi; plan veya local emulator sonucu managed-service Verified yapılmadı.

Ücretli AWS/Azure/GCP/HCP/SaaS/trial şartı yoktur; cloud hesap/kaynakları otomatik oluşturulmaz. Yerel lab gerçek production SLA, coğrafi HA veya mesleki unvan kanıtı değildir.
