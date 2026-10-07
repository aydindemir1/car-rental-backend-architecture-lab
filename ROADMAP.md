# Araç Kiralama — Eğitim Roadmap'i

Bu program emlak lab'ının 85 günlük planını değiştirmez. Java/Spring Boot/Spring Cloud/Docker/Kubernetes ekseninde eksikleri ve seçilmiş yaygın alternatifleri ayrı araç kiralama domain'inde uygular.

## Sıra ve fazlar

| Günler | Hedef |
|---|---|
| 01–08 | Domain, internet/browser, HTML/CSS/JavaScript/React, Java build ve API |
| 09–18 | Temsilî monolit→mikroservis, MariaDB, ACID, Nginx/cache/auth/security |
| 19–28 | Neo 4 j/InfluxDB/ClickHouse/Firebase/Solr, messaging, realtime, SOA, Twelve-Factor |
| 29–38 | Test, loadshifting, Docker/K 8 s, serverless, CI/GitOps/mesh ve DB lab |
| 39–44 | AI temelleri, geliştirme, RAG, streaming, structured output, tools/MCP/agents |
| 45–48 | Full Stack, restore, alternatifler ve Backend/Full Stack ara audit |
| 49–56 | System Design temeli, consistency/failover, DNS/CDN/LB/cache/jobs/protocols |
| 57–63 | Data topology, antipatterns, cloud/messaging/reliability/security pattern lab'ları |
| 64 | Backend + Full Stack + System Design ara kapsam checkpoint |
| 65–70 | Operasyon dilleri, OS/terminal/network, CI ve IaC |
| 71–76 | Artifact/secrets/logging/mesh/serverless; cloud kapsam sınırları |
| 77–78 | Uçtan uca DevOps tatbikatı ve dört roadmap ara checkpoint |
| 79–90 | HTML/CSS/JS/TS/React, build/test, design system ve güvenli API UI |
| 91–98 | SSR/SSG/performance/PWA/deployment, framework alternatifleri ve frontend AI |
| 99 | Beş roadmap ara kapsam checkpoint |
| 100–108 | Mimari seviyeler, karar/iletişim, ilkeler/actors, dokümantasyon/framework ve yönetim |
| 109–115 | Data engineering, ESB/BPM, microfrontends, trust/operations ve enterprise integration |
| 116–117 | Architecture evaluation/fitness ve altı roadmap ara checkpoint |
| 118–124 | Clean Code, paradigm/OOP/model tasarımı, ilkeler ve 23 GoF pattern |
| 125–130 | Component/PoSA, peer-to-peer, microkernel/blackboard, ORM ve ES/CQRS |
| 131 | Yedi roadmap ara kapsam checkpoint |
| 132–135 | Design System audit, tasarım dili, marka, token, typography ve iconography |
| 136–140 | 20 core component, Storybook/test/release ve local editor/plugin |
| 141–142 | Pilot/UX/regional/A-B ve governance/adoption/operations |
| 143 | Sekiz roadmap ve iki proje final audit |

Her gün için [görev/dosya/commit/kanıt planı](docs/roadmap/README.md) vardır. Tek gün birden fazla takvim gününe yayılabilir. Yeni repo uygulama kodu henüz içermez; bütün capabilities Planlandı durumundadır.


## Full Stack roadmap eşleştirmesi

[Full Stack kapsam matrisi](docs/coverage/full-stack-coverage.md) Node.js backend ve Basic AWS Services istisnalarıyla programa dahildir. Day 05 Tailwind, Day 06 npm/React, Day 07 collaborative Git/Java CLI, Day 14 frontend deployment, Day 45 complete app ve Day 46 Monit görevleri ayrıntılı plana eklenmiştir. Emlak programı korunur; 143 milestone gerektiğinde birden fazla takvim gününe yayılır.


## System Design roadmap eşleştirmesi

[System Design kapsam matrisi](docs/coverage/system-design-coverage.md) ve [snapshot](docs/coverage/system-design-roadmap-snapshot.json) programa eklenmiştir. 2026-10-07 canlı diyagramındaki **27 ana konu, 120 alt konu occurrence'ı ve 3 mavi bağlantı** eşleştirilir. Bu snapshot mor/yeşil tik metadata'sı içermediğinden bu renkler varmış gibi sınıflandırılmaz; alt konuların tamamı öğrenme/uygulama/test kapsamına alınır.

