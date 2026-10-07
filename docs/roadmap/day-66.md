# Day 66 — Ubuntu, RHEL türevi ve FreeBSD işletim lab'ı

Durum: **Planlandı**. Bu gün eğitim milestone'ıdır; tek takvim günü sınırı yoktur. Plan belgesi çalışan ürün/evidence değildir.

## Önkoşul ve kapsam

[Day 65](day-65.md) kapanır; birikimli implementation snapshot'ından `day/66` türetilir. Emlak repo/85 günlük planında değişiklik yapılmaz. [DevOps ortak kararları](../DEVOPS-ROADMAP-EXTENSION.md), [kapsam matrisi](../coverage/devops-coverage.md) ve [uygulama sözleşmesi](../coverage/mandatory-implementation-contract.md) geçerlidir.

## Öğrenme ve uygulama görevleri

Roadmap etiketleri: `Operating System`, `Ubuntu / Debian`, `RHEL / Derivatives`, `FreeBSD`, `Linux`.

1. Emlak Day 46 Linux temelini yeniden kullan. Ubuntu/Debian ana host; ücretsiz RHEL türevi olarak Rocky Linux/AlmaLinux ve FreeBSD için ayrı local VM profilleri seç. Sürüm, lisans, image checksum ve donanım/virtualization desteğini doğrula.
2. Her OS'de paket kurma/güncelleme, kullanıcı/group, dosya izinleri, servis başlatma/durdurma, boot startup, process ve ağ inceleme görevlerini gerçekten yap. Linux systemd/journal ile FreeBSD rc/service/pkg farklarını kaydet.
3. Local eğitim health worker'ını minimum yetkiyle servis olarak çalıştır; servis crash/restart, port binding ve log erişim testlerini yap. FreeBSD Linux container gibi gösterilmez; kendi kernel'iyle VM gerekir.
4. VM snapshot/restore, resource budget ve cleanup işlemlerini doğrula. Ağır VM'ler sırayla açılır; hepsinin sürekli çalışması gerekmez.
5. Windows/PowerShell ve SUSE/OpenBSD/NetBSD yeşil seçeneklerini karşılaştır; mevcut kullanıcı Windows ortamında uygulanmış görevler varsa ayrı evidence bağla.

## Planlanan dosyalar

- `infra/labs/operating-systems/`
- `docs/runbooks/os-service-lifecycle.md`
- `docs/evidence/day-66/` — exact komut, sürüm/edition, donanım, fixture, expected/actual sonuç ve recovery.

Bu yollar aday implementation dosyalarıdır; dosyanın varlığı Integration/Verified anlamına gelmez.

## Commit sırası

1. `docs(day-66): gereksinim sahiplik ve local kapsamı tanımla`
2. `feat(day-66): temsilî operasyon lab ve adapterlarını uygula`
3. `test(day-66): başarı hata ve toparlanmayı doğrula`
4. `docs(day-66): evidence runbook ve karşılaştırmayı kapat`

Var olan verified uygulama yeterliyse tekrar ürün veya boş feat commit oluşturulmaz; mevcut SHA/evidence ve gereken yeni testler bağlanır. Engellenen SaaS/provider için karşılaştırma commit'i literal runtime uygulaması gibi adlandırılmaz.

## Doğrulama ve kapanış

- [ ] Üç OS ailesinde servis lifecycle ve yetkisiz dosya/port erişimi gerçek runtime'da gözlenir.
- [ ] Reboot sonrası beklenen servis/log durumu ve VM restore kanıtlıdır; VM kurulamazsa açık OS gap'i kalır.
- [ ] Required başlıklara owner/öğrenme/implementation/test evidence bağlandı; engeller explicit gap veya kapsam istisnası olarak kaldı.
- [ ] Yeni/değişen kod için uygun build/contract/integration check başarılı; ardından local runtime çalıştırıldı.
- [ ] Compatibility, sürüm, ücretsiz edition/lisans ve resource bütçesi gün başında kontrol edilip pin edildi.
- [ ] İzole namespace/VM/profile sahipliği, stop condition, cleanup ve recovery kaydedildi.
- [ ] Secret/key/token/PII Git'e girmedi; untrusted CI publishing/deploy yetkisine erişmedi.
- [ ] Matris gerçek duruma güncellendi; plan veya local emulator sonucu managed-service Verified yapılmadı.

Ücretli AWS/Azure/GCP/HCP/SaaS/trial şartı yoktur; cloud hesap/kaynakları otomatik oluşturulmaz. Yerel lab gerçek production SLA, coğrafi HA veya mesleki unvan kanıtı değildir.
