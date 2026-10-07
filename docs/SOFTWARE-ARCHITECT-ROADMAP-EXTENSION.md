# Araç Kiralama — Software Architect genişletmesi

**Planlandı.** [Software Architect matrisi](coverage/software-architect-coverage.md) ve [snapshot](coverage/software-architect-roadmap-snapshot.json) explicit kullanıcı talebiyle scope'tur. Emlak 85 gün değişmez. Araç programı **117 milestone**: Day 99 önceki beş roadmap ara checkpoint; Day 100–116 mimari deneyler; Day 117 altı roadmap final audit. Günler takvim günü sınırı taşımaz.

## Hedef ve sınırlar

Farklı mimari seviyeleri, kalite kararları, principle/pattern/runtime'lar ve communication/governance becerilerini gerçek case/uygulama ile öğrenmek. Java/Spring Boot/Spring Cloud business backend, ücretsiz local ortam, canonical ownership ve önceki scope istisnaları korunur.

Teknik capability runtime evidence ister. Framework, stakeholder/communication, management görevi proje case artifact'ı, scenario/rubric review ve revision ile doğrulanır. Bir doküman/method adı case practice değildir; teknik olmayan konuya sırf test yazmak da anlamlı runtime application değildir. Eğitim rol simülasyonu gerçek enterprise ekip tecrübesi veya certification iddiasına dönüşmez.

## Seçilmiş gerçek ek deneyler

| Sorumluluk | Eğitim seçimi | Ownership / kapsam |
|---|---|---|
| Dil/paradigma | Java/Kotlin bounded FP; Python/Go/JS/TS mevcut uygulama | Backend owner Java; modern .NET optional read fixture |
| Actors | Apache Pekko typed Java | Bounded job fixture; canonical booking transaction owner değil |
| Data/warehouse | Java Spark local ETL + mevcut ClickHouse | Derived analytics, grain/lineage/dedupe/restart |
| MapReduce/storage | Java Hadoop local; uygun bütçede HDFS pseudo-distributed | Spark aynı fixture karşılaştırması; fiziksel HA değil |
| ESB | Apache Camel SOAP/ACL route | Adapter/integration owner; domain invariant owner değil |
| BPM | Flowable OSS BPMN | Process state; business canonical state değil; BPEL ayrı model/gap |
| Microfrontends | React shell + ayrı Vue/Angular artifact | Versioned UI contract, remote failure/isolation |
| Enterprise integration | ERPNext + Paperless-ngx OSS reference profile | Sahte dataset/service identity/ACL/reconciliation |
| Architecture/framework | UML/C4/structured docs; BABOK/TOGAF/IAF public-scope case | Tailored artifact+review; proprietary/full compliance ayrı |
| Delivery/collaboration | Repo workflow ve scoped framework case | Gerçek küçük release/incident ile simüle roller ayrı |
| Fitness/evaluation | ArchUnit/contract/owner checks ve scenario analysis | Deliberate drift fixture + actual runtime evidence |

## Günlük program

| Day | Milestone |
|---|---|
| [100](roadmap/day-100.md) | Mimari seviyeler, sorumluluklar ve kalite senaryoları |
| [101](roadmap/day-101.md) | Karar verme, iletişim, coaching ve tahmin |
| [102](roadmap/day-102.md) | Dil/paradigma seçimi ve karşılaştırmalı kod |
| [103](roadmap/day-103.md) | OOP, SOLID, DDD, TDD ve presentation pattern'leri |
| [104](roadmap/day-104.md) | Mimari stiller ve seçim koşulları |
| [105](roadmap/day-105.md) | Actors: Apache Pekko ile concurrency ve supervision |
| [106](roadmap/day-106.md) | Mimari dokümantasyon ve UML |
| [107](roadmap/day-107.md) | BABOK, TOGAF ve IAF ile mimari case |
| [108](roadmap/day-108.md) | Yönetim yaklaşımları ve teslimat simülasyonu |
| [109](roadmap/day-109.md) | Spark, ETL ve data warehouse tasarımı |
| [110](roadmap/day-110.md) | Hadoop, HDFS ve MapReduce lab'ı |
| [111](roadmap/day-111.md) | ESB, SOAP, BPM ve BPEL sınırları |
| [112](roadmap/day-112.md) | Microfrontends, reactive ve web standartları |
| [113](roadmap/day-113.md) | Security, network ve operasyon mimarisi audit'i |
| [114](roadmap/day-114.md) | Enterprise Software ve ücretsiz entegrasyon case'i |
| [115](roadmap/day-115.md) | Mimari çalışma araçları ve collaboration |
| [116](roadmap/day-116.md) | Architecture evaluation ve fitness function'ları |
| [117](roadmap/day-117.md) | Altı roadmap ve iki proje final audit |

## Uygulama çalışma modeli

- Önce requirements/ADR/owner/source scope; sonra gerekli küçük code/config spike ve test; ardından actual runtime veya case review/revision; en son evidence/runbook/coverage.
- Ağır actor/data/ERP/DMS profilleri sırayla açılır. CPU/RAM/disk/Java/driver/engine/edition compatibility uygulama gününde doğrulanır/pin edilir.
- Domain data/broker/controller owner'ı sırf pattern çeşitliliği için çoğaltılmaz; yeni fixture'lar isolated capability/derived state kullanır.
- Emlakta mevcut verified capability yeniden kurulmaz; plan satırı alone evidence değildir. Eksik actual görev araçta kalır.
- Ticari vendor ve source/license erişim engelleri [scope belgesinde](coverage/software-architect-access-and-scope.md) açık tutulur. OSS/benzetim exact product kullanımı sayılmaz.

Day 117, altı roadmap'in required konuları ve selected ek profilleri teknik/case/partial/comparison/gap ayrımıyla denetler.
