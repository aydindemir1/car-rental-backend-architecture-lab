# Day 68 — Networking, firewall, forward proxy ve TLS

Durum: **Planlandı**. Bu gün eğitim milestone'ıdır; tek takvim günü sınırı yoktur. Plan belgesi çalışan ürün/evidence değildir.

## Önkoşul ve kapsam

[Day 67](day-67.md) kapanır; birikimli implementation snapshot'ından `day/68` türetilir. Emlak repo/85 günlük planında değişiklik yapılmaz. [DevOps ortak kararları](../DEVOPS-ROADMAP-EXTENSION.md), [kapsam matrisi](../coverage/devops-coverage.md) ve [uygulama sözleşmesi](../coverage/mandatory-implementation-contract.md) geçerlidir.

## Öğrenme ve uygulama görevleri

Roadmap etiketleri: `Networking & Protocols`, `DNS`, `HTTP`, `HTTPS`, `SSL / TLS`, `SSH`, `What is and how to setup X ?`, `Forward Proxy`, `Firewall`, `Nginx`, `Caching Server`, `Load Balancer`, `Reverse Proxy`, `Network Engineer`.

1. Day 52 DNS, Day 14 HTTPS/Nginx ve Day 53 L4/L7 load balancing evidence'ını kullan; DNS/TCP/TLS/HTTP katmanlarını packet/trace üzerinden ayrı göster. Mavi Network Engineer için subnet, routing, MTU ve connection hata teşhisi uygula; tüm linked roadmap otomatik kapsam değildir.
2. İzole VM/network namespace'de nftables/firewall kur; allow/deny, established connection ve yanlış rule sonrası recovery'yi uygula. Kendi yönetim bağlantısını koparmamak için local console ve geri dönüş planı kullan.
3. Squid ile local forward proxy kur; client egress allowlist, CONNECT, access log ve forbidden destination testlerini yap. Reverse proxy ile yön/kimlik/sorumluluk farkını gerçekten gözle; TLS interception zorunlu değildir.
4. SSH key authentication, host-key verification, minimum user yetkisi ve SFTP transferini local VM'de uygula; yanlış host key ve yetkisiz kullanıcı negatif testlerini çalıştır.
5. Cache server/edge/LB için Day 52–54 görevlerinin cold/hot, backend outage ve private response testlerini bağla. Yeni kalıcı edge sahibi kurulmaz.
6. Gri OSI/SMTP/IMAP/POP3S/SPF/DMARC/Domain Keys ve white/grey listing için katman/akış tablosu hazırla; isteğe bağlı local fake mail fixture kullan. Public mail/domain/ücretli hizmet şartı yoktur; bu comparison gerçek mail delivery doğrulaması sayılmaz.

## Planlanan dosyalar

- `infra/labs/networking/`
- `infra/labs/forward-proxy/`
- `docs/runbooks/network-and-tls-troubleshooting.md`
- `docs/evidence/day-68/` — exact komut, sürüm/edition, donanım, fixture, expected/actual sonuç ve recovery.

Bu yollar aday implementation dosyalarıdır; dosyanın varlığı Integration/Verified anlamına gelmez.

## Commit sırası

1. `docs(day-68): gereksinim sahiplik ve local kapsamı tanımla`
2. `feat(day-68): temsilî operasyon lab ve adapterlarını uygula`
3. `test(day-68): başarı hata ve toparlanmayı doğrula`
4. `docs(day-68): evidence runbook ve karşılaştırmayı kapat`

Var olan verified uygulama yeterliyse tekrar ürün veya boş feat commit oluşturulmaz; mevcut SHA/evidence ve gereken yeni testler bağlanır. Engellenen SaaS/provider için karşılaştırma commit'i literal runtime uygulaması gibi adlandırılmaz.

## Doğrulama ve kapanış

- [ ] Firewall ve forward proxy allowed/denied local trafik için beklenen sonucu üretir; reset sonrası bağlantı toparlanır.
- [ ] TLS wrong CA/hostname ve SSH wrong host key reddedilir; DNS/LB/cache evidence mevcut günlük uygulamaya bağlıdır.
- [ ] Required başlıklara owner/öğrenme/implementation/test evidence bağlandı; engeller explicit gap veya kapsam istisnası olarak kaldı.
- [ ] Yeni/değişen kod için uygun build/contract/integration check başarılı; ardından local runtime çalıştırıldı.
- [ ] Compatibility, sürüm, ücretsiz edition/lisans ve resource bütçesi gün başında kontrol edilip pin edildi.
- [ ] İzole namespace/VM/profile sahipliği, stop condition, cleanup ve recovery kaydedildi.
- [ ] Secret/key/token/PII Git'e girmedi; untrusted CI publishing/deploy yetkisine erişmedi.
- [ ] Matris gerçek duruma güncellendi; plan veya local emulator sonucu managed-service Verified yapılmadı.

Ücretli AWS/Azure/GCP/HCP/SaaS/trial şartı yoktur; cloud hesap/kaynakları otomatik oluşturulmaz. Yerel lab gerçek production SLA, coğrafi HA veya mesleki unvan kanıtı değildir.
