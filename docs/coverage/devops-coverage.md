# DevOps — İki proje kapsam matrisi

Kaynak: [roadmap.sh/devops](https://roadmap.sh/devops), canlı graph **2026-10-07**. [Snapshot](devops-roadmap-snapshot.json), [ortak plan](../DEVOPS-ROADMAP-EXTENSION.md), [günlük görevler](../roadmap/README.md).

## Envanter ve kapsam

| Sınıf | Düğüm sayısı | Uygulama yükümlülüğü |
|---|---:|---|
| Sarı / topic ana başlık | 22 | Explicit owner/görev; Cloud Providers local/no-cloud istisnası açık |
| Mor tikli alt başlık | 46 | Ürün-spesifik öğrenme/uygulama/test; erişim/provider istisnaları ayrı |
| Mavi konu occurrence'ı | 6 | Backend, Docker, Kubernetes, Linux, Network Engineer (iki düğüm) |
| Yeşil alternatif | 58 | Seçilmiş ürünler uygulama; diğerleri requirement karşılaştırması |
| Gri alt başlık | 9 | Legend: sıra katı değil, istediğin zaman öğren; bu renk 'gereksiz' demek değil |
| Tiksiz alt başlık | 4 | Cloud Design Patterns alt konuları; gerçek günlük deneylere bağlı |
| **Toplam eğitim düğümü** | **145** | **74 zorunlu occurrence + 71 alternatif/gri/tiksiz** |

`Visit the Beginner Version` ve gri `roadmap.sh` navigasyonu eğitim konusu değildir. Renkler graph legend metadata'sından alınmıştır; System Design snapshot'ının aksine bu roadmap mor/yeşil legend taşır. Tekrar etiketler node ID bazında korunur.

**Durum Planlandı'dır.** Kapsam matrisi uygulama kanıtı değildir. Ücretsiz local/self-hosted kararımızla bazı mor ürünlerin gerçek managed kullanımını tamamlayamayız; [istisna ve gap belgesi](devops-cloud-exceptions.md) bu farkı açık tutar. Dolayısıyla “bütün mor ürünler literal kullanıldı/kullanılacak, hiçbir engel yok” iddiası yapılmaz.

Emlak 85 gün **değişmez**. Baseline okuma branch'i `docs/backend-roadmap-design`, HEAD `a84beefb0d8d932a01056fbd4542910856129a28`. [Onaylı DevOps ortak kararları](https://github.com/aydindemir1/real-estate-backend-architecture-lab/blob/docs/backend-roadmap-design/docs/DEVOPS-ENGINEERING-PLAN.md) ve ROADMAP.md Day 46–85 kaynak olarak okunmuştur. Araç Day 01–63 kapsamı korunur; Day 64 önceki üç roadmap checkpoint; Day 65–77 ek deneyler; Day 78 dört roadmap final audit.

## 22 ana başlığın sahibi

| Başlık | Mevcut temel | Araç öğrenme/uygulama/test görevi | Durum |
|---|---|---|---|
| Learn a Programming Language | Yeni açık görev / comparison sınırı | [Day 65](../roadmap/day-65.md) | Planlandı / runtime evidence yok |
| Operating System | Yeni açık görev / comparison sınırı | [Day 66](../roadmap/day-66.md) | Planlandı / runtime evidence yok |
| Terminal Knowledge | Yeni açık görev / comparison sınırı | [Day 67](../roadmap/day-67.md) | Planlandı / runtime evidence yok |
| Version Control Systems | İki repo; araç Day 07/34 | [Day 67](../roadmap/day-67.md) | Planlandı / runtime evidence yok |
| VCS Hosting | İki repo; araç Day 07/34 | [Day 67](../roadmap/day-67.md) | Planlandı / runtime evidence yok |
| What is and how to setup X ? | Yeni açık görev / comparison sınırı | [Day 68](../roadmap/day-68.md) | Planlandı / runtime evidence yok |
| Containers | Emlak Day 47–50; araç Day 31 | [Day 77](../roadmap/day-77.md) | Planlandı / runtime evidence yok |
| Cloud Providers | Yeni açık görev / comparison sınırı | [Day 76](../roadmap/day-76.md) | Açık istisna: gerçek provider runtime yok |
| Networking & Protocols | Yeni açık görev / comparison sınırı | [Day 68](../roadmap/day-68.md) | Planlandı / runtime evidence yok |
| Serverless | Yeni açık görev / comparison sınırı | [Day 75](../roadmap/day-75.md) | Planlandı / runtime evidence yok |
| Provisioning | Emlak Day 64–65; araç Day 70 gap görevi | [Day 70](../roadmap/day-70.md) | Planlandı / runtime evidence yok |
| Configuration Management | Emlak Day 63; araç VM Day 70 | [Day 70](../roadmap/day-70.md) | Planlandı / runtime evidence yok |
| CI / CD Tools | Yeni açık görev / comparison sınırı | [Day 69](../roadmap/day-69.md) | Planlandı / runtime evidence yok |
| Secret Management | Yeni açık görev / comparison sınırı | [Day 72](../roadmap/day-72.md) | Planlandı / runtime evidence yok |
| Infrastructure Monitoring | Yeni açık görev / comparison sınırı | [Day 73](../roadmap/day-73.md) | Planlandı / runtime evidence yok |
| Logs Management | Yeni açık görev / comparison sınırı | [Day 73](../roadmap/day-73.md) | Planlandı / runtime evidence yok |
| Container Orchestration | Emlak Day 51–62; araç Day 32 | [Day 77](../roadmap/day-77.md) | Planlandı / runtime evidence yok |
| Artifact Management | Yeni açık görev / comparison sınırı | [Day 71](../roadmap/day-71.md) | Planlandı / runtime evidence yok |
| GitOps | Yeni açık görev / comparison sınırı | [Day 74](../roadmap/day-74.md) | Planlandı / runtime evidence yok |
| Service Mesh | Yeni açık görev / comparison sınırı | [Day 74](../roadmap/day-74.md) | Planlandı / runtime evidence yok |
| Cloud Design Patterns | Araç Day 51/57/59/61/62 | [Day 77](../roadmap/day-77.md) | Planlandı / runtime evidence yok |
| Observability | Yeni açık görev / comparison sınırı | [Day 73](../roadmap/day-73.md) | Planlandı / runtime evidence yok |

## Yeni günlük plan ve kapanış

| Day | Konu | Runtime doğrulaması |
|---|---|---|
| [65](../roadmap/day-65.md) | Python ve Go ile operasyon araçları | Python malformed/eksik input için hatalı exit code, geçerli fixture için deterministik rapor üretir. Go timeout/cancel sırasında goroutine/connection sızıntısı üretmez; concurrency limiti gerçek ölçümle doğrulanır. |
| [66](../roadmap/day-66.md) | Ubuntu, RHEL türevi ve FreeBSD işletim lab'ı | Üç OS ailesinde servis lifecycle ve yetkisiz dosya/port erişimi gerçek runtime'da gözlenir. Reboot sonrası beklenen servis/log durumu ve VM restore kanıtlıdır; VM kurulamazsa açık OS gap'i kalır. |
| [67](../roadmap/day-67.md) | Terminal, Bash, process ve performans inceleme | Bash hata/interrupt durumunda doğru exit code ve cleanup üretir. Process/network/IO bulguları gerçek output ile açıklanır; Git conflict/revert sonrası repo ve config beklenen duruma döner. |
| [68](../roadmap/day-68.md) | Networking, firewall, forward proxy ve TLS | Firewall ve forward proxy allowed/denied local trafik için beklenen sonucu üretir; reset sonrası bağlantı toparlanır. TLS wrong CA/hostname ve SSH wrong host key reddedilir; DNS/LB/cache evidence mevcut günlük uygulamaya bağlıdır. |
| [69](../roadmap/day-69.md) | CI platformları: GitLab CI ve CircleCI kapsam sınırı | Local GitLab Runner job'u gerçek artifact üretir; failure pipeline'ı kırar; untrusted job publish secret'a erişmez. CircleCI full implementation ancak gerçek pipeline evidence'ıyla doğrulanır; erişim yoksa açık gap status'u audit'te korunur. |
| [70](../roadmap/day-70.md) | Terraform, Ansible ve kaynak sahipliği | Aynı playbook ikinci run'da beklenmeyen değişiklik yapmaz; Terraform ayrılmış kaynakları plan/apply/destroy eder. Drift ve partial failure sonrası kontrollü reconcile doğrulanır; başka controller'ın kaynağı silinmez. |
| [71](../roadmap/day-71.md) | Artifactory ve artifact lifecycle | Artifactory publish→clean consumer resolve gerçek JAR ve checksum ile doğrulanır; yetkisiz publish reddedilir. Repository failure/recovery ve retention sınırı gözlenir; uygun ücretsiz ürün yoksa literal Artifactory Verified olmaz. |
| [72](../roadmap/day-72.md) | Vault, ESO ve SOPS ile secret lifecycle | Yanlış identity secret okuyamaz; rotation uygulamaya doğru yansır; Vault outage policy'ye uygun fail-fast/degrade üretir. ESO reconcile/rotate ve SOPS yanlış key/tamper deneyleri kanıtlıdır; plaintext/key Git'e girmez. |
| [73](../roadmap/day-73.md) | Elastic, Loki ve observability ürünleri | Elastic ingestion/search ve Loki query gerçek fixture ile çalışır; malformed/redacted log ve outage sonrası davranış kaydedilir. Trace correlation ve Prometheus/Grafana alert firing/resolution kanıtlıdır; Datadog SaaS evidence olmadan ürün Verified değildir. |
| [74](../roadmap/day-74.md) | Consul service mesh ve GitOps sınırları | Consul workload trafiği identity/mTLS/intentions üzerinden izin/verme testiyle doğrulanır; plain discovery yeterli değildir. GitOps drift/recovery ve baseline mesh identity testleri kanıtlıdır; competing controller yoktur. |
| [75](../roadmap/day-75.md) | Serverless: Knative ve yerel provider runtime'ları | Java Knative scale-to-zero/restart ve function failure gözlenir; local Java SAM input/error testi çalışır. Workers local request/validation ve cleanup doğrulanır; iki provider satırı managed-cloud Verified diye kapanmaz. |
| [76](../roadmap/day-76.md) | Cloud sağlayıcıları: kavramlar ve kapsam istisnası | Local network/identity/restore sözleşmeleri gerçek test evidence'ına bağlıdır; provider tasarımının uygulanmadığı açıkça yazılır. Cloud Providers/AWS/Azure/GCP status'ları full coverage hesabında istisna olarak görünür; ücretli kaynak oluşturulmaz. |
| [77](../roadmap/day-77.md) | Container, supply chain ve recovery uçtan uca | Release zinciri digest/commit ile izlenebilir; failed gate deploy'u durdurur; uygulama E2E başarılıdır. Restore sonrası canonical booking ve projection invariant'ları doğrulanır; resource budget ve fiziksel HA sınırı raporlanır. |
| [78](../roadmap/day-78.md) | Dört roadmap ve iki proje final audit | Dört matrisin bütün required satırları Verified, açık gap veya açık istisna olarak evidence/reason sahibine bağlıdır. Literal 'roadmap'teki her mor ürün uygulandı' iddiası cloud/SaaS gap'leri varken yapılmaz; iki projenin final raporu tekrar üretilebilir. |

## Düğüm bazında tam coverage

Day bağlantılarında somut görevler, başarı/hata/toparlanma kriterleri ve commit sırası bulunur. Emlak planına link vermek Verified değildir: runtime evidence yoksa araç owner'ındaki gap görevi uygulanır. Ortak responsibility için aynı verified evidence birden fazla occurrence'ı karşılayabilir.

| Node ID | Renk / sınıf | Roadmap etiketi | Mevcut temel | Owner / görev | Plan status / sınır |
|---|---|---|---|---|---|
| `v5FGKQc-_7NYEsWjmTEuq` | Sarı / ana konu | Learn a Programming Language | Yeni açık görev / comparison sınırı | [Day 65](../roadmap/day-65.md) | Planlandı / runtime evidence yok |
| `TwVfCYMS9jSaJ6UyYmC-K` | Mor | Python | Yeni açık görev / comparison sınırı | [Day 65](../roadmap/day-65.md) | Planlandı / runtime evidence yok |
| `PuXAPYA0bsMgwcnlwJxQn` | Yeşil | Ruby | Yeni açık görev / comparison sınırı | [Day 78](../roadmap/day-78.md) | Comparison (alternatif/gri) |
| `npnMwSDEK2aLGgnuZZ4dO` | Mor | Go | Yeni açık görev / comparison sınırı | [Day 65](../roadmap/day-65.md) | Planlandı / runtime evidence yok |
| `eL62bKAoJCMsu7zPlgyhy` | Yeşil | Rust | Yeni açık görev / comparison sınırı | [Day 78](../roadmap/day-78.md) | Comparison (alternatif/gri) |
| `QCdemtWa2mE78poNXeqzr` | Yeşil | JavaScript / Node.js | Yeni açık görev / comparison sınırı | [Day 78](../roadmap/day-78.md) | Comparison (alternatif/gri) |
| `qe84v529VbCyydl0BKFk2` | Sarı / ana konu | Operating System | Yeni açık görev / comparison sınırı | [Day 66](../roadmap/day-66.md) | Planlandı / runtime evidence yok |
| `cTqVab0VbVcn3W7i0wBrX` | Mor | Ubuntu / Debian | Yeni açık görev / comparison sınırı | [Day 66](../roadmap/day-66.md) | Planlandı / runtime evidence yok |
| `zhNUK953p6tjREndk3yQZ` | Yeşil | SUSE Linux | Yeni açık görev / comparison sınırı | [Day 78](../roadmap/day-78.md) | Comparison (alternatif/gri) |
| `7mS6Y_BOAHNgM3OjyFtZ9` | Mor | RHEL / Derivatives | Yeni açık görev / comparison sınırı | [Day 66](../roadmap/day-66.md) | Planlandı / runtime evidence yok |
| `PiPHFimToormOPl1EtEe8` | Mor | FreeBSD | Yeni açık görev / comparison sınırı | [Day 66](../roadmap/day-66.md) | Planlandı / runtime evidence yok |
| `97cJYKqv7CPPUXkKNwM4x` | Yeşil | OpenBSD | Yeni açık görev / comparison sınırı | [Day 78](../roadmap/day-78.md) | Comparison (alternatif/gri) |
| `haiYSwNt3rjiiwCDszPk1` | Yeşil | NetBSD | Yeni açık görev / comparison sınırı | [Day 78](../roadmap/day-78.md) | Comparison (alternatif/gri) |
| `UOQimp7QkM3sxmFvk5d3i` | Yeşil | Windows | Yeni açık görev / comparison sınırı | [Day 78](../roadmap/day-78.md) | Comparison (alternatif/gri) |
| `wjJPzrFJBNYOD3SJLzW2M` | Sarı / ana konu | Terminal Knowledge | Yeni açık görev / comparison sınırı | [Day 67](../roadmap/day-67.md) | Planlandı / runtime evidence yok |
| `x-JWvG1iw86ULL9KrQmRu` | Mor | Process Monitoring | Yeni açık görev / comparison sınırı | [Day 67](../roadmap/day-67.md) | Planlandı / runtime evidence yok |
| `gIEQDgKOsoEnSv8mpEzGH` | Mor | Performance Monitoring | Yeni açık görev / comparison sınırı | [Day 67](../roadmap/day-67.md) | Planlandı / runtime evidence yok |
| `OaqKLZe-XnngcDhDzCtRt` | Mor | Networking Tools | Yeni açık görev / comparison sınırı | [Day 67](../roadmap/day-67.md) | Planlandı / runtime evidence yok |
| `cUifrP7v55psTb20IZndf` | Mor | Text Manipulation | Yeni açık görev / comparison sınırı | [Day 67](../roadmap/day-67.md) | Planlandı / runtime evidence yok |
| `syBIAL1mHbJLnTBoSxXI7` | Mor | Bash | Yeni açık görev / comparison sınırı | [Day 67](../roadmap/day-67.md) | Planlandı / runtime evidence yok |
| `z6IBekR8Xl-6f8WEb05Nw` | Yeşil | Power Shell | Yeni açık görev / comparison sınırı | [Day 67](../roadmap/day-67.md) | Planlandı: uygun platform/runtime varsa; aksi Comparison |
| `Jt8BmtLUH6fHT2pGKoJs3` | Mor | Vim / Nano /  Emacs | Yeni açık görev / comparison sınırı | [Day 67](../roadmap/day-67.md) | Planlandı / runtime evidence yok |
| `LvhFmlxz5uIy7k_nzx2Bv` | Sarı / ana konu | Version Control Systems | İki repo; araç Day 07/34 | [Day 67](../roadmap/day-67.md) | Planlandı / runtime evidence yok |
| `uyDm1SpOQdpHjq9zBAdck` | Mor | Git | İki repo; araç Day 07/34 | [Day 67](../roadmap/day-67.md) | Planlandı / runtime evidence yok |
| `h10BH3OybHcIN2iDTSGkn` | Sarı / ana konu | VCS Hosting | İki repo; araç Day 07/34 | [Day 67](../roadmap/day-67.md) | Planlandı / runtime evidence yok |
| `ot9I_IHdnq2yAMffrSrbN` | Mor | GitHub | İki repo; araç Day 07/34 | [Day 67](../roadmap/day-67.md) | Planlandı / runtime evidence yok |
| `oQIB0KE0BibjIYmxrpPZS` | Yeşil | GitLab | Yeni açık görev / comparison sınırı | [Day 69](../roadmap/day-69.md) | Planlandı / runtime evidence yok |
| `Z7SsBWgluZWr9iWb2e9XO` | Yeşil | Bitbucket | Yeni açık görev / comparison sınırı | [Day 78](../roadmap/day-78.md) | Comparison (alternatif/gri) |
| `jCWrnQNgjHKyhzd9dwOHz` | Sarı / ana konu | What is and how to setup X ? | Yeni açık görev / comparison sınırı | [Day 68](../roadmap/day-68.md) | Planlandı / runtime evidence yok |
| `F93XnRj0BLswJkzyRggLS` | Mor | Forward Proxy | Yeni açık görev / comparison sınırı | [Day 68](../roadmap/day-68.md) | Planlandı / runtime evidence yok |
| `f3tM2uo6LLSOmyeFfLc7h` | Mor | Firewall | Yeni açık görev / comparison sınırı | [Day 68](../roadmap/day-68.md) | Planlandı / runtime evidence yok |
| `ukOrSeyK1ElOt9tTjCkfO` | Mor | Nginx | Araç Day 14/52–53 | [Day 68](../roadmap/day-68.md) | Planlandı / runtime evidence yok |
| `dF3otkMMN09tgCzci8Jyv` | Yeşil | Tomcat | Yeni açık görev / comparison sınırı | [Day 77](../roadmap/day-77.md) | Planlandı: uygun platform/runtime varsa; aksi Comparison |
| `0_GMTcMeZv3A8dYkHRoW7` | Yeşil | Apache | Yeni açık görev / comparison sınırı | [Day 78](../roadmap/day-78.md) | Comparison (alternatif/gri) |
| `54UZNO2q8M5FiA_XbcU_D` | Yeşil | Caddy | Yeni açık görev / comparison sınırı | [Day 78](../roadmap/day-78.md) | Comparison (alternatif/gri) |
| `5iJOE1QxMvf8BQ_8ssiI8` | Yeşil | IIS | Yeni açık görev / comparison sınırı | [Day 78](../roadmap/day-78.md) | Comparison (alternatif/gri) |
| `R4XSY4TSjU1M7cW66zUqJ` | Mor | Caching Server | Araç Day 52–54 | [Day 68](../roadmap/day-68.md) | Planlandı / runtime evidence yok |
| `i8Sd9maB_BeFurULrHXNq` | Mor | Load Balancer | Araç Day 52–54 | [Day 68](../roadmap/day-68.md) | Planlandı / runtime evidence yok |
| `eGF7iyigl57myx2ejpmNC` | Mor | Reverse Proxy | Araç Day 14/52–53 | [Day 68](../roadmap/day-68.md) | Planlandı / runtime evidence yok |
| `CQhUflAcv1lhBnmDY0gaz` | Sarı / ana konu | Containers | Emlak Day 47–50; araç Day 31 | [Day 77](../roadmap/day-77.md) | Planlandı / runtime evidence yok |
| `P0acFNZ413MSKElHqCxr3` | Mor | Docker | Emlak Day 47–50; araç Day 31 | [Day 77](../roadmap/day-77.md) | Planlandı / runtime evidence yok |
| `qYRJYIZsmf-inMqKECRkI` | Yeşil | LXC | Yeni açık görev / comparison sınırı | [Day 78](../roadmap/day-78.md) | Comparison (alternatif/gri) |
| `2Wd9SlWGg6QtxgiUVLyZL` | Sarı / ana konu | Cloud Providers | Yeni açık görev / comparison sınırı | [Day 76](../roadmap/day-76.md) | Açık istisna: gerçek provider runtime yok |
| `1ieK6B_oqW8qOC6bdmiJe` | Mor | AWS | Yeni açık görev / comparison sınırı | [Day 76](../roadmap/day-76.md) | Açık istisna: gerçek provider runtime yok |
| `ctor79Vd7EXDMdrLyUcu_` | Mor | Azure | Yeni açık görev / comparison sınırı | [Day 76](../roadmap/day-76.md) | Açık istisna: gerçek provider runtime yok |
| `zYrOxFQkl3KSe67fh3smD` | Mor | Google Cloud | Yeni açık görev / comparison sınırı | [Day 76](../roadmap/day-76.md) | Açık istisna: gerçek provider runtime yok |
| `-h-kNVDNzZYnQAR_4lfXc` | Yeşil | Digital Ocean | Yeni açık görev / comparison sınırı | [Day 78](../roadmap/day-78.md) | Comparison (alternatif/gri) |
| `YUJf-6ccHvYjL_RzufQ-G` | Yeşil | Alibaba Cloud | Yeni açık görev / comparison sınırı | [Day 78](../roadmap/day-78.md) | Comparison (alternatif/gri) |
| `I327qPYGMcdayRR5WT0Ek` | Yeşil | Hetzner | Yeni açık görev / comparison sınırı | [Day 78](../roadmap/day-78.md) | Comparison (alternatif/gri) |
| `FaPf567JGRAg1MBlFj9Tk` | Yeşil | Heroku | Yeni açık görev / comparison sınırı | [Day 78](../roadmap/day-78.md) | Comparison (alternatif/gri) |
| `RDLmML_HS2c8J4D_U_KYe` | Gri (sıra bağımsız) | FTP / SFTP | Yeni açık görev / comparison sınırı | [Day 68](../roadmap/day-68.md) | Planlandı / runtime evidence yok |
| `Vu955vdsYerCG8G6suqml` | Mor | DNS | Araç Day 52–54 | [Day 68](../roadmap/day-68.md) | Planlandı / runtime evidence yok |
| `ke-8MeuLx7AS2XjSsPhxe` | Mor | HTTP | Yeni açık görev / comparison sınırı | [Day 68](../roadmap/day-68.md) | Planlandı / runtime evidence yok |
| `AJO3jtHvIICj8YKaSXl0U` | Mor | HTTPS | Araç Day 14/52–53 | [Day 68](../roadmap/day-68.md) | Planlandı / runtime evidence yok |
| `0o6ejhfpmO4S8A6djVWva` | Mor | SSL / TLS | Araç Day 14/52–53 | [Day 68](../roadmap/day-68.md) | Planlandı / runtime evidence yok |
| `wcIRMLVm3SdEJWF9RPfn7` | Mor | SSH | Yeni açık görev / comparison sınırı | [Day 68](../roadmap/day-68.md) | Planlandı / runtime evidence yok |
| `E-lSLGzgOPrz-25ER2Hk7` | Gri (sıra bağımsız) | White / Grey Listing | Yeni açık görev / comparison sınırı | [Day 78](../roadmap/day-78.md) | Comparison (alternatif/gri) |
| `zJy9dOynWgLTDKI1iBluG` | Gri (sıra bağımsız) | SMTP | Yeni açık görev / comparison sınırı | [Day 78](../roadmap/day-78.md) | Comparison (alternatif/gri) |
| `5vUKHuItQfkarp7LtACvX` | Gri (sıra bağımsız) | DMARC | Yeni açık görev / comparison sınırı | [Day 78](../roadmap/day-78.md) | Comparison (alternatif/gri) |
| `WMuXqa4b5wyRuYAQKQJRj` | Gri (sıra bağımsız) | IMAP | Yeni açık görev / comparison sınırı | [Day 78](../roadmap/day-78.md) | Comparison (alternatif/gri) |
| `ewcJfnDFKXN8I5TLpXEaB` | Gri (sıra bağımsız) | SPF | Yeni açık görev / comparison sınırı | [Day 78](../roadmap/day-78.md) | Comparison (alternatif/gri) |
| `fzO6xVTBxliu24f3W5zaU` | Gri (sıra bağımsız) | POP3S | Yeni açık görev / comparison sınırı | [Day 78](../roadmap/day-78.md) | Comparison (alternatif/gri) |
| `RYCD78msIR2BPJoIP71aj` | Gri (sıra bağımsız) | Domain Keys | Yeni açık görev / comparison sınırı | [Day 78](../roadmap/day-78.md) | Comparison (alternatif/gri) |
| `QZ7bkY-MaEgxYoPDP3nma` | Gri (sıra bağımsız) | OSI Model | Yeni açık görev / comparison sınırı | [Day 78](../roadmap/day-78.md) | Comparison (alternatif/gri) |
| `w5d24Sf8GDkLDLGUPxzS9` | Sarı / ana konu | Networking & Protocols | Yeni açık görev / comparison sınırı | [Day 68](../roadmap/day-68.md) | Planlandı / runtime evidence yok |
| `9p_ufPj6QH9gHbWBQUmGw` | Sarı / ana konu | Serverless | Yeni açık görev / comparison sınırı | [Day 75](../roadmap/day-75.md) | Planlandı / runtime evidence yok |
| `LZDRgDxEZ3klp2PrrJFBX` | Yeşil | Vercel | Yeni açık görev / comparison sınırı | [Day 78](../roadmap/day-78.md) | Comparison (alternatif/gri) |
| `l8VAewSEXzoyqYFhoplJj` | Mor | Cloudflare | Yeni açık görev / comparison sınırı | [Day 75](../roadmap/day-75.md) | Planlandı: local runtime; managed provider Partial |
| `mlrlf2McMI7IBhyEdq0Nf` | Yeşil | Azure Functions | Yeni açık görev / comparison sınırı | [Day 78](../roadmap/day-78.md) | Comparison (alternatif/gri) |
| `UfQrIJ-uMNJt9H_VM_Q5q` | Mor | AWS Lambda | Yeni açık görev / comparison sınırı | [Day 75](../roadmap/day-75.md) | Planlandı: local runtime; managed provider Partial |
| `hCKODV2b_l2uPit0YeP1M` | Yeşil | Netlify | Yeni açık görev / comparison sınırı | [Day 78](../roadmap/day-78.md) | Comparison (alternatif/gri) |
| `1oYvpFG8LKT1JD6a_9J0m` | Sarı / ana konu | Provisioning | Emlak Day 64–65; araç Day 70 gap görevi | [Day 70](../roadmap/day-70.md) | Planlandı / runtime evidence yok |
| `XA__697KgofsH28coQ-ma` | Yeşil | AWS CDK | Yeni açık görev / comparison sınırı | [Day 78](../roadmap/day-78.md) | Comparison (alternatif/gri) |
| `TgBb4aL_9UkyU36CN4qvS` | Yeşil | CloudFormation | Yeni açık görev / comparison sınırı | [Day 78](../roadmap/day-78.md) | Comparison (alternatif/gri) |
| `O0xZ3dy2zIDbOetVrgna6` | Yeşil | Pulumi | Yeni açık görev / comparison sınırı | [Day 78](../roadmap/day-78.md) | Comparison (alternatif/gri) |
| `nUBGf1rp9GK_pbagWCP9g` | Mor | Terraform | Emlak Day 64–65; araç Day 70 gap görevi | [Day 70](../roadmap/day-70.md) | Planlandı / runtime evidence yok |
| `V9sOxlNOyRp0Mghl7zudv` | Sarı / ana konu | Configuration Management | Emlak Day 63; araç VM Day 70 | [Day 70](../roadmap/day-70.md) | Planlandı / runtime evidence yok |
| `h9vVPOmdUSeEGVQQaSTH5` | Mor | Ansible | Emlak Day 63; araç VM Day 70 | [Day 70](../roadmap/day-70.md) | Planlandı / runtime evidence yok |
| `kv508kxzUj_CjZRb-TeRv` | Yeşil | Chef | Yeni açık görev / comparison sınırı | [Day 78](../roadmap/day-78.md) | Comparison (alternatif/gri) |
| `yP1y8U3eblpzbaLiCGliU` | Yeşil | Puppet | Yeni açık görev / comparison sınırı | [Day 78](../roadmap/day-78.md) | Comparison (alternatif/gri) |
| `aQJaouIaxIJChM-40M3HQ` | Sarı / ana konu | CI / CD Tools | Yeni açık görev / comparison sınırı | [Day 69](../roadmap/day-69.md) | Planlandı / runtime evidence yok |
| `JnWVCS1HbAyfCJzGt-WOH` | Mor | GitHub Actions | Araç Day 34 | [Day 69](../roadmap/day-69.md) | Planlandı / runtime evidence yok |
| `2KjSLLVTvl2G2KValw7S7` | Mor | GitLab CI | Yeni açık görev / comparison sınırı | [Day 69](../roadmap/day-69.md) | Planlandı / runtime evidence yok |
| `dUapFp3f0Rum-rf_Vk_b-` | Yeşil | Jenkins | Emlak Day 66–68 | [Day 77](../roadmap/day-77.md) | Planlandı / runtime evidence yok |
| `1-JneOQeGhox-CKrdiquq` | Mor | Circle CI | Yeni açık görev / comparison sınırı | [Day 69](../roadmap/day-69.md) | Planlandı: actual hizmet erişimi yoksa açık gap |
| `TsXFx1wWikVBVoFUUDAMx` | Yeşil | Octopus Deploy | Yeni açık görev / comparison sınırı | [Day 78](../roadmap/day-78.md) | Comparison (alternatif/gri) |
| `L000AbzF3oLcn4B1eUIYX` | Yeşil | TeamCity | Yeni açık görev / comparison sınırı | [Day 78](../roadmap/day-78.md) | Comparison (alternatif/gri) |
| `hcrPpjFxPi_iLiMdLKJrO` | Sarı / ana konu | Secret Management | Yeni açık görev / comparison sınırı | [Day 72](../roadmap/day-72.md) | Planlandı / runtime evidence yok |
| `ZWq23Q9ZNxLNti68oltxA` | Yeşil | Sealed Secrets | Yeni açık görev / comparison sınırı | [Day 78](../roadmap/day-78.md) | Comparison (alternatif/gri) |
| `yQ4d2uiROZYr950cjYnQE` | Yeşil | Cloud Specific Tools | Yeni açık görev / comparison sınırı | [Day 78](../roadmap/day-78.md) | Comparison (alternatif/gri) |
| `tZzvs80KzqT8aDvEyjack` | Mor | Vault | Emlak Day 24/54; araç Day 72 | [Day 72](../roadmap/day-72.md) | Planlandı / runtime evidence yok |
| `GHQWHLxsO40kJ6z_YCinJ` | Yeşil | SOPs | Yeni açık görev / comparison sınırı | [Day 72](../roadmap/day-72.md) | Planlandı / runtime evidence yok |
| `qqRLeTpuoW64H9LvY0U_w` | Sarı / ana konu | Infrastructure Monitoring | Yeni açık görev / comparison sınırı | [Day 73](../roadmap/day-73.md) | Planlandı / runtime evidence yok |
| `W9sKEoDlR8LzocQkqSv82` | Yeşil | Zabbix | Yeni açık görev / comparison sınırı | [Day 78](../roadmap/day-78.md) | Comparison (alternatif/gri) |
| `NiVvRbCOCDpVvif48poCo` | Mor | Prometheus | Emlak Day 29–30/81; araç Day 36/61 | [Day 73](../roadmap/day-73.md) | Planlandı / runtime evidence yok |
| `bujq_C-ejtpmk-ICALByy` | Mor | Datadog | Yeni açık görev / comparison sınırı | [Day 73](../roadmap/day-73.md) | Planlandı: actual hizmet erişimi yoksa açık gap |
| `niA_96yR7uQ0sc6S_OStf` | Mor | Grafana | Emlak Day 29–30/81; araç Day 36/61 | [Day 73](../roadmap/day-73.md) | Planlandı / runtime evidence yok |
| `gaoZjOYmU0J5aM6vtLNvN` | Sarı / ana konu | Logs Management | Yeni açık görev / comparison sınırı | [Day 73](../roadmap/day-73.md) | Planlandı / runtime evidence yok |
| `K_qLhK2kKN_uCq7iVjqph` | Mor | Elastic Stack | Yeni açık görev / comparison sınırı | [Day 73](../roadmap/day-73.md) | Planlandı / runtime evidence yok |
| `s_kss4FJ2KyZRdcKNHK2v` | Yeşil | Graylog | Yeni açık görev / comparison sınırı | [Day 78](../roadmap/day-78.md) | Comparison (alternatif/gri) |
| `dZID_Y_uRTF8JlfDCqeqs` | Yeşil | Splunk | Yeni açık görev / comparison sınırı | [Day 78](../roadmap/day-78.md) | Comparison (alternatif/gri) |
| `cjjMZdyLgakyVkImVQTza` | Yeşil | Papertrail | Yeni açık görev / comparison sınırı | [Day 78](../roadmap/day-78.md) | Comparison (alternatif/gri) |
| `Yq8kVoRf20aL_o4VZU5--` | Sarı / ana konu | Container Orchestration | Emlak Day 51–62; araç Day 32 | [Day 77](../roadmap/day-77.md) | Planlandı / runtime evidence yok |
| `XbrWlTyH4z8crSHkki2lp` | Yeşil | GKE / EKS / AKS | Yeni açık görev / comparison sınırı | [Day 78](../roadmap/day-78.md) | Comparison (alternatif/gri) |
| `FE2h-uQy6qli3rKERci1j` | Yeşil | AWS ECS / Fargate | Yeni açık görev / comparison sınırı | [Day 78](../roadmap/day-78.md) | Comparison (alternatif/gri) |
| `VD24HC9qJOC42lbpJ-swC` | Yeşil | Docker Swarm | Yeni açık görev / comparison sınırı | [Day 78](../roadmap/day-78.md) | Comparison (alternatif/gri) |
| `zuBAjrqQPjj-0DHGjCaqT` | Sarı / ana konu | Artifact Management | Yeni açık görev / comparison sınırı | [Day 71](../roadmap/day-71.md) | Planlandı / runtime evidence yok |
| `C_sFyIsIIpriZlovvcbSE` | Mor | Artifactory | Yeni açık görev / comparison sınırı | [Day 71](../roadmap/day-71.md) | Planlandı: ücretsiz güncel distribution erişimi gate |
| `ootuLJfRXarVvm3J1Ir11` | Yeşil | Nexus | Emlak Day 70 | [Day 71](../roadmap/day-71.md) | Planlandı / runtime evidence yok |
| `vsmE6EpCc2DFGk1YTbkHS` | Yeşil | Cloud Smith | Yeni açık görev / comparison sınırı | [Day 78](../roadmap/day-78.md) | Comparison (alternatif/gri) |
| `-INN1qTMLimrZgaSPCcHj` | Sarı / ana konu | GitOps | Yeni açık görev / comparison sınırı | [Day 74](../roadmap/day-74.md) | Planlandı / runtime evidence yok |
| `i-DLwNXdCUUug6lfjkPSy` | Mor | ArgoCD | Emlak Day 74–78 | [Day 74](../roadmap/day-74.md) | Planlandı / runtime evidence yok |
| `6gVV_JUgKgwJb4C8tHZn7` | Yeşil | FluxCD | Araç Day 35 | [Day 74](../roadmap/day-74.md) | Planlandı / runtime evidence yok |
| `EeWsihH9ehbFKebYoB5i9` | Sarı / ana konu | Service Mesh | Yeni açık görev / comparison sınırı | [Day 74](../roadmap/day-74.md) | Planlandı / runtime evidence yok |
| `XsSnqW6k2IzvmrMmJeU6a` | Mor | Istio | Emlak Day 79 | [Day 74](../roadmap/day-74.md) | Planlandı / runtime evidence yok |
| `OXOTm3nz6o44p50qd0brN` | Mor | Consul | Yeni açık görev / comparison sınırı | [Day 74](../roadmap/day-74.md) | Planlandı / runtime evidence yok |
| `hhoSe4q1u850PgK62Ubau` | Yeşil | Linkerd | Araç Day 36 | [Day 74](../roadmap/day-74.md) | Planlandı / runtime evidence yok |
| `epLLYArR16HlhAS4c33b4` | Yeşil | Envoy | Yeni açık görev / comparison sınırı | [Day 74](../roadmap/day-74.md) | Planlandı / runtime evidence yok |
| `Qc0MGR5bMG9eeM5Zb9PMk` | Sarı / ana konu | Cloud Design Patterns | Araç Day 51/57/59/61/62 | [Day 77](../roadmap/day-77.md) | Planlandı / runtime evidence yok |
| `JCe3fcOf-sokTJURyX1oI` | Tiksiz alt konu | Availability | Araç Day 51/57/59/61/62 | [Day 77](../roadmap/day-77.md) | Planlandı / runtime evidence yok |
| `5FN7iva4DW_lv-r1tijd8` | Tiksiz alt konu | Data Management | Araç Day 51/57/59/61/62 | [Day 77](../roadmap/day-77.md) | Planlandı / runtime evidence yok |
| `1_NRXjckZ0F8EtEmgixqz` | Tiksiz alt konu | Design and Implementation | Araç Day 51/57/59/61/62 | [Day 77](../roadmap/day-77.md) | Planlandı / runtime evidence yok |
| `8kby89epyullS9W7uKDrs` | Tiksiz alt konu | Management and Monitoring | Araç Day 51/57/59/61/62 | [Day 77](../roadmap/day-77.md) | Planlandı / runtime evidence yok |
| `wKYrZhmdNsv1Dw74-oAjR` | Mavi | Backend | Yeni açık görev / comparison sınırı | [Day 77](../roadmap/day-77.md) | Planlandı / runtime evidence yok |
| `IjRWRJtJqhSsf67kh5YE6` | Mavi | Docker | Emlak Day 47–50; araç Day 31 | [Day 77](../roadmap/day-77.md) | Planlandı / runtime evidence yok |
| `0iBhYESSf5f6WHvs_QqC5` | Mavi | Kubernetes | Emlak Day 51–62; araç Day 32 | [Day 77](../roadmap/day-77.md) | Planlandı / runtime evidence yok |
| `uSLzfLPXxS5-P7ozscvjZ` | Mavi | Linux | Yeni açık görev / comparison sınırı | [Day 66](../roadmap/day-66.md) | Planlandı / runtime evidence yok |
| `w2eCgBC-ydMHSxh7LMti8` | Mor | Loki | Emlak Day 29–30/81; araç Day 36/61 | [Day 73](../roadmap/day-73.md) | Planlandı / runtime evidence yok |
| `hIBeTUiAI3zwUY6NgAO-A` | Mor | Kubernetes | Emlak Day 51–62; araç Day 32 | [Day 77](../roadmap/day-77.md) | Planlandı / runtime evidence yok |
| `JXsctlXUUS1ie8nNEgIk9` | Yeşil | GCP Functions | Yeni açık görev / comparison sınırı | [Day 78](../roadmap/day-78.md) | Comparison (alternatif/gri) |
| `wNguM6-YEznduz3MgBCYo` | Sarı / ana konu | Observability | Yeni açık görev / comparison sınırı | [Day 73](../roadmap/day-73.md) | Planlandı / runtime evidence yok |
| `8rd7T5ahK2I_zh5co-IF-` | Yeşil | Jaeger | Yeni açık görev / comparison sınırı | [Day 73](../roadmap/day-73.md) | Planlandı / runtime evidence yok |
| `pk76Us6z8LoX3f0mhnCyR` | Yeşil | New Relic | Yeni açık görev / comparison sınırı | [Day 78](../roadmap/day-78.md) | Comparison (alternatif/gri) |
| `BHny2Emf96suhAlltiEro` | Yeşil | Datadog | Yeni açık görev / comparison sınırı | [Day 73](../roadmap/day-73.md) | Planlandı: actual hizmet erişimi yoksa açık gap |
| `eOyu4wmKOrcMlhD8pUGGh` | Yeşil | Prometheus | Emlak Day 29–30/81; araç Day 36/61 | [Day 73](../roadmap/day-73.md) | Planlandı / runtime evidence yok |
| `K81bmtgnB1gfhYdi3TB5a` | Yeşil | OpenTelemetry | Emlak Day 29–30/81; araç Day 36/61 | [Day 73](../roadmap/day-73.md) | Planlandı / runtime evidence yok |
| `lUUJAEBrGJvL8dRs2n1GD` | Yeşil | ESO | Yeni açık görev / comparison sınırı | [Day 72](../roadmap/day-72.md) | Planlandı / runtime evidence yok |
| `4aJVaimsuvGIPXMZ_WjaA` | Yeşil | Dynatrace | Yeni açık görev / comparison sınırı | [Day 78](../roadmap/day-78.md) | Comparison (alternatif/gri) |
| `Kumwd6XOlEMeDohDH0q9P` | Yeşil | Salt | Yeni açık görev / comparison sınırı | [Day 78](../roadmap/day-78.md) | Comparison (alternatif/gri) |
| `3GryoQuI67JTHg9r3xUHO` | Yeşil | OpenShift | Yeni açık görev / comparison sınırı | [Day 78](../roadmap/day-78.md) | Comparison (alternatif/gri) |
| `YeWQnKPIWti6sfYT51WT1` | Mavi | Network Engineer | Yeni açık görev / comparison sınırı | [Day 68](../roadmap/day-68.md) | Planlandı / runtime evidence yok |
| `hBrlgoiP-eRsxVf8xYmJZ` | Mavi | Network Engineer | Yeni açık görev / comparison sınırı | [Day 68](../roadmap/day-68.md) | Planlandı / runtime evidence yok |
| `DjDR8Yn5Q55NvoihElj7m` | Yeşil | Render | Yeni açık görev / comparison sınırı | [Day 78](../roadmap/day-78.md) | Comparison (alternatif/gri) |
| `e0CIteRMxc0DydKEJnMhp` | Yeşil | Railway | Yeni açık görev / comparison sınırı | [Day 78](../roadmap/day-78.md) | Comparison (alternatif/gri) |
| `1du8Q2pRZM82ri6jBy5T7` | Yeşil | Buildkite | Yeni açık görev / comparison sınırı | [Day 78](../roadmap/day-78.md) | Comparison (alternatif/gri) |

## Seçilmiş yeşil seçenekler

- Mevcut emlakta Jenkins/Nexus; araçta FluxCD/Linkerd uygulama görevleri korunur.
- GitLab, ESO, SOPS (snapshot etiketi `SOPs`), Envoy, OpenTelemetry ve Jaeger ayrı görev veya mevcut data plane üzerinden gerçek evidence'a bağlanır.
- Prometheus'un yeşil observability occurrence'ı mevcut Prometheus uygulamasıyla; mor infrastructure occurrence'ı da aynı ürünün ilgili runtime evidence'ıyla karşılanabilir.
- PowerShell uygun platformda küçük gerçek CLI görevi; Tomcat seçilmiş Spring embedded runtime üzerinde somut lifecycle deneyi. Koşul yoksa Comparison kalır.
- Diğer yeşil ürünler zorunlu ikinci ürün olarak kurulmaz. Gri network/mail konuları karşılaştırma ve isteğe bağlı local fixture ile korunur; actual provider/mail runtime diye gösterilmez.

## Final gate ve istisnalar

Day 78, Backend/Full Stack/System Design/DevOps matrislerini birlikte denetler. 74 required occurrence için implementation SHA, öğrenme notu, version/edition ve başarı/hata/recovery evidence veya açık gap/istisna sahibi bulunur. AWS/Azure/GCP gerçek provider, local Lambda/Cloudflare ve CircleCI/Datadog erişim satırları full literal implementation sayısına karıştırılmaz. Tüm ürünler uygulandı iddiası yerine verified/gap/istisna/partial sayıları ayrı raporlanır.
