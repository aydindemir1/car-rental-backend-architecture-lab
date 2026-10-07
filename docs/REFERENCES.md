# Kaynaklar ve sürüm politikası

- [Backend roadmap](https://roadmap.sh/backend) — konu/tik snapshot tarihi 2026-10-07.
- [Emlak canonical plan](https://github.com/aydindemir1/real-estate-backend-architecture-lab/tree/docs/backend-roadmap-design) — Day 1–85, karşılaştırma başlangıç HEAD'i `a84beefb0d8d932a01056fbd4542910856129a28`.
- [Firebase Local Emulator Suite](https://firebase.google.com/docs/emulator-suite)
- [Spring AI](https://docs.spring.io/spring-ai/reference/)
- [Knative](https://knative.dev/docs/)
- [InfluxDB 3 Core](https://docs.influxdata.com/influxdb3/core/)
- [Neo4j](https://neo4j.com/docs/)
- [ClickHouse](https://clickhouse.com/docs)
- [Nginx](https://nginx.org/en/docs/)
- [OWASP](https://owasp.org/)

Exact sürüm day başında resmi compatibility/support/license matrix'ten seçilip pin edilir. Spring Boot/Cloud/AI BOM, Java, datastore driver/server, container/chart/CRD uyumluluğu birlikte kaydedilir. Floating latest yok. Free local distribution lisansının her ürün için aynı olduğu veya wholecloud feature parity olduğu varsayılmaz.

Roadmap static PDF'si canlı diyagramdan farklı olabilir; coverage canlı düğüm snapshot'ını esas alır. Mavi bağlantının hedef yol haritasının her alt konusu bu repo kapsamına otomatik girmez; ilgili capability öğrenme/evidence hedefi burada açıkça tanımlanır.

- [Claude Code ile yerel Ollama entegrasyonu](https://docs.ollama.com/integrations/claude-code) — local model seçimi; cloud ürün erişimi varsayılmaz.


## Full Stack ek kaynakları

- [Full Stack roadmap](https://roadmap.sh/full-stack) — 2026-10-07 snapshot.
- [npm](https://docs.npmjs.com/about-npm/)
- [Tailwind CSS ve Vite](https://tailwindcss.com/docs/installation/using-vite)
- [Monit resmi manual](https://mmonit.com/monit/documentation/monit.html)

Exact version/license/support, ilgili uygulama gününde doğrulanır. Paid M/Monit veya Tailwind Plus gerekmez.


## System Design ek kaynakları

- [System Design roadmap](https://roadmap.sh/system-design) — 2026-10-07 canlı graph snapshot.
- [Kubernetes Leases](https://kubernetes.io/docs/concepts/architecture/leases/)
- [CoreDNS manual](https://coredns.io/manual/toc/)
- [HAProxy resmi dokümantasyon](https://www.haproxy.org/#docs)
- [Microsoft Cloud Design Patterns](https://learn.microsoft.com/en-us/azure/architecture/patterns/) — pattern kavramı; Azure deployment şartı değil.
- [Deployment Stamps](https://learn.microsoft.com/en-us/azure/architecture/patterns/deployment-stamp)
- [Geodes](https://learn.microsoft.com/en-us/azure/architecture/patterns/geodes)
- [Scheduler Agent Supervisor](https://learn.microsoft.com/en-us/azure/architecture/patterns/scheduler-agent-supervisor)
- [Sequential Convoy](https://learn.microsoft.com/en-us/azure/architecture/patterns/sequential-convoy)
- [Claim Check](https://learn.microsoft.com/en-us/azure/architecture/patterns/claim-check)
- [Gatekeeper](https://learn.microsoft.com/en-us/azure/architecture/patterns/gatekeeper)
- [Valet Key](https://learn.microsoft.com/en-us/azure/architecture/patterns/valet-key)

Pattern'lerin yerel eğitim adaptasyonu, tüm cloud ürün özelliklerini veya fiziksel fault-domain garantilerini sağlamaz. Ürün/version/support/license doğrulaması uygulama gününde yapılır.
