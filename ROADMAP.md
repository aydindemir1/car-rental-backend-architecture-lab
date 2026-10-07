# Araç Kiralama — Eğitim Roadmap'i

Bu program emlak lab'ının 85 günlük planını değiştirmez. Java/Spring Boot/Spring Cloud/Docker/Kubernetes ekseninde eksikleri ve seçilmiş yaygın alternatifleri ayrı araç kiralama domain'inde uygular.

## Sıra ve fazlar

| Günler | Hedef |
|---|---|
| 01–08 | Domain, internet/browser, HTML/CSS/JavaScript/React, Java build ve API |
| 09–18 | Temsilî monolit→mikroservis, MariaDB, ACID, Nginx/cache/auth/security |
| 19–28 | Neo4j/InfluxDB/ClickHouse/Firebase/Solr, messaging, realtime, SOA, Twelve-Factor |
| 29–38 | Test, loadshifting, Docker/K8s, serverless, CI/GitOps/mesh ve DB lab |
| 39–44 | AI temelleri, geliştirme, RAG, streaming, structured output, tools/MCP/agents |
| 45–48 | Full Stack, restore, alternatifler ve Backend/Full Stack ara audit |
| 49–56 | System Design temeli, consistency/failover, DNS/CDN/LB/cache/jobs/protocols |
| 57–63 | Data topology, antipatterns, cloud/messaging/reliability/security pattern lab'ları |
| 64 | Backend + Full Stack + System Design iki proje final audit |

Her gün için [görev/dosya/commit/kanıt planı](docs/roadmap/README.md) vardır. Tek gün birden fazla takvim gününe yayılabilir. Yeni repo uygulama kodu henüz içermez; bütün capabilities Planlandı durumundadır.


## Full Stack roadmap eşleştirmesi

[Full Stack kapsam matrisi](docs/coverage/full-stack-coverage.md) Node.js backend ve Basic AWS Services istisnalarıyla programa dahildir. Day 05 Tailwind, Day 06 npm/React, Day 07 collaborative Git/Java CLI, Day 14 frontend deployment, Day 45 complete app ve Day 46 Monit görevleri ayrıntılı plana eklenmiştir. Emlak programı korunur; 64 milestone gerektiğinde birden fazla takvim gününe yayılır.


## System Design roadmap eşleştirmesi

[System Design kapsam matrisi](docs/coverage/system-design-coverage.md) ve [snapshot](docs/coverage/system-design-roadmap-snapshot.json) programa eklenmiştir. 2026-10-07 canlı diyagramındaki **27 ana konu, 120 alt konu occurrence'ı ve 3 mavi bağlantı** eşleştirilir. Bu snapshot mor/yeşil tik metadata'sı içermediğinden bu renkler varmış gibi sınıflandırılmaz; alt konuların tamamı öğrenme/uygulama/test kapsamına alınır.

Önceki Day 01–47 korunur; Day 48 Backend/Full Stack ara kontrolüdür. Yeni Day 49–63 eksik System Design deneylerini mevcut uygulamalar üzerinde veya izole local profillerde işler; Day 64 bütün kapsamın final audit'idir. Emlakta mevcut datastore/pattern için evidence yeniden kullanılır; kanıtı olmayan plan tamamlanmış sayılmaz. Her eksik zorunlu konu araç kiralamada gerçek görev olarak kalır.
