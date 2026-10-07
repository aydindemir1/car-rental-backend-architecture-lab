# Araç Kiralama — DevOps genişletme programı

**Planlandı.** Emlak Day 46–85 onaylı DevOps programı ve araç mevcut programı karşılaştırılarak, roadmap.sh/devops eksikleri **Day 65–78** kapsamına eklendi. Program 78 milestone'dır; milestone tek takvim günü demek değildir. Emlak repo değişmez. [Günlük planlar](roadmap/README.md), [coverage](coverage/devops-coverage.md), [erişim sınırları](coverage/devops-cloud-exceptions.md).

## Hedef

Java/Spring Boot/Spring Cloud sistemini build, test, yayınlama, deploy, işletme ve recovery süreçleriyle öğrenmek. Farklı yaklaşım/pattern/teknolojilerin karar gerekçesi, veri/kaynak sahipliği ve failure davranışı gerçek deneyle gösterilir. Senior/staff/principal/architect bilgi ve beceri hedefi mesleki unvan veya üretim tecrübesi garantisi değildir.

## Korunan seçimler ve yeni eğitim rolleri

| Responsibility | Önceki seçim / temel | Yeni eğitim görevi ve sınır |
|---|---|---|
| Backend | Java/Spring Boot/Spring Cloud | Python/Go yalnız ops CLI; Node backend yok |
| OS | Emlak Linux Day 46 | Ubuntu/Debian ana ortam; RHEL türevi ve FreeBSD ayrı local VM |
| Proxy/network | Traefik emlak, Nginx araç, HAProxy System Design L4 | Squid forward proxy; firewall/SSH/TLS local deney |
| Container/cluster | Docker/Minikube/Kubernetes; tek CNI/controller | Mevcut Day 31–32 ve emlak 47–62 evidence; gap Day 77 |
| IaC | Terraform Community CLI + Ansible | Aynı kaynakların ikinci owner'ı yok; VM/ayrılmış lab kaynakları |
| CI | Jenkins emlak; GitHub Actions araç | GitLab CE+Runner izole alternatif lab; CircleCI actual erişim gap'i açık |
| Java artifact / OCI | Nexus / Harbor emlak | Artifactory OSS ayrı temporary reference profile; primary registry değişmez |
| Secret | Vault | ESO sadece ayrı lab secret reconciliation; SOPS ayrı encrypted bootstrap file |
| Metrics/tracing | OTel/Prometheus/Grafana/Loki/Tempo | Elastic local log profile; Jaeger alternatif trace profile; Datadog SaaS gap'i |
| GitOps | Argo CD emlak; Flux araç | Aynı resource iki reconcile controller'a verilmez |
| Mesh | Istio emlak; Linkerd araç | Consul+Envoy ayrı temsilî profile; discovery tek başına mesh değildir |
| Serverless | Knative Java | SAM Java ve Workers local lab; managed provider uygulaması sayılmaz |
| Recovery/security | Native datastore restore, Trivy/SBOM/Cosign vb. | Mevcut pipeline/failure tatbikatında evidence; eksik görev Day 77 |
| Cloud pattern | Araç Day 49–63 | Availability/data/design/management görevleri yeniden kullanılır |

Mor ürün-spesifik satırlar için gerekli farklı ürün deneyleri ayrı lab profillerindedir. İki projenin canonical kararları değiştirilmez; aynı runtime'a competing controller/CI publisher kurulmaz. Yeşil ürün sayısını artırmak tek başına hedef değildir; requirement ve farklı öğrenme çıktısı gerekir. Terraform yerine OpenTofu'ya geçilmez.

## Fazlar

| Day | Çıktı |
|---|---|
| [65](roadmap/day-65.md) | Python ve Go ile operasyon araçları |
| [66](roadmap/day-66.md) | Ubuntu, RHEL türevi ve FreeBSD işletim lab'ı |
| [67](roadmap/day-67.md) | Terminal, Bash, process ve performans inceleme |
| [68](roadmap/day-68.md) | Networking, firewall, forward proxy ve TLS |
| [69](roadmap/day-69.md) | CI platformları: GitLab CI ve CircleCI kapsam sınırı |
| [70](roadmap/day-70.md) | Terraform, Ansible ve kaynak sahipliği |
| [71](roadmap/day-71.md) | Artifactory ve artifact lifecycle |
| [72](roadmap/day-72.md) | Vault, ESO ve SOPS ile secret lifecycle |
| [73](roadmap/day-73.md) | Elastic, Loki ve observability ürünleri |
| [74](roadmap/day-74.md) | Consul service mesh ve GitOps sınırları |
| [75](roadmap/day-75.md) | Serverless: Knative ve yerel provider runtime'ları |
| [76](roadmap/day-76.md) | Cloud sağlayıcıları: kavramlar ve kapsam istisnası |
| [77](roadmap/day-77.md) | Container, supply chain ve recovery uçtan uca |
| [78](roadmap/day-78.md) | Dört roadmap ve iki proje final audit |

## Ownership ve kaynak bütçesi

- Ağır VM/GitLab/Elastic/Artifactory/mesh profilleri sırayla açılır; aynı anda bütün stack şart değildir.
- Başlangıçta CPU/RAM/disk/virtualization ölçülür; desteklenmeyen VM/runtime engeli açık gap'tir.
- Terraform yalnız ayrılmış provisioning kaynakları; Ansible host config; Compose kendi lab servisleri; GitOps kendi Kubernetes resource'ları için owner'dır.
- Nexus canonical Java artifact, Harbor image sahibi kalır. Artifactory fixture ayrı artifact namespace/lifecycle'a sahiptir.
- Vault runtime credential, ESO seçilmiş namespace Kubernetes Secret reconciliation, SOPS ayrı Git bootstrap encryption görevi taşır.
- Kubernetes secret tüketicisi aynı credential için Spring Cloud Vault/Injector/ESO'dan bir tek fetch/reconcile yolu kullanır.
- Local namespace veya VM iki coğrafi/fiziksel bağımsız fault domain değildir; üretim HA/SLA iddiası yoktur.

## Günlük standart ve final gate

Her gün scope→ADR/ownership→küçük implementation commit→anlamlı başarı/hata/recovery testi→CI/build→local runtime→evidence/runbook sırasıyla kapanır. Sürüm/edition/license uyumluluğu gün başında doğrulanır ve pin edilir; secret/key/PII Git'e girmez.

Day 64 önceki üç roadmap checkpoint olarak korunur. Day 78 Backend/Full Stack/System Design/DevOps final audit'tir. Envanterin 74 zorunlu occurrence'ı için owner ve görev vardır; provider/SaaS actual kullanım engelleri [istisna belgesinde](coverage/devops-cloud-exceptions.md) ayrı status'ta görünür. Tüm mor ürünler runtime'da doğrulandı iddiası erişim/gap varken yapılmaz.
