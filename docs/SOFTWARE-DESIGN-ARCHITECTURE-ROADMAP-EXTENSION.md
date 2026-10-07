# Araç Kiralama — Software Design & Architecture genişletmesi

**Planlandı.** Kullanıcının açık talebiyle [Software Design & Architecture](https://roadmap.sh/software-design-architecture) iki proje scope'una eklendi. Emlak 85 gün, repo ve branch'lerinde değişiklik yoktur. Araç 117→**131 milestone**. Önceki 117 gün korunur; Day 117 ara checkpoint olur. Eksik deneyler Day 118–130, Day 131 final audit'tir. Bir milestone birden fazla takvim gününe yayılabilir.

[97 occurrence kapsam matrisi](coverage/software-design-architecture-coverage.md) ve [kaynak snapshot](coverage/software-design-architecture-roadmap-snapshot.json) node ID bazındadır:13 topic,81 subtopic,3 renkli roadmap kutusu. Kaynakta mor/yeşil tik metadata'sı yoktur; bütün alt konular envantere ve gerçek görev sahibine alınır. Highlighted grup topic'leri ve 9 minimap alt düğümü atlanmaz.

## Mevcut kapsamın yeniden kullanılması

DDD, Clean/Onion/Hexagonal, Vertical Slice, modüler monolit/extraction, SOA, microservices, serverless, MVC, messaging, CQRS ve Event Sourcing iki projenin mevcut planlarında vardır. Plan konusu gerçek uygulama kanıtı değildir; exact SHA/code/runtime/başarı-hata-recovery evidence'ı karşılıyorsa yeniden kurmayız. Eksik evidence/deney araç günlerinde açık görevdir.

Java/Spring Boot/Spring Cloud, Docker/Kubernetes, ücretsiz local/self-hosted ve tek canonical owner kararları değişmez. GoF/PoSA için yeni ağır ürün kurmak gerekmez; Java ve mevcut framework/DB/broker profilleri yeterlidir. İzole lab pattern öğrenir; her pattern product'a taşınmaz.

## Günlük plan

| Gün | Ek öğrenme ve uygulama |
|---|---|
| [118](roadmap/day-118.md) | Clean Code ilkeleri ve davranışı koruyan refactoring |
| [119](roadmap/day-119.md) | Structured, functional ve object-oriented paradigm deneyleri |
| [120](roadmap/day-120.md) | OOP ayrıntıları ve model-driven domain tasarımı |
| [121](roadmap/day-121.md) | SOLID ve tamamlayıcı tasarım ilkeleri |
| [122](roadmap/day-122.md) | GoF — beş creational pattern |
| [123](roadmap/day-123.md) | GoF — yedi structural pattern |
| [124](roadmap/day-124.md) | GoF — on bir behavioral pattern |
| [125](roadmap/day-125.md) | Architectural principles ve component sınırları |
| [126](roadmap/day-126.md) | PoSA — yapı, event handling ve concurrency pattern lab'ı |
| [127](roadmap/day-127.md) | Distributed style — gerçek peer-to-peer deney |
| [128](roadmap/day-128.md) | Microkernel ve Blackboard architectural pattern'leri |
| [129](roadmap/day-129.md) | Enterprise patterns ve ORM davranışlarının doğrulanması |
| [130](roadmap/day-130.md) | Event Sourcing, CQRS ve messaging kapsam doğrulaması |
| [131](roadmap/day-131.md) | Yedi roadmap ve iki proje final kapsam audit'i |

## Somut scope

- Clean Code'nin 13 ayrıntılı ilkesi, structured/functional/OOP paradigm, class/interface/visibility/encapsulation/polymorphism ve rich/anemic model deneyleri.
- SOLID'in 5 ilkesi; composition, vary encapsulation, abstractions, Hollywood, Demeter, Tell don't ask, DRY/YAGNI ayrı ihlal/refactor/test örnekleri.
- **23 GoF pattern**; PoSA seçilmiş yapı/network/concurrency ailesi ve kaynak/volume kapsamı. Kütüphane adı pattern uygulaması değildir.
- **6 component principle** REP/CCP/CRP/ADP/SDP/SAP; policy/detail, coupling/cohesion ve boundary fitness kuralları.
- Gerçek 3 local Java peer; ServiceLoader plugin JAR'lı microkernel; state/control/knowledge source'lu blackboard.
- 11 enterprise alt konusu; JPA/Hibernate identity map, dirty checking/flush/rollback/lazy/N+1/version conflict; Unit of Work ek görevi.
- Event Sourcing ve CQRS mevcut kanıtı reuse veya izole inspection stream/projection lab'ı; replay dış side effect tetiklemez.

## Çalışma ve kapanış

Önce requirement/contract/owner ve gerekli characterization/TDD; sonra bounded code/refactor; CI/build/test; sonra local runtime ve failure/recovery; en son evidence/ADR/knowledgebase/coverage. Case temelli konular artifact+review+revision ile ayrı kapanır.

23 GoF pattern'in hepsi izole lab veya mevcut verified code üzerinden görülür. PoSA label'ı sınırsız kitap serisinin tamamını zorunlu tek milestone'a dönüştürmez: seçilmiş pattern ailesi runtime, diğer family catalog/comparison/ileri backlog açık ayrılır. Peer-to-peer/microkernel/blackboard birbirinin tam alternatifleri değildir; üçünün de kendi behavior'ı uygulanır.

Node business backend/native Desktop-Mobile/ücretli cloud ve SaaS/model API sınırları sürer. Bir günün işi bugün yapıldı veya tüm roadmap uygulanıp doğrulandı iddiası yoktur. Day 131 yedi matrisin evidence/gap audit'idir; emlak değişmez.
