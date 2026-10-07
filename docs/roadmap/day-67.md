# Day 67 — Terminal, Bash, process ve performans inceleme

Durum: **Planlandı**. Bu gün eğitim milestone'ıdır; tek takvim günü sınırı yoktur. Plan belgesi çalışan ürün/evidence değildir.

## Önkoşul ve kapsam

[Day 66](day-66.md) kapanır; birikimli implementation snapshot'ından `day/67` türetilir. Emlak repo/85 günlük planında değişiklik yapılmaz. [DevOps ortak kararları](../DEVOPS-ROADMAP-EXTENSION.md), [kapsam matrisi](../coverage/devops-coverage.md) ve [uygulama sözleşmesi](../coverage/mandatory-implementation-contract.md) geçerlidir.

## Öğrenme ve uygulama görevleri

Roadmap etiketleri: `Terminal Knowledge`, `Process Monitoring`, `Performance Monitoring`, `Networking Tools`, `Text Manipulation`, `Bash`, `Vim / Nano /  Emacs`, `Version Control Systems`, `Git`, `VCS Hosting`, `GitHub`.

1. ps/top, pid/signal, /proc ve process tree; free/vmstat/iostat/disk usage ile bounded worker'ın CPU/RAM/IO davranışını gözle. Platformda bulunmayan komut için eşdeğer aracı kaydet.
2. ss/ip/curl/dig/traceroute/tcpdump araçlarıyla local request'in çözümleme/connection/timeout yolunu incele. Packet capture yalnız lab trafiğinde ve secretsız fixture ile yapılır.
3. rg/awk/sed/sort/uniq/jq ile büyük olmayan log/evidence fixture'ını filtrele ve özetle. Quoting, pipefail, exit codes, signal trap, temp file cleanup ve tekrar çalıştırma güvenliği olan Bash script'i yaz.
4. Vim/Nano/Emacs başlığında Nano veya Vim seç; terminalden dosya değiştir, diff incele, hatalı ayarı düzelt ve geri al. Üç editörü birden kurmak gerekmez.
5. Day 07 Git/GitHub işlerini kullan: conflict çözümü, revert, tag, PR review ve history'den kaynak/evidence izleme tatbikatı yap. Lab çıktısı ve sensitive dosyalar için ignore/redaction uygula.
6. Yeşil Power Shell için Windows/PowerShell erişimi varsa aynı probe JSON raporunu doğrulayan küçük pwsh script'ini gerçek success/failure input ile çalıştır; Bash script'inin başka shell'de aynen çalışacağını varsayma. Erişim yoksa alternatif Comparison olarak kalır.

## Planlanan dosyalar

- `tools/ops/bash/`
- `docs/evidence/day-67/terminal-lab.md`
- `docs/evidence/day-67/` — exact komut, sürüm/edition, donanım, fixture, expected/actual sonuç ve recovery.

Bu yollar aday implementation dosyalarıdır; dosyanın varlığı Integration/Verified anlamına gelmez.

## Commit sırası

1. `docs(day-67): gereksinim sahiplik ve local kapsamı tanımla`
2. `feat(day-67): temsilî operasyon lab ve adapterlarını uygula`
3. `test(day-67): başarı hata ve toparlanmayı doğrula`
4. `docs(day-67): evidence runbook ve karşılaştırmayı kapat`

Var olan verified uygulama yeterliyse tekrar ürün veya boş feat commit oluşturulmaz; mevcut SHA/evidence ve gereken yeni testler bağlanır. Engellenen SaaS/provider için karşılaştırma commit'i literal runtime uygulaması gibi adlandırılmaz.

## Doğrulama ve kapanış

- [ ] Bash hata/interrupt durumunda doğru exit code ve cleanup üretir.
- [ ] Process/network/IO bulguları gerçek output ile açıklanır; Git conflict/revert sonrası repo ve config beklenen duruma döner.
- [ ] Required başlıklara owner/öğrenme/implementation/test evidence bağlandı; engeller explicit gap veya kapsam istisnası olarak kaldı.
- [ ] Yeni/değişen kod için uygun build/contract/integration check başarılı; ardından local runtime çalıştırıldı.
- [ ] Compatibility, sürüm, ücretsiz edition/lisans ve resource bütçesi gün başında kontrol edilip pin edildi.
- [ ] İzole namespace/VM/profile sahipliği, stop condition, cleanup ve recovery kaydedildi.
- [ ] Secret/key/token/PII Git'e girmedi; untrusted CI publishing/deploy yetkisine erişmedi.
- [ ] Matris gerçek duruma güncellendi; plan veya local emulator sonucu managed-service Verified yapılmadı.

Ücretli AWS/Azure/GCP/HCP/SaaS/trial şartı yoktur; cloud hesap/kaynakları otomatik oluşturulmaz. Yerel lab gerçek production SLA, coğrafi HA veya mesleki unvan kanıtı değildir.