Önceki Day 01–47 korunur; Day 48 Backend/Full Stack ara kontrolüdür. Yeni Day 49–63 eksik System Design deneylerini mevcut uygulamalar üzerinde veya izole local profillerde işler; Day 64 bu üç roadmap için ara checkpoint; Day 78 dört roadmap ara checkpoint; Day 99 beş roadmap ara checkpoint; Day 117 altı roadmap ara checkpoint; Day 131 yedi roadmap ara checkpoint; Day 143 genişletilmiş programın final audit'idir. Emlakta mevcut datastore/pattern için evidence yeniden kullanılır; kanıtı olmayan plan tamamlanmış sayılmaz. Her eksik zorunlu konu araç kiralamada gerçek görev olarak kalır.


## DevOps roadmap eşleştirmesi

[DevOps ortak planı](docs/DEVOPS-ROADMAP-EXTENSION.md), [145 düğümün kapsam matrisi](docs/coverage/devops-coverage.md) ve [canlı snapshot](docs/coverage/devops-roadmap-snapshot.json) programa eklenmiştir. **22 ana başlık, 46 mor tikli alt başlık ve 6 mavi düğüm occurrence'ı** explicit görev/status sahibine bağlıdır. 58 yeşil seçenek ve 13 gri/tiksiz alt konu da envanterde korunur.

Araç programı 143 milestone'dır. Day 65–77 mevcut emlak/araç görevlerinin karşılamadığı deneyleri işler; Day 78 dört roadmap ara checkpoint; Day 117 altı roadmap ara checkpoint; Day 131 yedi roadmap ara checkpoint; Day 143 sekiz roadmap'i birlikte denetler. Emlak 85 gün değişmez; önceki Terraform/Ansible/Jenkins/Nexus/Harbor/Argo CD/Istio kararları yeniden yazılmaz.

**Tam literal ürün uygulaması iddiası yoktur:** Cloud Providers/AWS/Azure/GCP önceki local/no-cloud sınırıyla açık istisnadır. Lambda SAM ve Cloudflare Workers sadece local runtime lab'ıdır. CircleCI/Datadog ürün runtime evidence'ı erişime bağlı açık gap'tir; ücretli/trial zorunluluğu yoktur. Ayrıntılar [kapsam istisnalarında](docs/coverage/devops-cloud-exceptions.md) izlenir.


## Frontend roadmap eşleştirmesi

[Frontend ortak planı](docs/FRONTEND-ROADMAP-EXTENSION.md), [119 düğüm matrisi](docs/coverage/frontend-coverage.md) ve [snapshot](docs/coverage/frontend-roadmap-snapshot.json) eklendi. **30 sarı ana konu, 35 mor occurrence ve 7 mavi konu = 72 required occurrence** günlük görev sahibine bağlıdır. Ayrıca 31 yeşil, 4 gri ve 12 tiksiz düğüm envantere alınmıştır. Desktop Apps/Mobile Apps ve bunlara bağlı 6 native ürün occurrence'ı kapsam dışıdır.

Araç Day 01–77 kapsamı korunur; Day 78 önceki dört roadmap ara checkpoint. Day 79–98 frontend deneyleri, Day 99 beş roadmap ara checkpoint; Day 117 altı roadmap ara checkpoint; Day 131 yedi roadmap ara checkpoint; Day 143 sekiz roadmap final audit'idir. Emlak 85 gün değişmez. Program eğitim milestone'larıdır; 143 takvim gününde bitme şartı yoktur.

Java/Spring business backend korunur. Day 91–92/97 Node.js yalnız ayrı SSR frontend rendering profillerinde kullanılır; önceki Full Stack Node business-backend eğitim istisnası devam eder. CSR/SSG portal Nginx üzerinde korunur; yeni frontend talebindeki SSR, mavi Nodejs ve framework ürünleri gerçek runtime deneyine sahiptir. Cloudflare local/managed ve Pages erişim sınırları matriste açık tutulur.


## Software Architect roadmap eşleştirmesi

