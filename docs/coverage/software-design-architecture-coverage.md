# Software Design & Architecture — İki proje kapsam matrisi

Kaynak: [roadmap.sh/software-design-architecture](https://roadmap.sh/software-design-architecture), canlı graph **2026-10-08 Europe/Istanbul**. [Snapshot](software-design-architecture-roadmap-snapshot.json), [ortak program](../SOFTWARE-DESIGN-ARCHITECTURE-ROADMAP-EXTENSION.md), [gün dizini](../roadmap/README.md).

## Envanter ve kapsam

| Kaynak sınıf | Occurrence | Karar |
|---|---:|---|
| Topic: ana + highlighted grup | 13 | 9 ana alan + Model-Driven Design/Messaging/Distributed/Structural grupları; hepsi görev sahibi |
| Subtopic | 81 | 9 minimap özeti +72 ayrıntılı alt konu; tümü node ID ile eşleşir |
| Renkli roadmap kutusu | 3 | Backend Developer Roadmap, Backend, System Design; iki Backend occurrence ayrı korunur |
| Mor/yeşil tik | 0 | Snapshot metadata'sında yok; renkli button ile tik karıştırılmaz |
| **Eğitim kapsamı** | **97** | Öğrenme + gerçek temsilî uygulama + doğrulama |
| Navigasyon/harici kaynak button | 2 | roadmap.sh navigasyon; Khalil öğrenme yazısı kaynak olarak ayrıca kayıtlı |

Bütün satırlar **Planlandı / evidence henüz yok**. Matris program yükümlülüğüdür; uygulandı iddiası değildir. Emlak 85 gün/branch/kod/doküman değişmez. Araç programı 131 milestone; Day 117 altı-roadmap ara checkpoint, Day 131 yedi-roadmap final audit. Minimap ve tekrar etiketler aynı evidence'ı paylaşabilir ama ID satırı atlanmaz.

Emlak Clean/Onion/Hexagonal/Vertical Slice/DDD/CQRS/Event Sourcing/messaging/SOA kapsamının varlığı plan referansıdır. Exact implementation SHA ve başarı/hata/toparlanma evidence bulunursa yeniden kullanılır; plan tek başına tamamlanma değildir. Eksik teknik kanıtın sahibi aşağıdaki araç günüdür; emlak planını genişleterek kapatma yoktur.

## Node ID bazında görevler

| Node ID | Kaynak etiketi | Sınıf | Owner / gün | Uygulama ve doğrulama yükümlülüğü | Durum |
|---|---|---|---|---|---|
| `TJZgsxpfOmltUUChMzlEM` | Clean Code | Alt konu | Araç / [Day 118](../roadmap/day-118.md) | Refactoring fixture, karakterizasyon/regression; CQS ve effect/dependency sınırı | Planlandı |
| `RgYq3YOJhPGSf5in1Rcdp` | Programming Paradigms | Alt konu | Araç / [Day 119](../roadmap/day-119.md) | Aynı contract'ın structured/functional/OOP üç gerçek Java profili | Planlandı |
| `qZQDOe2MHBh8wNcmvkLQm` | Object Oriented Programming | Alt konu | Araç / [Day 120](../roadmap/day-120.md) | Domain/class model→kod/test izi; rich/anemic ve polymorphism/visibility deneyleri | Planlandı |
| `p96fNXv0Z4rEEXJR9hAYX` | Design Principles | Alt konu | Araç / [Day 121](../roadmap/day-121.md) | İhlal→refactor→regression ve gerçek değişiklik isteği; SOLID beşlisi | Planlandı |
| `gyQw885dvupmkohzJPg3a` | Design Patterns | Alt konu | Araç / [Day 122](../roadmap/day-122.md) | Day 122–124:23 GoF pattern ayrı role/kod/test; product'a zorunlu taşıma yok | Planlandı |
| `XBCxWdpvQyK2iIG2eEA1K` | Architectural Principles | Alt konu | Araç / [Day 125](../roadmap/day-125.md) | REP/CCP/CRP/ADP/SDP/SAP; dependency/change/release ve ArchUnit deliberate violation | Planlandı |
| `En_hvwRvY6k_itsNCQBYE` | Architectural Styles | Alt konu | Araç / [Day 126](../roadmap/day-126.md) | Day 09/104 mevcut code; Day 125–126 layers/component/PoSA runtime scope ve test | Planlandı |
| `jq916t7svaMw5sFOcqZSi` | Architectural Patterns | Alt konu | Araç / [Day 130](../roadmap/day-130.md) | Day 12/24/27/33/103 yeniden kullanılır; Day 130 ES/CQRS append/replay/concurrency/projection audit | Planlandı |
| `WrzsvLgo7cf2KjvJhtJEC` | Enterprise Patterns | Alt konu | Araç / [Day 129](../roadmap/day-129.md) | 11 enterprise alt konusu; Hibernate Identity Map/UoW/SQL/rollback ve domain/application sınırı | Planlandı |
| `pd0_ffU8fTHcg_nLPae6W` | Backend Developer Roadmap | Roadmap bağlantısı | Araç / [Day 131](../roadmap/day-131.md) | Backend/System Design mevcut explicit matrisleri + Day 131 cross-roadmap gerçek kanıt denetimi | Planlandı |
| `08qKtgnhJ3tlb5JKfTDf5` | Clean Code Principles | Ana/grup konusu | Araç / [Day 118](../roadmap/day-118.md) | Refactoring fixture, karakterizasyon/regression; CQS ve effect/dependency sınırı | Planlandı |
| `2SOZvuEcy8Cy8ymN7x4L-` | Be consistent | Alt konu | Araç / [Day 118](../roadmap/day-118.md) | Refactoring fixture, karakterizasyon/regression; CQS ve effect/dependency sınırı | Planlandı |
| `6Cd1BbGsmPJs_5jKhumyV` | Meaningful names over comments | Alt konu | Araç / [Day 118](../roadmap/day-118.md) | Refactoring fixture, karakterizasyon/regression; CQS ve effect/dependency sınırı | Planlandı |
| `81WOL1nxb56ZbAOvxJ7NK` | Indentation and Code Style | Alt konu | Araç / [Day 118](../roadmap/day-118.md) | Refactoring fixture, karakterizasyon/regression; CQS ve effect/dependency sınırı | Planlandı |
| `XEwC6Fyf2DNNHQsoGTrQj` | Keep methods / classes / files small | Alt konu | Araç / [Day 118](../roadmap/day-118.md) | Refactoring fixture, karakterizasyon/regression; CQS ve effect/dependency sınırı | Planlandı |
| `5S5A5wCJUCNPLlHJ5fRjU` | Pure functions | Alt konu | Araç / [Day 118](../roadmap/day-118.md) | Refactoring fixture, karakterizasyon/regression; CQS ve effect/dependency sınırı | Planlandı |
| `qZzl0hAD2LkShsPql1IlZ` | Minimize cyclomatic complexity | Alt konu | Araç / [Day 118](../roadmap/day-118.md) | Refactoring fixture, karakterizasyon/regression; CQS ve effect/dependency sınırı | Planlandı |
| `yyKvmutbxu3iVHTuqr5q4` | Avoid passing nulls, booleans | Alt konu | Araç / [Day 118](../roadmap/day-118.md) | Refactoring fixture, karakterizasyon/regression; CQS ve effect/dependency sınırı | Planlandı |
| `OoCCy-3W5y7bUcKz_iyBw` | Keep framework code distant | Alt konu | Araç / [Day 118](../roadmap/day-118.md) | Refactoring fixture, karakterizasyon/regression; CQS ve effect/dependency sınırı | Planlandı |
| `S1m7ty7Qrzu1rr4Jl-WgM` | Use correct constructs | Alt konu | Araç / [Day 118](../roadmap/day-118.md) | Refactoring fixture, karakterizasyon/regression; CQS ve effect/dependency sınırı | Planlandı |
| `mzt7fvx6ab3tmG1R1NcLO` | Tests should be fast and independent | Alt konu | Araç / [Day 118](../roadmap/day-118.md) | Refactoring fixture, karakterizasyon/regression; CQS ve effect/dependency sınırı | Planlandı |
| `kp86Vc3uue3IxTN9B9p59` | Organize code by actor it belongs to | Alt konu | Araç / [Day 118](../roadmap/day-118.md) | Refactoring fixture, karakterizasyon/regression; CQS ve effect/dependency sınırı | Planlandı |
| `tLbckKmfVxgn59j_dlh8b` | Command query separation | Alt konu | Araç / [Day 118](../roadmap/day-118.md) | Refactoring fixture, karakterizasyon/regression; CQS ve effect/dependency sınırı | Planlandı |
| `9naCfoHF1LW1OEsVZGi8v` | Keep it simple and refactor often | Alt konu | Araç / [Day 118](../roadmap/day-118.md) | Refactoring fixture, karakterizasyon/regression; CQS ve effect/dependency sınırı | Planlandı |
| `TDhTYdEyBuOnDKcQJzTAk` | Programming Paradigms | Ana/grup konusu | Araç / [Day 119](../roadmap/day-119.md) | Aynı contract'ın structured/functional/OOP üç gerçek Java profili | Planlandı |
| `VhSEH_RoWFt1z2lial7xZ` | Structured Programming | Alt konu | Araç / [Day 119](../roadmap/day-119.md) | Aynı contract'ın structured/functional/OOP üç gerçek Java profili | Planlandı |
| `YswaOqZNYcmDwly2IXrTT` | Functional Programming | Alt konu | Araç / [Day 119](../roadmap/day-119.md) | Aynı contract'ın structured/functional/OOP üç gerçek Java profili | Planlandı |
| `VZrERRRYhmqDx4slnZtdc` | Object Oriented Programming | Alt konu | Araç / [Day 120](../roadmap/day-120.md) | Domain/class model→kod/test izi; rich/anemic ve polymorphism/visibility deneyleri | Planlandı |
| `HhYdURE4X-a9GVwJhAyE0` | Object Oriented Programming | Ana/grup konusu | Araç / [Day 120](../roadmap/day-120.md) | Domain/class model→kod/test izi; rich/anemic ve polymorphism/visibility deneyleri | Planlandı |
| `0VO_-1g-TS29y0Ji2yCjc` | Model-Driven Design | Ana/grup konusu | Araç / [Day 120](../roadmap/day-120.md) | Domain/class model→kod/test izi; rich/anemic ve polymorphism/visibility deneyleri | Planlandı |
| `I25ghe8xYWpZ-9pRcHfOh` | Domain Models | Alt konu | Araç / [Day 120](../roadmap/day-120.md) | Domain/class model→kod/test izi; rich/anemic ve polymorphism/visibility deneyleri | Planlandı |
| `c6n-wOHylTbzpxqgoXtdw` | Class Variants | Alt konu | Araç / [Day 120](../roadmap/day-120.md) | Domain/class model→kod/test izi; rich/anemic ve polymorphism/visibility deneyleri | Planlandı |
| `HN160YgryBBtVGjnWxNie` | Layered Architectures | Alt konu | Araç / [Day 120](../roadmap/day-120.md) | Domain/class model→kod/test izi; rich/anemic ve polymorphism/visibility deneyleri | Planlandı |
| `kWNQd3paQrhMHMJzM35w8` | Domain Language | Alt konu | Araç / [Day 120](../roadmap/day-120.md) | Domain/class model→kod/test izi; rich/anemic ve polymorphism/visibility deneyleri | Planlandı |
| `nVaoI4IDPVEsdtFcjGNRw` | Anemic Models | Alt konu | Araç / [Day 120](../roadmap/day-120.md) | Domain/class model→kod/test izi; rich/anemic ve polymorphism/visibility deneyleri | Planlandı |
| `RMkEE7c0jdVFqZ4fmjL6Y` | Abstract Classes | Alt konu | Araç / [Day 120](../roadmap/day-120.md) | Domain/class model→kod/test izi; rich/anemic ve polymorphism/visibility deneyleri | Planlandı |
| `hd6GJ-H4p9I4aaiRTni57` | Concrete Classes | Alt konu | Araç / [Day 120](../roadmap/day-120.md) | Domain/class model→kod/test izi; rich/anemic ve polymorphism/visibility deneyleri | Planlandı |
| `b-YIbw-r-nESVt_PUFQeq` | Scope / Visibility | Alt konu | Araç / [Day 120](../roadmap/day-120.md) | Domain/class model→kod/test izi; rich/anemic ve polymorphism/visibility deneyleri | Planlandı |
| `SrcPhS4F7aT80qNjbv54f` | Interfaces | Alt konu | Araç / [Day 120](../roadmap/day-120.md) | Domain/class model→kod/test izi; rich/anemic ve polymorphism/visibility deneyleri | Planlandı |
| `Dj36yLBShoazj7SAw6a_A` | Inheritance | Alt konu | Araç / [Day 120](../roadmap/day-120.md) | Domain/class model→kod/test izi; rich/anemic ve polymorphism/visibility deneyleri | Planlandı |
| `4DVW4teisMz8-58XttMGt` | Polymorphism | Alt konu | Araç / [Day 120](../roadmap/day-120.md) | Domain/class model→kod/test izi; rich/anemic ve polymorphism/visibility deneyleri | Planlandı |
| `VA8FMrhF4non9x-J3urY8` | Abstraction | Alt konu | Araç / [Day 120](../roadmap/day-120.md) | Domain/class model→kod/test izi; rich/anemic ve polymorphism/visibility deneyleri | Planlandı |
| `GJxfVjhiLuuc36hatx9dP` | Encapsulation | Alt konu | Araç / [Day 120](../roadmap/day-120.md) | Domain/class model→kod/test izi; rich/anemic ve polymorphism/visibility deneyleri | Planlandı |
| `9dMbo4Q1_Sd9wW6-HSCA9` | Design Principles | Ana/grup konusu | Araç / [Day 121](../roadmap/day-121.md) | İhlal→refactor→regression ve gerçek değişiklik isteği; SOLID beşlisi | Planlandı |
| `Izno7xX7wDvwPEg7f_d1Y` | Composition over Inheritance | Alt konu | Araç / [Day 121](../roadmap/day-121.md) | İhlal→refactor→regression ve gerçek değişiklik isteği; SOLID beşlisi | Planlandı |
| `DlefJ9JuJ1LdQYC4WSx6y` | Encapsulate what varies | Alt konu | Araç / [Day 121](../roadmap/day-121.md) | İhlal→refactor→regression ve gerçek değişiklik isteği; SOLID beşlisi | Planlandı |
| `UZeY36dABmULhsHPhlzn_` | Program against abstractions | Alt konu | Araç / [Day 121](../roadmap/day-121.md) | İhlal→refactor→regression ve gerçek değişiklik isteği; SOLID beşlisi | Planlandı |
| `WzUhKlmFB9alTlAyV-MWJ` | Hollywood Principle | Alt konu | Araç / [Day 121](../roadmap/day-121.md) | İhlal→refactor→regression ve gerçek değişiklik isteği; SOLID beşlisi | Planlandı |
| `vnLhItObDgp_XaDmplBsJ` | Law of Demeter | Alt konu | Araç / [Day 121](../roadmap/day-121.md) | İhlal→refactor→regression ve gerçek değişiklik isteği; SOLID beşlisi | Planlandı |
| `0rGdh72HjqPZa2bCbY9Gz` | Tell, don't ask | Alt konu | Araç / [Day 121](../roadmap/day-121.md) | İhlal→refactor→regression ve gerçek değişiklik isteği; SOLID beşlisi | Planlandı |
| `3XckqZA--knUb8IYKOeVy` | SOLID | Alt konu | Araç / [Day 121](../roadmap/day-121.md) | İhlal→refactor→regression ve gerçek değişiklik isteği; SOLID beşlisi | Planlandı |
| `ltBnVWZ3UMAuUvDkU6o4P` | DRY | Alt konu | Araç / [Day 121](../roadmap/day-121.md) | İhlal→refactor→regression ve gerçek değişiklik isteği; SOLID beşlisi | Planlandı |
| `eEO-WeNIyjErBE53n8JsD` | YAGNI | Alt konu | Araç / [Day 121](../roadmap/day-121.md) | İhlal→refactor→regression ve gerçek değişiklik isteği; SOLID beşlisi | Planlandı |
| `Jd79KXxZavpnp3mtE1q0n` | Design Patterns | Ana/grup konusu | Araç / [Day 122](../roadmap/day-122.md) | Day 122–124:23 GoF pattern ayrı role/kod/test; product'a zorunlu taşıma yok | Planlandı |
| `hlHl00ELlK9YdnzHDGnEW` | GoF Design Patterns | Alt konu | Araç / [Day 122](../roadmap/day-122.md) | Day 122–124:23 GoF pattern ayrı role/kod/test; product'a zorunlu taşıma yok | Planlandı |
| `6VoDGFOPHj5p_gvaZ8kTt` | PoSA Patterns | Alt konu | Araç / [Day 126](../roadmap/day-126.md) | Day 09/104 mevcut code; Day 125–126 layers/component/PoSA runtime scope ve test | Planlandı |
| `dBq7ni-of5v1kxpdmh227` | Architectural Principles | Ana/grup konusu | Araç / [Day 125](../roadmap/day-125.md) | REP/CCP/CRP/ADP/SDP/SAP; dependency/change/release ve ArchUnit deliberate violation | Planlandı |
| `8Bm0sRhUg6wZtnvtTmpgY` | Component Principles | Alt konu | Araç / [Day 125](../roadmap/day-125.md) | REP/CCP/CRP/ADP/SDP/SAP; dependency/change/release ve ArchUnit deliberate violation | Planlandı |
| `b_PvjjL2ZpEKETa5_bd0v` | Policy vs Detail | Alt konu | Araç / [Day 125](../roadmap/day-125.md) | REP/CCP/CRP/ADP/SDP/SAP; dependency/change/release ve ArchUnit deliberate violation | Planlandı |
| `TXus3R5vVQDBeBag6B5qs` | Coupling and Cohesion | Alt konu | Araç / [Day 125](../roadmap/day-125.md) | REP/CCP/CRP/ADP/SDP/SAP; dependency/change/release ve ArchUnit deliberate violation | Planlandı |
| `-Kw8hJhgQH2qInUFj2TUe` | Boundaries | Alt konu | Araç / [Day 125](../roadmap/day-125.md) | REP/CCP/CRP/ADP/SDP/SAP; dependency/change/release ve ArchUnit deliberate violation | Planlandı |
| `37xWxG2D9lVuDsHUgLfzP` | Architectural Styles | Ana/grup konusu | Araç / [Day 126](../roadmap/day-126.md) | Day 09/104 mevcut code; Day 125–126 layers/component/PoSA runtime scope ve test | Planlandı |
| `j9j45Auf60kIskyEMUGE3` | Messaging | Ana/grup konusu | Araç / [Day 130](../roadmap/day-130.md) | Day 12/24/27/33/103 yeniden kullanılır; Day 130 ES/CQRS append/replay/concurrency/projection audit | Planlandı |
| `KtzcJBb6-EcIoXnwYvE7a` | Event-Driven | Alt konu | Araç / [Day 130](../roadmap/day-130.md) | Day 12/24/27/33/103 yeniden kullanılır; Day 130 ES/CQRS append/replay/concurrency/projection audit | Planlandı |
| `SX4vOVJY9slOXGwX_q1au` | Publish-Subscribe | Alt konu | Araç / [Day 130](../roadmap/day-130.md) | Day 12/24/27/33/103 yeniden kullanılır; Day 130 ES/CQRS append/replay/concurrency/projection audit | Planlandı |
| `3V74lLPlcOXFB-QRTUA5j` | Distributed | Ana/grup konusu | Araç / [Day 127](../roadmap/day-127.md) | Day 08/104 client-server; Day 127 üç local peer direct message/partition/rejoin | Planlandı |
| `ZGIMUaNfBwE5b6O1yexSz` | Client-Server | Alt konu | Araç / [Day 127](../roadmap/day-127.md) | Day 08/104 client-server; Day 127 üç local peer direct message/partition/rejoin | Planlandı |
| `Cf9Z2wxBcbnNg_q9PA6xA` | Peer-to-Peer | Alt konu | Araç / [Day 127](../roadmap/day-127.md) | Day 08/104 client-server; Day 127 üç local peer direct message/partition/rejoin | Planlandı |
| `86Jw9kMBD7YP5nTV5jTz-` | Structural | Ana/grup konusu | Araç / [Day 126](../roadmap/day-126.md) | Day 09/104 mevcut code; Day 125–126 layers/component/PoSA runtime scope ve test | Planlandı |
| `a0geFJWl-vi3mYytTjYdb` | Component-Based | Alt konu | Araç / [Day 126](../roadmap/day-126.md) | Day 09/104 mevcut code; Day 125–126 layers/component/PoSA runtime scope ve test | Planlandı |
| `xYPR_X1KhBwdpqYzNJiuT` | Monolithic | Alt konu | Araç / [Day 126](../roadmap/day-126.md) | Day 09/104 mevcut code; Day 125–126 layers/component/PoSA runtime scope ve test | Planlandı |
| `IELEJcKYdZ6VN-UIq-Wln` | Layered | Alt konu | Araç / [Day 126](../roadmap/day-126.md) | Day 09/104 mevcut code; Day 125–126 layers/component/PoSA runtime scope ve test | Planlandı |
| `gJYff_qD6XS3dg3I-jJFK` | Architectural Patterns | Ana/grup konusu | Araç / [Day 130](../roadmap/day-130.md) | Day 12/24/27/33/103 yeniden kullanılır; Day 130 ES/CQRS append/replay/concurrency/projection audit | Planlandı |
| `CD20zA6k9FxUpMgHnNYRJ` | Domain-Driven Design | Alt konu | Araç / [Day 130](../roadmap/day-130.md) | Day 12/24/27/33/103 yeniden kullanılır; Day 130 ES/CQRS append/replay/concurrency/projection audit | Planlandı |
| `-arChRC9zG2DBmuSTHW0J` | Model-View Controller | Alt konu | Araç / [Day 130](../roadmap/day-130.md) | Day 12/24/27/33/103 yeniden kullanılır; Day 130 ES/CQRS append/replay/concurrency/projection audit | Planlandı |
| `eJsCCURZAURCKnOK-XeQe` | Microservices | Alt konu | Araç / [Day 130](../roadmap/day-130.md) | Day 12/24/27/33/103 yeniden kullanılır; Day 130 ES/CQRS append/replay/concurrency/projection audit | Planlandı |
| `Kk7u2B67Fdg2sU8E_PGqr` | Blackboard Pattern | Alt konu | Araç / [Day 128](../roadmap/day-128.md) | Java plugin JAR/SPI ve shared blackboard knowledge source/control ayrı gerçek lab | Planlandı |
| `r-Yeca-gpdFM8iq7f0lYQ` | Microkernel | Alt konu | Araç / [Day 128](../roadmap/day-128.md) | Java plugin JAR/SPI ve shared blackboard knowledge source/control ayrı gerçek lab | Planlandı |
| `5WSvAA3h3lmelL53UJSMy` | Serverless Architecture | Alt konu | Araç / [Day 130](../roadmap/day-130.md) | Day 12/24/27/33/103 yeniden kullanılır; Day 130 ES/CQRS append/replay/concurrency/projection audit | Planlandı |
| `GAs6NHBkUgxan3hyPvVs7` | Message Queues / Streams | Alt konu | Araç / [Day 130](../roadmap/day-130.md) | Day 12/24/27/33/103 yeniden kullanılır; Day 130 ES/CQRS append/replay/concurrency/projection audit | Planlandı |
| `K8X_-bsiy7gboInPzbiEb` | Event Sourcing | Alt konu | Araç / [Day 130](../roadmap/day-130.md) | Day 12/24/27/33/103 yeniden kullanılır; Day 130 ES/CQRS append/replay/concurrency/projection audit | Planlandı |
| `FysFru2FJN4d4gj11gv--` | SOA | Alt konu | Araç / [Day 130](../roadmap/day-130.md) | Day 12/24/27/33/103 yeniden kullanılır; Day 130 ES/CQRS append/replay/concurrency/projection audit | Planlandı |
| `IU86cGkLPMXUJKvTBywPu` | CQRS | Alt konu | Araç / [Day 130](../roadmap/day-130.md) | Day 12/24/27/33/103 yeniden kullanılır; Day 130 ES/CQRS append/replay/concurrency/projection audit | Planlandı |
| `h0aeBhQRkDxNeFwDxT4Tf` | Enterprise Patterns | Ana/grup konusu | Araç / [Day 129](../roadmap/day-129.md) | 11 enterprise alt konusu; Hibernate Identity Map/UoW/SQL/rollback ve domain/application sınırı | Planlandı |
| `y_Qj7KITSB8aUWHwiZ2It` | DTOs | Alt konu | Araç / [Day 129](../roadmap/day-129.md) | 11 enterprise alt konusu; Hibernate Identity Map/UoW/SQL/rollback ve domain/application sınırı | Planlandı |
| `tb0X1HtuiGwz7YhQ5xPsV` | Identity Maps | Alt konu | Araç / [Day 129](../roadmap/day-129.md) | 11 enterprise alt konusu; Hibernate Identity Map/UoW/SQL/rollback ve domain/application sınırı | Planlandı |
| `gQ7Xj8tsl6IlCcyJgSz46` | Usecases | Alt konu | Araç / [Day 129](../roadmap/day-129.md) | 11 enterprise alt konusu; Hibernate Identity Map/UoW/SQL/rollback ve domain/application sınırı | Planlandı |
| `8y0ot5sbplUIUyXe9gvc8` | Repositories | Alt konu | Araç / [Day 129](../roadmap/day-129.md) | 11 enterprise alt konusu; Hibernate Identity Map/UoW/SQL/rollback ve domain/application sınırı | Planlandı |
| `ndUTgl2YBzOdu1MQKJocu` | Mappers | Alt konu | Araç / [Day 129](../roadmap/day-129.md) | 11 enterprise alt konusu; Hibernate Identity Map/UoW/SQL/rollback ve domain/application sınırı | Planlandı |
| `tyReIY4iO8kmyc_LPafp1` | Transaction Script | Alt konu | Araç / [Day 129](../roadmap/day-129.md) | 11 enterprise alt konusu; Hibernate Identity Map/UoW/SQL/rollback ve domain/application sınırı | Planlandı |
| `j_SUD3SxpKYZstN9LSP82` | Commands / Queries | Alt konu | Araç / [Day 129](../roadmap/day-129.md) | 11 enterprise alt konusu; Hibernate Identity Map/UoW/SQL/rollback ve domain/application sınırı | Planlandı |
| `Ks6njbfxOHiZ_TrJDnVtk` | Value Objects | Alt konu | Araç / [Day 129](../roadmap/day-129.md) | 11 enterprise alt konusu; Hibernate Identity Map/UoW/SQL/rollback ve domain/application sınırı | Planlandı |
| `NpSfbzYtGebmfrifkKsUf` | Domain Models | Alt konu | Araç / [Day 129](../roadmap/day-129.md) | 11 enterprise alt konusu; Hibernate Identity Map/UoW/SQL/rollback ve domain/application sınırı | Planlandı |
| `VnW_7dl5G0IFL9W3YF_W3` | Entities | Alt konu | Araç / [Day 129](../roadmap/day-129.md) | 11 enterprise alt konusu; Hibernate Identity Map/UoW/SQL/rollback ve domain/application sınırı | Planlandı |
| `SYYulHfDceIyDkDT5fcqj` | ORMs | Alt konu | Araç / [Day 129](../roadmap/day-129.md) | 11 enterprise alt konusu; Hibernate Identity Map/UoW/SQL/rollback ve domain/application sınırı | Planlandı |
| `StxLh1r3qXqyRSqfJGird` | Backend | Roadmap bağlantısı | Araç / [Day 131](../roadmap/day-131.md) | Backend/System Design mevcut explicit matrisleri + Day 131 cross-roadmap gerçek kanıt denetimi | Planlandı |
| `OIcmPSbdsuWapb6HZ4BEi` | System Design | Roadmap bağlantısı | Araç / [Day 131](../roadmap/day-131.md) | Backend/System Design mevcut explicit matrisleri + Day 131 cross-roadmap gerçek kanıt denetimi | Planlandı |

## Pattern ailelerinin kapanış ölçütü

- GoF: Day 122 beş creational, Day 123 yedi structural, Day 124 onbir behavioral = **23** ayrı implementation/test/anti-example satırı. Spring bean veya class adından otomatik pattern coverage çıkarılmaz.
- PoSA: Layers/Pipes and Filters/Broker/MVC + Reactor/Proactor/Acceptor-Connector/Active Object/Monitor Object/Half-Sync-Half-Async/Leader-Followers seçilmiş runtime fixture'ları; Blackboard/Microkernel Day 128 ayrıca bağlıdır. Bu temsilî kapsam kitap serisinin tüm volume'larını bitirme iddiası değildir. Kaynak scope'u ve ileri backlog açık kalır.
- Model-Driven Design: model→code→test trace; otomatik model compiler/codegen/MDA yapıldı iddiası yok. Domain-Driven Design ile bağlantısı ve ayrımı açıklanır.
- Distributed: client-server ve gerçek peer-to-peer direct-message lab; local üç peer production consensus/HA kanıtı değildir.
- Enterprise: DTO/usecase/repository/mapper/entity/value/domain model/commands/queries/transaction script ve scoped ORM Identity Map davranışı; Unit of Work seçilmiş ek konudur.
- Architectural Patterns: Event Sourcing append/replay/optimistic concurrency; CQRS read projection; EDA/pub-sub durable publication farklı semantiklerle doğrulanır. Emlak doğrulanmış kanıt'ı yeterliyse tekrar uygulama şartı yoktur.

Comparison/Design Only zorunlu teknik konuyu kapatmaz. Bu kaynakta yeşil ürün listesi yoktur; başka roadmap'te seçilen yaygın alternatifler mevcut kapsamlarıyla korunur. Yeni isim çeşitliliği için canonical state veya controller owner'ı çoğaltılmaz.


## Design System explicit genişlemesi ve güncel final gate

[Design System127düğüm kapsamı](design-system-coverage.md) ayrıca kullanıcı talebidir. Day 88 foundation korunur; Day 132–142 eksik gerçek görevler; Day 131 yedi-roadmap ara checkpoint; [Day143](../roadmap/day-143.md) sekiz-roadmap final audit. Önceki final ifadeleri tarihsel kapsamıyla okunur; Emlak 85 gün değişmez. Linked UX Design kutusu representative pilot kapsamıdır; UX roadmap'in bütünü otomatik scope değildir.
