# Software Architect — Konu türü, kaynak ve ürün erişimi

Bu belge learning scope ile actual capability/product/certification farkını korur. Emlak planı değişmez; ücretli cloud/SaaS/trial/license/course zorunluluğu yoktur. [Matris](software-architect-coverage.md) bütün alt konuları owner/status ile izler.

| Konu | Gerçek eğitim çıktısı | Tamamlanmış sayılmayan scope |
|---|---|---|
| Programming Languages | Java + seçilmiş Kotlin, Python/Go, JS/TS gerçek programları; modern .NET optional | Ruby/Scala/Swift ve klasik Windows .NET Framework runtime sadece seçilmiş başka dil var diye implemented değildir |
| BABOK/TOGAF/IAF | Public resmi kaynak kapsamıyla tailored proje case artifact/review/revision | Tüm proprietary standard, formal uyumluluk ve certified practitioner |
| PMI/ITIL/PRINCE2/RUP/LeSS/SAFe/Scrum/Kanban/XP | Delivery/incident case, gerçek küçük release evidence'ı, gerekçeli comparison | Eğitim rol kartları gerçek multi-team enterprise yönetimi değildir |
| ESB/SOAP/BPM/BPEL | Camel route/SOAP integration; Flowable OSS BPMN runtime; BPEL model/validation | BPMN çalışması BPEL engine execution değildir; uygun engine yoksa BPEL runtime açık gap |
| Enterprise Software | ERPNext/Paperless gibi ücretsiz actual reference API integration + error/reconciliation | MS Dynamics/SAP ERP-HANA-Business Objects/EMC DMS/IBM BPM/Salesforce exact vendor implementation |
| Slack/Trello/Atlassian | Responsibility/access/privacy comparison; erişim+yetki varsa actual ayrı test scope | Mock/local alternatif exact SaaS kullanımı değildir; dış kişilere otomatik iletişim yok |
| Hadoop/actors | Local MapReduce/Pekko; varsa HDFS pseudo-distributed evidence | Local model distributed production HA/scale/exactly-once kanıtı değil |
| Cloud Providers/Web Mobile | Önceki local cloud-pattern lab ve actual web/mobile-client design case | Gerçek AWS/Azure/GCP provider veya native mobile/Desktop implementation yeniden aktive edilmez |

## Kaynak erişimi

Public overview ile tam telifli standard/book erişimi aynı değildir. Gerekli kaynak yoksa erişim/görev owner'ı açık kalır; ücretli lisans/kitap/sınav veya kullanıcı adına agreement kabulü otomatik yapılmaz. İzin verilmeyen uzun standard/vendor metinleri repo'ya kopyalanmaz. Uygulama günü source/version/licence ve ücretsiz edition/resource şartları doğrulanır.

## Evidence standardı

- **Technical runtime:** implementation/config + actual success/failure/recovery; failure fixture ve source/version kayıtlı.
- **Case Applied:** proje ihtiyacı + artifact + scenario/rubric review + feedback/revision + ilgili teknik decision/test trace.
- **Comparison/Design Only:** model/konsept/alternatif değerlendirmesi; implementation değildir.
- **Partial/Access Gap:** hangi capability veya kaynak/vendor runtime'ın eksik olduğu ve owner/çözüm koşulu açıktır.

Şu an bütün yeni technical/case görevleri Planlandı. Day 117 raporu runtime Verified ve Case Applied ile Comparison/gap sayılarını ayrı verir; konu main-level coverage ile listedeki her alternatif dil/vendor ürünü literal kurmak aynı değildir.
