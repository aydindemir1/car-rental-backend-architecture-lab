# Software Architect — İki proje kapsam matrisi

Kaynak: [roadmap.sh/software-architect](https://roadmap.sh/software-architect), live graph **2026-10-08 Europe/Istanbul**. [Snapshot](software-architect-roadmap-snapshot.json), [ortak plan](../SOFTWARE-ARCHITECT-ROADMAP-EXTENSION.md), [günlük görevler](../roadmap/README.md).

## Kapsam ve kanıt türü

| Canlı sınıf | Occurrence | Scope |
|---|---:|---|
| Sarı ana topic | 18 | İki Tools düğümü ayrı ID; bütün ana konular owner/görev sahibi |
| Mor/yeşil legend | 0 | Snapshot'ta yok; renk/ürün tikleri uydurulmaz |
| Tiksiz subtopic | 95 | Tam envanter; teknik görev, vaka, language choice, Comparison veya access scope açık |
| Mavi konu | 4 | Visit DevOps Roadmap, Backend, System Design, Software Design & Architecture |
| **Toplam eğitim düğümü** | **117** | **22 sarı/mavi required occurrence + 95 tiksiz alt konu** |

Gri `roadmap.sh` navigasyonu eğitim konusu değildir. Aynı Tools label'ı iki ayrı topic'te korunur. Bu roadmap'te green/purple metadata olmadığı için zorunlu tüm language/vendor seçeneklerini birlikte kurma yükümlülüğü çıkarılmaz; her alt konu yine owner/status'a bağlıdır.

**Planlandı.** Kod/case evidence henüz yok. Emlak `docs/backend-roadmap-design` HEAD `a84beefb0d8d932a01056fbd4542910856129a28` planı okunmuş, değiştirilmemiştir. Mevcut emlak backend/architecture/DevOps ve araç Day 01–98 işleri gerçek kanıt ile yeniden kullanılabilir. Day 99 önceki beş roadmap ara checkpoint; Day 100–116 ek deneyler; Day 117 altı roadmap nihai audit.

Teknik konunun evidence'ı gerçek implementation/runtime başarı/hata/toparlanma'dir. Communication/framework/management konusunun evidence'ı gerçek proje case artifact'ı, scenario evaluation, reviewer rubric, feedback ve revision'dır. **Case Applied ≠ teknik ürün Implemented/Verified**. Okuma veya method adı vaka uygulaması sayılmaz; teknik ürün yalnız ADR ile kapatılamaz. [Uygulama sözleşmesi](mandatory-implementation-contract.md).

## 18 ana topic

| Ana topic | Mevcut temel | Günlük owner / uygulama | Status |
|---|---|---|---|
| Understand the Basics | Yeni vaka/teknik spike veya açık access scope | [Day 100](../roadmap/day-100.md) | Planlandı / technical runtime evidence yok |
| Responsibilities | Yeni vaka/teknik spike veya açık access scope | [Day 100](../roadmap/day-100.md) | Vaka planlandı / review-revision evidence yok |
| Important Skills to Learn | Yeni vaka/teknik spike veya açık access scope | [Day 101](../roadmap/day-101.md) | Vaka planlandı / review-revision evidence yok |
| Technical Skills | Yeni vaka/teknik spike veya açık access scope | [Day 116](../roadmap/day-116.md) | Planlandı / technical runtime evidence yok |
| Programming Languages | Yeni vaka/teknik spike veya açık access scope | [Day 102](../roadmap/day-102.md) | Planlandı / technical runtime evidence yok |
| Patterns & Design Principles | Yeni vaka/teknik spike veya açık access scope | [Day 103](../roadmap/day-103.md) | Planlandı / technical runtime evidence yok |
| Tools | İki repo workflow; araç Day 07/34/69 | [Day 115](../roadmap/day-115.md) | Planlandı / technical runtime evidence yok |
| Tools | İki repo workflow; araç Day 07/34/69 | [Day 115](../roadmap/day-115.md) | Planlandı / technical runtime evidence yok |
| Architecture | Araç Day 09–13/27/33/49–63 | [Day 104](../roadmap/day-104.md) | Planlandı / technical runtime evidence yok |
| Security | Araç Day 14/16–18/63/89 | [Day 113](../roadmap/day-113.md) | Planlandı / technical runtime evidence yok |
| Working with Data | Yeni vaka/teknik spike veya açık access scope | [Day 109](../roadmap/day-109.md) | Planlandı / technical runtime evidence yok |
| APIs & Integrations | Yeni vaka/teknik spike veya açık access scope | [Day 111](../roadmap/day-111.md) | Planlandı / technical runtime evidence yok |
| Web, Mobile | Yeni vaka/teknik spike veya açık access scope | [Day 112](../roadmap/day-112.md) | Planlandı / technical runtime evidence yok |
| Frameworks | Yeni vaka/teknik spike veya açık access scope | [Day 107](../roadmap/day-107.md) | Vaka planlandı / review-revision evidence yok |
| Management | Yeni vaka/teknik spike veya açık access scope | [Day 108](../roadmap/day-108.md) | Vaka planlandı / review-revision evidence yok |
| Networks | Araç Day 52–56/68 | [Day 113](../roadmap/day-113.md) | Planlandı / technical runtime evidence yok |
| Operations Knowledge | Emlak Day 46–85; araç Day 49–77 | [Day 113](../roadmap/day-113.md) | Planlandı / technical runtime evidence yok |
| Enterprise Software | Yeni vaka/teknik spike veya açık access scope | [Day 114](../roadmap/day-114.md) | Planlandı / technical runtime evidence yok |

## Ek günlük program

| Day | Milestone | Doğrulama |
|---|---|---|
| [100](../roadmap/day-100.md) | Mimari seviyeler, sorumluluklar ve kalite senaryoları | Üç seviyenin kapsamı/owner'ı tutarlı; en az bir requirement→karar→kod/konfigürasyon→test trace'i çalışır. Değişen requirement'ın failure/capacity etkisi gerçek kanıta bağlıdır. |
| [101](../roadmap/day-101.md) | Karar verme, iletişim, coaching ve tahmin | Review rubric'ine göre requirement, anlaşılabilirlik, seçenek/risk ve ölçülebilir acceptance kontrol edilir; feedback/revision izi vardır. Küçük görev actual effort ve regression evidence'ı üretir; simplification sonrası contract korunur. |
| [102](../roadmap/day-102.md) | Dil/paradigma seçimi ve karşılaştırmalı kod | Pure transform edge case ve API error contract Java/Kotlin fixture'ında doğrulanır. Python/Go/JS/TS mevcut runtime evidence'ı bağlıdır; C# yapılırsa version/runtime ve compatibility sınırlaması ayrı gösterilir. |
| [103](../roadmap/day-103.md) | OOP, SOLID, DDD, TDD ve presentation pattern'leri | Aggregate invariant ve architecture dependency rule gerçek testte korunur; deliberately broken boundary gate'i kırar. TDD commit izi ve üç presentation pattern'inin gerçek kullanıcı/state davranışı kanıtlıdır. |
| [104](../roadmap/day-104.md) | Mimari stiller ve seçim koşulları | Her seçilmiş style gerçek code/runtime fixture ve failure sınırıyla ilişkilidir. Style değiştirme/extraction sonrası API/domain invariant ve rollback/recovery korunur. |
| [105](../roadmap/day-105.md) | Actors: Apache Pekko ile concurrency ve supervision | Mailbox overflow/deadline/supervision/restart davranışı gerçek runtime'da gözlenir. Duplicate iş yan etkisi durable owner'da idempotenttir; actor crash sonrası replay/result sınırı açık ve testlerle doğrulanmışdir. |
| [106](../roadmap/day-106.md) | Mimari dokümantasyon ve UML | Diagram/call/owner ilişkisi gerçek runtime trace ve architecture test ile uyumludur. Requirement/evidence link kontrolü ve review feedback/revision çıktıları tekrarlanabilir. |
| [107](../roadmap/day-107.md) | BABOK, TOGAF ve IAF ile mimari case | Need→requirement→target decision→transition/test trace'i reviewer rubric'iyle denetlenir. Gap/change senaryosu artifact ve actual teknik proof-of-concept'te tutarlı sonuç üretir; erişim sınırı saklanmaz. |
| [108](../roadmap/day-108.md) | Yönetim yaklaşımları ve teslimat simülasyonu | WIP/dependency/blocked-item senaryosu decision/lead-time çıktısı ve improvement trace üretir. Actual küçük release ve incident evidence'ı yönetim case'ine bağlıdır; simüle/gerçek ölçüm ayrımı açıktır. |
| [109](../roadmap/day-109.md) | Spark, ETL ve data warehouse tasarımı | Duplicate/late/malformed record ve restart sonrası aggregate doğru, load idempotenttir. Warehouse grain/lineage/source-of-truth ve schema evolution contract'ı test edilir; local Spark job evidence vardır. |
| [110](../roadmap/day-110.md) | Hadoop, HDFS ve MapReduce lab'ı | Java MapReduce local job'u actual output üretir ve Spark fixture sonucu ile eşleşir. HDFS kullanıldı iddiası ancak daemon/file operation evidence'ıyla yapılır; failure/rerun davranışı testlerle doğrulanmışdir. |
| [111](../roadmap/day-111.md) | ESB, SOAP, BPM ve BPEL sınırları | Camel SOAP mapping/error/recovery ve Flowable BPMN process restart gerçek kanıt üretir. Duplicate process trigger logical işi çoğaltmaz; BPEL Design Only/runtime sınırı matriste ayrı görünür. |
| [112](../roadmap/day-112.md) | Microfrontends, reactive ve web standartları | İki UI artifact'ı bağımsız deploy/rollback ve remote failure testine sahiptir; auth/a 11 y boundary korunur. Reactive backpressure/cancel ve selected browser standard behavior gerçek kanıt ile doğrulanır. |
| [113](../roadmap/day-113.md) | Security, network ve operasyon mimarisi audit'i | PKI wrong trust/hostname/rotation ve firewall/authorization failure actual local runtime'da doğrulanır. Operation audit owner/evidence drift'i bulup düzeltir; provider istisnası full Verified'e karıştırılmaz. |
| [114](../roadmap/day-114.md) | Enterprise Software ve ücretsiz entegrasyon case'i | Actual OSS reference API sync/reconciliation ve schema/auth/outage recovery evidence'ı vardır. Commercial vendor comparison/gap ve uygulanan OSS capability ayrı raporlanır; external system canonical booking owner olmaz. |
| [115](../roadmap/day-115.md) | Mimari çalışma araçları ve collaboration | Decision→issue/ADR→commit→test/evidence trace çalışır ve broken link review'da bulunur. Permission/account sınırları açık; comparison ve actual collaboration tool kullanımı ayrı status'tadır. |
| [116](../roadmap/day-116.md) | Architecture evaluation ve fitness function'ları | Deliberate architecture drift/contract break gate'i kırar; düzeltme sonrası regression başarılıdır. Risk/trade-off kararı gerçek kanıta dayanır; case review ve runtime doğrulaması ayrı raporlanır. |
| [117](../roadmap/day-117.md) | Altı roadmap ve iki proje final audit | Altı roadmap'te required ownersız satır yok; evidence veya explicit gap/istisna ve kapanış ölçütü var. Runtime, case-validation, Comparison ve vendor access statüleri birbirine karıştırılmadan tekrar üretilebilir final rapor teslim edilir. |

## 117 düğümün tam eşleştirmesi

Day dosyaları concrete görev, aday dosya, commit sırası ve kapanış ölçütü içerir. Mevcut plan bir implementation kanıtı değildir; evidence eksikse owner'ın gerçek fixture/case görevi kapanır. Composite Hadoop/Spark/MapReduce satırı Day 109 Spark + Day 110 MapReduce/HDFS evidence'ını; BPM/BPEL satırı actual BPM ile BPEL model/engine ayrımını birlikte denetler.

| Node ID | Canlı sınıf | Etiket | Mevcut temel | Owner / görev | Plan status / sınır |
|---|---|---|---|---|---|
| `4zicbh7Wg2lmKSRhb6E-L` | Sarı ana topic | Understand the Basics | Yeni vaka/teknik spike veya açık access scope | [Day 100](../roadmap/day-100.md) | Planlandı / technical runtime evidence yok |
| `EGG99VA-PEdWdVxNDLtG_` | Tiksiz alt konu | What is Software Architecture | Yeni vaka/teknik spike veya açık access scope | [Day 100](../roadmap/day-100.md) | Vaka planlandı / review-revision evidence yok |
| `eG38hT0rotYJ3G-t9df9R` | Tiksiz alt konu | What is a Software Architect | Yeni vaka/teknik spike veya açık access scope | [Day 100](../roadmap/day-100.md) | Vaka planlandı / review-revision evidence yok |
| `2sR4KULvAUUoOtopvsEBs` | Tiksiz alt konu | Levels of Architecture | Yeni vaka/teknik spike veya açık access scope | [Day 100](../roadmap/day-100.md) | Vaka planlandı / review-revision evidence yok |
| `Lqe47l4j-C4OwkbkwPYry` | Tiksiz alt konu | Application Architecture | Yeni vaka/teknik spike veya açık access scope | [Day 100](../roadmap/day-100.md) | Vaka planlandı / review-revision evidence yok |
| `uGs-9xE3DMJxKhenltbFK` | Tiksiz alt konu | Solution Architecture | Yeni vaka/teknik spike veya açık access scope | [Day 100](../roadmap/day-100.md) | Vaka planlandı / review-revision evidence yok |
| `vlW07sc-FQnxPMjDMn8_F` | Tiksiz alt konu | Enterprise Architecture | Yeni vaka/teknik spike veya açık access scope | [Day 100](../roadmap/day-100.md) | Vaka planlandı / review-revision evidence yok |
| `rUxbG2S2nJuA1YVY6sjiX` | Sarı ana topic | Responsibilities | Yeni vaka/teknik spike veya açık access scope | [Day 100](../roadmap/day-100.md) | Vaka planlandı / review-revision evidence yok |
| `lBtlDFPEQvQ_xtLtehU0S` | Sarı ana topic | Important Skills to Learn | Yeni vaka/teknik spike veya açık access scope | [Day 101](../roadmap/day-101.md) | Vaka planlandı / review-revision evidence yok |
| `fBd2m8tMJmhuNSaakrpg4` | Tiksiz alt konu | Design & Architecture | Yeni vaka/teknik spike veya açık access scope | [Day 101](../roadmap/day-101.md) | Vaka planlandı / review-revision evidence yok |
| `MSDo0nPk_ghRYkZS4MAQ_` | Tiksiz alt konu | Decision Making | Yeni vaka/teknik spike veya açık access scope | [Day 101](../roadmap/day-101.md) | Vaka planlandı / review-revision evidence yok |
| `lrtgF1RTaS4TCKww0aY6C` | Tiksiz alt konu | Simplifying Things | Yeni vaka/teknik spike veya açık access scope | [Day 101](../roadmap/day-101.md) | Planlandı / technical runtime evidence yok |
| `77KvWCA1oHSGgDKBTwjv7` | Tiksiz alt konu | How to Code | Yeni vaka/teknik spike veya açık access scope | [Day 101](../roadmap/day-101.md) | Planlandı / technical runtime evidence yok |
| `5D-kbQ520k1D3fCtD01T7` | Tiksiz alt konu | Documentation | Yeni vaka/teknik spike veya açık access scope | [Day 106](../roadmap/day-106.md) | Vaka planlandı / review-revision evidence yok |
| `Ac49sOlQKblYK4FZuFHDR` | Tiksiz alt konu | Communication | Yeni vaka/teknik spike veya açık access scope | [Day 101](../roadmap/day-101.md) | Vaka planlandı / review-revision evidence yok |
| `m0ZYdqPFDoHOPo18wKyvV` | Tiksiz alt konu | Estimate and Evaluate | Yeni vaka/teknik spike veya açık access scope | [Day 101](../roadmap/day-101.md) | Vaka planlandı / review-revision evidence yok |
| `otHQ6ye1xgkI1qb4tEHVF` | Tiksiz alt konu | Balance | Yeni vaka/teknik spike veya açık access scope | [Day 101](../roadmap/day-101.md) | Vaka planlandı / review-revision evidence yok |
| `LSWlk9A3b6hco9Il_elao` | Tiksiz alt konu | Consult & Coach | Yeni vaka/teknik spike veya açık access scope | [Day 101](../roadmap/day-101.md) | Vaka planlandı / review-revision evidence yok |
| `YW6j3Sg511dXToTcwSnOS` | Tiksiz alt konu | Marketing Skills | Yeni vaka/teknik spike veya açık access scope | [Day 101](../roadmap/day-101.md) | Vaka planlandı / review-revision evidence yok |
| `hFx3mLqh5omNxqI9lfaAQ` | Sarı ana topic | Technical Skills | Yeni vaka/teknik spike veya açık access scope | [Day 116](../roadmap/day-116.md) | Planlandı / technical runtime evidence yok |
| `uoDtVFThaV6OMK2wXGfP5` | Sarı ana topic | Programming Languages | Yeni vaka/teknik spike veya açık access scope | [Day 102](../roadmap/day-102.md) | Planlandı / technical runtime evidence yok |
| `a5DB_hsD4bAf8BtHNFNPo` | Tiksiz alt konu | Java / Kotlin / Scala / Swift | Yeni vaka/teknik spike veya açık access scope | [Day 102](../roadmap/day-102.md) | Java/Kotlin seçimi; Scala/Swift Comparison |
| `j2Ph2QcKwmKlbaMHz1l_i` | Tiksiz alt konu | Python | Araç Day 65 ops araçları | [Day 102](../roadmap/day-102.md) | Planlandı / technical runtime evidence yok |
| `U_Hmzfjjs1jVtu2CZ0TlG` | Tiksiz alt konu | Ruby | Yeni vaka/teknik spike veya açık access scope | [Day 102](../roadmap/day-102.md) | Comparison / exact ürün erişimi yoksa gap |
| `nKlM9k4qAh4wBFXqM-2kC` | Tiksiz alt konu | Go | Araç Day 65 ops araçları | [Day 102](../roadmap/day-102.md) | Planlandı / technical runtime evidence yok |
| `bhP5gMpRVebSFpCeHVXBj` | Tiksiz alt konu | JavaScript / TypeScript | Araç Day 81–82 frontend | [Day 102](../roadmap/day-102.md) | Planlandı / technical runtime evidence yok |
| `D1IXOBUrrXf5bXhVu9cmI` | Tiksiz alt konu | .NET Framework Based | Yeni vaka/teknik spike veya açık access scope | [Day 102](../roadmap/day-102.md) | Seçilmiş modern .NET optional; klasik Framework runtime ayrı |
| `_U0VoTkqM1d6NR13p5azS` | Sarı ana topic | Patterns & Design Principles | Yeni vaka/teknik spike veya açık access scope | [Day 103](../roadmap/day-103.md) | Planlandı / technical runtime evidence yok |
| `AMDLJ_Bup-AY1chl_taV3` | Tiksiz alt konu | OOP | Emlak mimari/CQRS; araç Day 10–11/50/60 | [Day 103](../roadmap/day-103.md) | Planlandı / technical runtime evidence yok |
| `jj5otph6mEYiR-oU5WVtT` | Tiksiz alt konu | MVC, MVP, MVVM | Yeni vaka/teknik spike veya açık access scope | [Day 103](../roadmap/day-103.md) | Planlandı / technical runtime evidence yok |
| `RsnN5bt8OhSMjSFmVgw-X` | Tiksiz alt konu | CQRS, Eventual Consistency | Emlak mimari/CQRS; araç Day 10–11/50/60 | [Day 103](../roadmap/day-103.md) | Planlandı / technical runtime evidence yok |
| `AoWO2BIKG5X4JWir6kh5r` | Tiksiz alt konu | Actors | Yeni vaka/teknik spike veya açık access scope | [Day 105](../roadmap/day-105.md) | Planlandı / technical runtime evidence yok |
| `bbKEEk7dvfFZBBJaIjm0j` | Tiksiz alt konu | ACID, CAP Theorem | Emlak mimari/CQRS; araç Day 10–11/50/60 | [Day 103](../roadmap/day-103.md) | Planlandı / technical runtime evidence yok |
| `QNG-KP01WQnq8o1-In1-n` | Tiksiz alt konu | SOLID | Emlak mimari/CQRS; araç Day 10–11/50/60 | [Day 103](../roadmap/day-103.md) | Planlandı / technical runtime evidence yok |
| `DnP66pjK3b8tCtYr05n2G` | Tiksiz alt konu | TDD | Yeni vaka/teknik spike veya açık access scope | [Day 103](../roadmap/day-103.md) | Planlandı / technical runtime evidence yok |
| `IIelzs8XYMPnXabFKRI51` | Tiksiz alt konu | DDD | Emlak mimari/CQRS; araç Day 10–11/50/60 | [Day 103](../roadmap/day-103.md) | Planlandı / technical runtime evidence yok |
| `diu8MyHxZuZSdhavYVj1T` | Sarı ana topic | Tools | İki repo workflow; araç Day 07/34/69 | [Day 115](../roadmap/day-115.md) | Planlandı / technical runtime evidence yok |
| `ZEzYb-i55hBe9kK3bla94` | Tiksiz alt konu | Git | İki repo workflow; araç Day 07/34/69 | [Day 115](../roadmap/day-115.md) | Planlandı / technical runtime evidence yok |
| `CYnUg_okOcRrD7fSllxLW` | Tiksiz alt konu | Slack | Yeni vaka/teknik spike veya açık access scope | [Day 115](../roadmap/day-115.md) | Comparison / exact ürün erişimi yoksa gap |
| `a6joS9WXg-rbw29_KfBd9` | Tiksiz alt konu | Trello | Yeni vaka/teknik spike veya açık access scope | [Day 115](../roadmap/day-115.md) | Comparison / exact ürün erişimi yoksa gap |
| `3bpd0iZTd3G-H8A7yrExY` | Tiksiz alt konu | Atlassian Tools | Yeni vaka/teknik spike veya açık access scope | [Day 115](../roadmap/day-115.md) | Comparison / exact ürün erişimi yoksa gap |
| `PyTuVs08_z4EhLwhTYzFu` | Tiksiz alt konu | GitHub | İki repo workflow; araç Day 07/34/69 | [Day 115](../roadmap/day-115.md) | Planlandı / technical runtime evidence yok |
| `SuMhTyaBS9vwASxAt39DH` | Sarı ana topic | Tools | İki repo workflow; araç Day 07/34/69 | [Day 115](../roadmap/day-115.md) | Planlandı / technical runtime evidence yok |
| `OaLmlfkZid7hKqJ9G8oNV` | Sarı ana topic | Architecture | Araç Day 09–13/27/33/49–63 | [Day 104](../roadmap/day-104.md) | Planlandı / technical runtime evidence yok |
| `FAXKxl3fWUFShYmoCsInZ` | Tiksiz alt konu | Serverless | Araç Day 09–13/27/33/49–63 | [Day 104](../roadmap/day-104.md) | Planlandı / technical runtime evidence yok |
| `mka_DwiboH5sGFhXhk6ez` | Tiksiz alt konu | Client / Server | Araç Day 09–13/27/33/49–63 | [Day 104](../roadmap/day-104.md) | Planlandı / technical runtime evidence yok |
| `05hLO2_A8Tr6cLJGFRhOh` | Tiksiz alt konu | Layered | Araç Day 09–13/27/33/49–63 | [Day 104](../roadmap/day-104.md) | Planlandı / technical runtime evidence yok |
| `j7OP6RD_IAU6HsyiGaynx` | Tiksiz alt konu | Distributed Systems | Araç Day 09–13/27/33/49–63 | [Day 104](../roadmap/day-104.md) | Planlandı / technical runtime evidence yok |
| `6uvmMgvOwGyuLC5TOhjFu` | Tiksiz alt konu | Service Oriented | Araç Day 09–13/27/33/49–63 | [Day 104](../roadmap/day-104.md) | Planlandı / technical runtime evidence yok |
| `IzFTn5-tQuF_Z0cG_w6CW` | Sarı ana topic | Security | Araç Day 14/16–18/63/89 | [Day 113](../roadmap/day-113.md) | Planlandı / technical runtime evidence yok |
| `7tBAD0ox9hTK4D483GTRo` | Tiksiz alt konu | Hashing Algorithms | Araç Day 14/16–18/63/89 | [Day 113](../roadmap/day-113.md) | Planlandı / technical runtime evidence yok |
| `OpL2EqvHbUmFgnpuhtZPr` | Tiksiz alt konu | PKI | Araç Day 14/16–18/63/89 | [Day 113](../roadmap/day-113.md) | Planlandı / technical runtime evidence yok |
| `KhqUK-7jdClu9M2Pq7x--` | Tiksiz alt konu | OWASP | Araç Day 14/16–18/63/89 | [Day 113](../roadmap/day-113.md) | Planlandı / technical runtime evidence yok |
| `KiwFXB6yd0go30zAFMTJt` | Tiksiz alt konu | Auth Strategies | Araç Day 14/16–18/63/89 | [Day 113](../roadmap/day-113.md) | Planlandı / technical runtime evidence yok |
| `YCJYRA3b-YSm8vKmGUFk5` | Sarı ana topic | Working with Data | Yeni vaka/teknik spike veya açık access scope | [Day 109](../roadmap/day-109.md) | Planlandı / technical runtime evidence yok |
| `92GG4IRZ3FijumC94aL-T` | Tiksiz alt konu | Hadoop, Spark, MapReduce | Yeni vaka/teknik spike veya açık access scope | [Day 109](../roadmap/day-109.md) | Planlandı / technical runtime evidence yok |
| `JUFE4OQhnXOt1J_MG-Sjf` | Tiksiz alt konu | ETL, Datawarehouses | Araç Day 10–11/19–22/37/57; ETL genişletmesi | [Day 109](../roadmap/day-109.md) | Planlandı / technical runtime evidence yok |
| `n5AcBt_u8qtTe3PP9svPZ` | Tiksiz alt konu | SQL Databases | Araç Day 10–11/19–22/37/57; ETL genişletmesi | [Day 109](../roadmap/day-109.md) | Planlandı / technical runtime evidence yok |
| `57liQPaPyVpE-mdLnsbi0` | Tiksiz alt konu | NoSQL Databases | Araç Day 10–11/19–22/37/57; ETL genişletmesi | [Day 109](../roadmap/day-109.md) | Planlandı / technical runtime evidence yok |
| `a0baFv7hVWZGvS5VLh5ig` | Tiksiz alt konu | Apache Spark | Yeni vaka/teknik spike veya açık access scope | [Day 109](../roadmap/day-109.md) | Planlandı / technical runtime evidence yok |
| `I_VjjmMK52_tS8qjQUspN` | Tiksiz alt konu | Hadoop | Yeni vaka/teknik spike veya açık access scope | [Day 110](../roadmap/day-110.md) | Planlandı / technical runtime evidence yok |
| `B5YtP8C1A0jB3MOdg0c_q` | Tiksiz alt konu | Datawarehouse Principles | Araç Day 10–11/19–22/37/57; ETL genişletmesi | [Day 109](../roadmap/day-109.md) | Planlandı / technical runtime evidence yok |
| `Ocn7-ctpnl71ZCZ_uV-uD` | Sarı ana topic | APIs & Integrations | Yeni vaka/teknik spike veya açık access scope | [Day 111](../roadmap/day-111.md) | Planlandı / technical runtime evidence yok |
| `priDGksAvJ05YzakkTFtM` | Tiksiz alt konu | gRPC | Araç Day 08/24/38/56/60/90 | [Day 111](../roadmap/day-111.md) | Planlandı / technical runtime evidence yok |
| `fELnBA0eOoE-d9rSmDJ8l` | Tiksiz alt konu | ESB, SOAP | Yeni vaka/teknik spike veya açık access scope | [Day 111](../roadmap/day-111.md) | Planlandı / technical runtime evidence yok |
| `Sp3FdPT4F9YnTGvlE_vyq` | Tiksiz alt konu | GraphQL | Araç Day 08/24/38/56/60/90 | [Day 111](../roadmap/day-111.md) | Planlandı / technical runtime evidence yok |
| `Ss43xwK1ydEToj6XmmCt7` | Tiksiz alt konu | REST | Araç Day 08/24/38/56/60/90 | [Day 111](../roadmap/day-111.md) | Planlandı / technical runtime evidence yok |
| `DwNda95-fE7LWnDA6u1LU` | Tiksiz alt konu | BPM, BPEL | Yeni vaka/teknik spike veya açık access scope | [Day 111](../roadmap/day-111.md) | Planlandı: BPM runtime; BPEL model/engine gap ayrı |
| `4NVdEbmpQVHpBc7582S6E` | Tiksiz alt konu | Messaging Queues | Araç Day 08/24/38/56/60/90 | [Day 111](../roadmap/day-111.md) | Planlandı / technical runtime evidence yok |
| `j9Y2YbBKi3clO_sZ2L_hQ` | Sarı ana topic | Web, Mobile | Yeni vaka/teknik spike veya açık access scope | [Day 112](../roadmap/day-112.md) | Planlandı / technical runtime evidence yok |
| `6FDGecsHbqY-cm32yTZJa` | Tiksiz alt konu | Functional Programming | Yeni vaka/teknik spike veya açık access scope | [Day 102](../roadmap/day-102.md) | Planlandı / technical runtime evidence yok |
| `mCiYCbKIOVU34qil_q7Hg` | Tiksiz alt konu | React, Vue, Angular | Araç Day 83/91–97 | [Day 112](../roadmap/day-112.md) | Planlandı / technical runtime evidence yok |
| `ulwgDCQi_BYx5lmll7pzU` | Tiksiz alt konu | SPA, SSR, SSG | Araç Day 83/91–97 | [Day 112](../roadmap/day-112.md) | Planlandı / technical runtime evidence yok |
| `vpko5Kyf6BZ5MHpxXOKaf` | Tiksiz alt konu | Microfrontends | Yeni vaka/teknik spike veya açık access scope | [Day 112](../roadmap/day-112.md) | Planlandı / technical runtime evidence yok |
| `s0RvufK2PLMXtlsn2KAUN` | Tiksiz alt konu | W 3 C and WHATWG | Yeni vaka/teknik spike veya açık access scope | [Day 112](../roadmap/day-112.md) | Planlandı / technical runtime evidence yok |
| `C0g_kQFlte5siHMHwlHQb` | Tiksiz alt konu | Reactive Programming | Emlak Day 38; araç frontend/stream | [Day 112](../roadmap/day-112.md) | Planlandı / technical runtime evidence yok |
| `hjlkxYZS7Zf9En3IUS-Wm` | Sarı ana topic | Frameworks | Yeni vaka/teknik spike veya açık access scope | [Day 107](../roadmap/day-107.md) | Vaka planlandı / review-revision evidence yok |
| `LQlzVxUxM3haWRwbhYHKY` | Tiksiz alt konu | BABOK | Yeni vaka/teknik spike veya açık access scope | [Day 107](../roadmap/day-107.md) | Vaka planlandı / review-revision evidence yok |
| `wFu9VO48EYbIQrsM8YUCj` | Tiksiz alt konu | IAF | Yeni vaka/teknik spike veya açık access scope | [Day 107](../roadmap/day-107.md) | Vaka planlandı; proprietary kaynak/full yöntem access scope |
| `8FTKnAKNL9LnZBrw9YXqK` | Tiksiz alt konu | UML | Yeni vaka/teknik spike veya açık access scope | [Day 106](../roadmap/day-106.md) | Vaka planlandı / review-revision evidence yok |
| `5TDTU22Fla2mRr6JeOcaY` | Tiksiz alt konu | TOGAF | Yeni vaka/teknik spike veya açık access scope | [Day 107](../roadmap/day-107.md) | Vaka planlandı / review-revision evidence yok |
| `UyIwiIiKaa6LTQaqzbCam` | Sarı ana topic | Management | Yeni vaka/teknik spike veya açık access scope | [Day 108](../roadmap/day-108.md) | Vaka planlandı / review-revision evidence yok |
| `hRug9yJKYacB9X_2cUalR` | Tiksiz alt konu | PMI | Yeni vaka/teknik spike veya açık access scope | [Day 108](../roadmap/day-108.md) | Vaka planlandı / review-revision evidence yok |
| `Rq1Wi-cHjS54SYo-Btp-e` | Tiksiz alt konu | ITIL | Yeni vaka/teknik spike veya açık access scope | [Day 108](../roadmap/day-108.md) | Vaka planlandı / review-revision evidence yok |
| `SJ5lrlvyXgtAwOx4wvT2W` | Tiksiz alt konu | Prince 2 | Yeni vaka/teknik spike veya açık access scope | [Day 108](../roadmap/day-108.md) | Vaka planlandı / review-revision evidence yok |
| `7rudOREGG-TTkCosU0hNw` | Tiksiz alt konu | RUP | Yeni vaka/teknik spike veya açık access scope | [Day 108](../roadmap/day-108.md) | Vaka planlandı / review-revision evidence yok |
| `qwpsGRFgzAYstM7bJA2ZJ` | Tiksiz alt konu | LeSS | Yeni vaka/teknik spike veya açık access scope | [Day 108](../roadmap/day-108.md) | Vaka planlandı / review-revision evidence yok |
| `Bg7ru1q1j6pNB43HGxnHT` | Tiksiz alt konu | SaFE | Yeni vaka/teknik spike veya açık access scope | [Day 108](../roadmap/day-108.md) | Vaka planlandı / review-revision evidence yok |
| `O7H6dt3Z7EKohxfJzwbPM` | Tiksiz alt konu | Kanban | Yeni vaka/teknik spike veya açık access scope | [Day 108](../roadmap/day-108.md) | Vaka planlandı / review-revision evidence yok |
| `PKqwKvoffm0unwcFwpojk` | Tiksiz alt konu | Scrum | Yeni vaka/teknik spike veya açık access scope | [Day 108](../roadmap/day-108.md) | Vaka planlandı / review-revision evidence yok |
| `7fL9lSu4BD1wRjnZy9tM9` | Tiksiz alt konu | XP | Yeni vaka/teknik spike veya açık access scope | [Day 108](../roadmap/day-108.md) | Vaka planlandı / review-revision evidence yok |
| `cBWJ6Duw99tSKr7U6OW3A` | Sarı ana topic | Networks | Araç Day 52–56/68 | [Day 113](../roadmap/day-113.md) | Planlandı / technical runtime evidence yok |
| `Mt5W1IvuHevNXVRlh7z26` | Tiksiz alt konu | OSI | Araç Day 52–56/68 | [Day 113](../roadmap/day-113.md) | Planlandı / technical runtime evidence yok |
| `UCCT7-E_QUKPg3jAsjobx` | Tiksiz alt konu | TCP/IP Model | Araç Day 52–56/68 | [Day 113](../roadmap/day-113.md) | Planlandı / technical runtime evidence yok |
| `Nq6o6Ty8VyNRsvg-UWp7D` | Tiksiz alt konu | HTTP, HTTPS | Araç Day 52–56/68 | [Day 113](../roadmap/day-113.md) | Planlandı / technical runtime evidence yok |
| `6_EOmU5GYGDGzmNoLY8cB` | Tiksiz alt konu | Proxies | Araç Day 52–56/68 | [Day 113](../roadmap/day-113.md) | Planlandı / technical runtime evidence yok |
| `Hqk_GGsFi14SI5fgPSoGV` | Tiksiz alt konu | Firewalls | Araç Day 52–56/68 | [Day 113](../roadmap/day-113.md) | Planlandı / technical runtime evidence yok |
| `EdJhuNhMSWjeVxGW-RZtL` | Sarı ana topic | Operations Knowledge | Emlak Day 46–85; araç Day 49–77 | [Day 113](../roadmap/day-113.md) | Planlandı / technical runtime evidence yok |
| `igf9yp1lRdAlN5gyQ8HHC` | Tiksiz alt konu | Infrastructure as Code | Emlak Day 46–85; araç Day 49–77 | [Day 113](../roadmap/day-113.md) | Planlandı / technical runtime evidence yok |
| `C0rKd5Rr27Z1_GleoEZxF` | Tiksiz alt konu | Cloud Providers | Yeni vaka/teknik spike veya açık access scope | [Day 113](../roadmap/day-113.md) | Önceki local/no-cloud istisnası; actual provider yok |
| `WoXoVwkSqXTP5U8HtyJOL` | Tiksiz alt konu | Serverless Concepts | Emlak Day 46–85; araç Day 49–77 | [Day 113](../roadmap/day-113.md) | Planlandı / technical runtime evidence yok |
| `XnvlRrOhdoMsiGwGEhBro` | Tiksiz alt konu | Linux / Unix | Emlak Day 46–85; araç Day 49–77 | [Day 113](../roadmap/day-113.md) | Planlandı / technical runtime evidence yok |
| `OErbfM-H3laFm47GCHNPI` | Tiksiz alt konu | Service Mesh | Emlak Day 46–85; araç Day 49–77 | [Day 113](../roadmap/day-113.md) | Planlandı / technical runtime evidence yok |
| `isavRe4ANVn77ZX6gNSLH` | Tiksiz alt konu | CI / CD | Emlak Day 46–85; araç Day 49–77 | [Day 113](../roadmap/day-113.md) | Planlandı / technical runtime evidence yok |
| `l3oeo65FyV5HHvw5n_1wa` | Tiksiz alt konu | Containers | Emlak Day 46–85; araç Day 49–77 | [Day 113](../roadmap/day-113.md) | Planlandı / technical runtime evidence yok |
| `CxceVdaNCyKDhs0huDtcL` | Tiksiz alt konu | Cloud Design Patterns | Emlak Day 46–85; araç Day 49–77 | [Day 113](../roadmap/day-113.md) | Planlandı / technical runtime evidence yok |
| `glz8FmnkNhdmgBUj3EeL2` | Mavi | Visit DevOps Roadmap | Yeni vaka/teknik spike veya açık access scope | [Day 116](../roadmap/day-116.md) | Planlandı / technical runtime evidence yok |
| `8yALyPVUZPtd7LX3GrO1e` | Sarı ana topic | Enterprise Software | Yeni vaka/teknik spike veya açık access scope | [Day 114](../roadmap/day-114.md) | Planlandı / technical runtime evidence yok |
| `gdtI0H_PzzTj_aFQn_NeA` | Tiksiz alt konu | MS Dynamics | Yeni vaka/teknik spike veya açık access scope | [Day 114](../roadmap/day-114.md) | Comparison / exact ürün erişimi yoksa gap |
| `TxWAznp1tUtZ1MvThf9M1` | Tiksiz alt konu | SAP ERP, HANA, Business Objects | Yeni vaka/teknik spike veya açık access scope | [Day 114](../roadmap/day-114.md) | Comparison / exact ürün erişimi yoksa gap |
| `YfYviOXqGVp9C6DuhqBrn` | Tiksiz alt konu | EMC DMS | Yeni vaka/teknik spike veya açık access scope | [Day 114](../roadmap/day-114.md) | Comparison / exact ürün erişimi yoksa gap |
| `5EVecZmvor09LjD7WR_Y9` | Tiksiz alt konu | IBM BPM | Yeni vaka/teknik spike veya açık access scope | [Day 114](../roadmap/day-114.md) | Comparison / exact ürün erişimi yoksa gap |
| `mOXyzdNn8W-9R99ffcnor` | Tiksiz alt konu | Salesforce | Yeni vaka/teknik spike veya açık access scope | [Day 114](../roadmap/day-114.md) | Comparison / exact ürün erişimi yoksa gap |
| `gC8lsIdYLRzo3HzwVqtm1` | Mavi | Backend | Yeni vaka/teknik spike veya açık access scope | [Day 116](../roadmap/day-116.md) | Planlandı / technical runtime evidence yok |
| `U4YFpc82iJ60qD3aYnJkt` | Mavi | System Design | Yeni vaka/teknik spike veya açık access scope | [Day 116](../roadmap/day-116.md) | Planlandı / technical runtime evidence yok |
| `uSLzfLPXxS5-P7ozscvjZ` | Mavi | Software Design & Architecture | Yeni vaka/teknik spike veya açık access scope | [Day 116](../roadmap/day-116.md) | Planlandı / technical runtime evidence yok |
| `b6lCGw82qKpUmsxe1r1f5` | Tiksiz alt konu | Microservices | Araç Day 09–13/27/33/49–63 | [Day 104](../roadmap/day-104.md) | Planlandı / technical runtime evidence yok |

## Uygulama seçimi ve erişim sınırlamaları

- Programming Languages: Java ana backend; Python/Go ops; JS/TS frontend; ek Kotlin bounded fixture. Seçilmiş C# modern .NET optional lab klasik .NET Framework runtime uygulanmış sayılmaz. Ruby/Scala/Swift seçenekleri Comparison olabilir.
- Actors/Pekko, Spark/Hadoop/MapReduce, Camel ESB/Flowable BPM, microfrontends ve OSS enterprise API integration gerçek teknik eğitim görevleridir. Local volume/cluster hiçbir zaman production HA/big-data scale kanıtı değildir.
- BABOK/TOGAF/IAF ve management framework'leri tailored case/overview scope'unda uygulanır. Source/licence/full-method erişimi ayrı; cert/full compliance iddiası yoktur.
- MS Dynamics/SAP/EMC/IBM/Salesforce exact runtime yoksa Comparison/access gap. ERPNext/Paperless actual entegrasyonu **Enterprise Software konusunu** karşılar; bu vendor ürünlerinin kullanıldığı anlamına gelmez.
- Flowable BPMN execution BPEL execution değildir; ücretsiz desteklenen engine yoksa BPEL runtime Design Only/access gap.
- Slack/Trello/Atlassian ürünlerinde actual erişim/scope yoksa Comparison; Git/GitHub/yerel workflow actual case evidence'ı Tools ana konusunu karşılar.
- Önceki cloud/paid-SaaS/Node business backend/native Desktop-Mobile sınırları korunur. Web, Mobile ana konusu actual web ve mobile-client architecture contract değerlendirmesiyle işlenir; native app built iddiası yoktur.

[Kaynak/ürün erişim belgesi](software-architect-access-and-scope.md) bu sınırları ayrı izler.

## Nihai gate

Day 117 altı matristeki required konuları owner, learning/case note, implementation SHA veya case revision, kaynak/sürüm ve anlamlı validation evidence ile denetler. Technical Verified, Case Applied, Partial, Comparison, Design Only ve Access Gap ayrı sayılır. Bütün vendor/dil ürünleri literal uygulandı veya eğitim simülasyonu gerçek enterprise tecrübesi iddiası yapılmaz.


## Yeni explicit kapsam ve final gün güncellemesi — 2026-10-08

[Software Design & Architecture](software-design-architecture-coverage.md) ayrıca 97 node scope'tur. Bu matristeki eski milestone/evidence owner'ları korunur. Day 48/64/78/99/117 kendi roadmap checkpoint'leridir; **[Day 131](../roadmap/day-131.md) yedi-roadmap final audit** yürürlüktedir. Emlak 85 günlük programı değişmez; yeni araç görevleri Planlandı'dır.