[Ortak plan](docs/SOFTWARE-ARCHITECT-ROADMAP-EXTENSION.md), [117 düğüm matrisi](docs/coverage/software-architect-coverage.md) ve [snapshot](docs/coverage/software-architect-roadmap-snapshot.json) 2026-10-08 kullanıcı talebiyle eklendi. Canlı graph **18 ana topic occurrence, 95 tiksiz alt konu ve 4 mavi konu** içerir; mor/yeşil tik metadata'sı yoktur. İki Tools düğümü farklı ID olarak korunur. Bütün konular owner/status'a bağlanır; seçilen diller ve ticari product erişim sınırlamaları açık tutulur.

Araç programı **143 milestone**; Day 99 önceki beş roadmap checkpoint, Day 100–116 Software Architect deneyleri, Day 117 altı roadmap ara checkpoint; Day 131 yedi roadmap ara checkpoint; Day 143 sekiz roadmap final audit'tir. Emlak 85 gün değişmez. Actors/Pekko, Spark/Hadoop/MapReduce, Camel/Flowable, microfrontends, UML/framework ve delivery case'leri mevcut planlarda olmayan açık deneylerdir.

Teknik capability gerçek runtime/test; mimari framework/soft skill/management proje case'i, artifact, scenario review ve revision ile değerlendirilir. Commercial enterprise vendor, BPEL runtime ve framework resource erişimi [sınır belgesinde](docs/coverage/software-architect-access-and-scope.md) izlenir; OSS veya simulation aynı literal ürün kullanımı sayılmaz.


## Software Design & Architecture roadmap eşleştirmesi

[Ortak plan](docs/SOFTWARE-DESIGN-ARCHITECTURE-ROADMAP-EXTENSION.md), [97 düğüm matrisi](docs/coverage/software-design-architecture-coverage.md) ve [snapshot](docs/coverage/software-design-architecture-roadmap-snapshot.json) 2026-10-08 explicit talebiyle eklendi. **13 topic (9 ana+4 grup),81 subtopic (9 minimap+72 ayrıntılı) ve 3 renkli roadmap kutusu** günlük öğrenme/gerçek uygulama/test görevlerine bağlıdır. Mor/yeşil tik metadata'sı yoktur; olmayan renkler uydurulmaz.

Araç programı **143 milestone**. Önceki 117 gün korunur; Day 117 altı-roadmap ara checkpoint, Day 118–130 eksik design/architecture deneyleri, Day 131 yedi-roadmap ara checkpoint; Day 143 sekiz-roadmap final audit'tir. Emlak 85 gün ve repo/branch/kod/doküman değişmez. DDD/CQRS/ES/messaging/microservices/SOA/serverless/MVC gibi mevcut doğrulanmış capability için SHA/evidence yeniden kullanılır; plan satırı yeterli değildir.

Clean Code ve SOLID/complementary principles, **23 GoF**, seçilmiş PoSA families,6 component principle,3 peer P2P, plugin microkernel, blackboard, ORM Identity Map/Unit of Work ve ES/CQRS doğrulaması ayrıntılı günlük görevlere sahiptir. Pattern lab'ı sınırsız üretim dependency'si oluşturmaz; ileri PoSA kitap serisi ile temsilî kaynak kapsamı ayrımı matriste açık tutulur.


## Design System roadmap eşleştirmesi

[Ortak plan](docs/DESIGN-SYSTEM-ROADMAP-EXTENSION.md), [127 düğüm matrisi](docs/coverage/design-system-coverage.md) ve [snapshot](docs/coverage/design-system-roadmap-snapshot.json) explicit kullanıcı talebiyle eklendi. **9 sarı/topic,115 alt konu ve 3 renkli roadmap kutusu** günlük görev sahibidir;14 grup label bağlamı ayrıca korunur. Mor/yeşil metadata yoktur; bütün alt konular kapsanır.

Araç **143 milestone**. Day 88 foundation ve önceki günlük sıra korunur; Day 131 yedi-roadmap ara checkpoint, Day 132–142 yeni Design System deneyleri; Day 143 sekiz-roadmap final audit. Emlak 85 gün ve repo/branch/kod/doküman değişmez.

Storybook local catalog, Style Dictionary token build ve Penpot self-hosted design/editor/plugin seçildi; mevcut React/TS+Java/Spring ve test/CI/telemetry yeniden kullanılır.20 core component, design language/brand/microcopy, from-scratch+existing pilot, regional/A-B, release/contribution/adoption/governance gerçek görevlerdir. UI screenshot/component package tek başına tüm Design System öğrenildi kanıtı değildir; teknik runtime ve vaka review/revision ayrı kapanır.
