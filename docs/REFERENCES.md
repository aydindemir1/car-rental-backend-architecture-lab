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


## DevOps genişletme kaynakları

- [DevOps roadmap](https://roadmap.sh/devops) — 2026-10-07 canlı graph, renk/legend ve node ID snapshot.
- [Emlak onaylı DevOps programı](https://github.com/aydindemir1/real-estate-backend-architecture-lab/blob/docs/backend-roadmap-design/docs/DEVOPS-ENGINEERING-PLAN.md)
- [Python](https://docs.python.org/3/), [Go](https://go.dev/doc/), [FreeBSD Handbook](https://docs.freebsd.org/en/books/handbook/)
- [GitLab local Docker installation](https://docs.gitlab.com/install/docker/)
- [CircleCI CLI migration](https://circleci.com/docs/guides/toolkit/cli-migration-guide/) — v1 local execute kaldırıldı; local validation actual managed pipeline değildir.
- [Artifactory OSS](https://jfrog.com/community/download-artifactory-oss/) ve [self-managed release erişimi](https://docs.jfrog.com/releases/docs/artifactory-self-managed-releases)
- [Consul service mesh](https://developer.hashicorp.com/consul/docs/connect)
- [Vault ESO provider](https://external-secrets.io/latest/provider/hashicorp-vault/), [SOPS](https://getsops.io/)
- [Elastic](https://www.elastic.co/docs), [OpenTelemetry](https://opentelemetry.io/docs/), [Jaeger](https://www.jaegertracing.io/docs/)
- [Cloudflare Workers local development](https://developers.cloudflare.com/workers/local-development/)
- [AWS SAM local](https://docs.aws.amazon.com/serverless-application-model/latest/developerguide/using-sam-cli-local.html)
- [Datadog plan/usage](https://docs.datadoghq.com/account_management/plan_and_usage/) — post-trial kullanımın ücretli olabileceği nedeniyle trial zorunlu değildir.

Exact version/license/compatibility ve ücretsiz edition sınırları uygulama gününde yeniden doğrulanır. Resmi kaynağın bulunması erişim lisansını, free service hakkını veya actual integration'ı kanıtlamaz.


## Frontend genişletme kaynakları

- [Frontend roadmap](https://roadmap.sh/frontend) — 2026-10-07 canlı renk/legend/node ID snapshot.
- [MDN Web platform](https://developer.mozilla.org/en-US/docs/Web), [Web Components](https://developer.mozilla.org/en-US/docs/Web/API/Web_components)
- [WAI ARIA Authoring Practices](https://www.w3.org/WAI/ARIA/apg/), [WCAG](https://www.w3.org/WAI/standards-guidelines/wcag/)
- [TypeScript](https://www.typescriptlang.org/docs/), [React](https://react.dev/learn), [React Router](https://reactrouter.com/)
- [Vite migration](https://vite.dev/guide/migration) — Vite 8 Rolldown/Oxc; esbuild/Rollup kullanımı sessiz varsayılmaz.
- [esbuild](https://esbuild.github.io/), [Rollup](https://rollupjs.org/), [SWC](https://swc.rs/docs/getting-started)
- [ESLint](https://eslint.org/docs/latest/), [Prettier](https://prettier.io/docs/), [Biome](https://biomejs.dev/)
- [Vitest](https://vitest.dev/guide/), [Playwright](https://playwright.dev/docs/intro), [Cypress](https://docs.cypress.io/), [Jest](https://jestjs.io/docs/getting-started)
- [Next self-hosting](https://nextjs.org/docs/app/guides/self-hosting), [TanStack Start](https://tanstack.com/start/latest/docs/framework/react/overview), [Astro](https://docs.astro.build/)
- [Apollo Client](https://www.apollographql.com/docs/react/), [Relay](https://relay.dev/docs/)
- [Angular](https://angular.dev/), [Vue](https://vuejs.org/guide/), [Nuxt](https://nuxt.com/docs), [SvelteKit](https://svelte.dev/docs/kit), [Solid](https://docs.solidjs.com/)
- [Lighthouse](https://developer.chrome.com/docs/lighthouse), [Web Vitals](https://web.dev/articles/vitals)
- [GitHub Pages](https://docs.github.com/en/pages), [Cloudflare Pages local](https://developers.cloudflare.com/pages/functions/local-development/)

Sürüm/security/license ve runtime/browser compatibility uygulama gününde doğrulanıp pin edilir. Local validation gerçek provider deployment veya field performance ölçümü değildir.


## Software Architect genişletme kaynakları

- [Software Architect roadmap](https://roadmap.sh/software-architect) — 2026-10-08 live graph snapshot (Europe/Istanbul tarihi).
- [Apache Pekko typed supervision](https://pekko.apache.org/docs/pekko/current/typed/fault-tolerance.html)
- [Spark](https://spark.apache.org/docs/latest/), [Hadoop local/pseudo-distributed](https://hadoop.apache.org/docs/current/hadoop-project-dist/hadoop-common/SingleCluster.html)
- [Apache Camel](https://camel.apache.org/manual/), [Flowable OSS](https://www.flowable.com/open-source-code)
- [IIBA BABOK](https://www.iiba.org/knowledgehub/business-analysis-body-of-knowledge-babok-guide/)
- [TOGAF kaynak/lisans erişimi](https://www.opengroup.org/togaf-licensed-downloads)
- [Capgemini architecture](https://www.capgemini.com/solutions/clean-core-with-mpsa-approach/) — public enterprise-architecture context; proprietary IAF bütün yönteminin açık tam kaynak olduğu varsayılmaz.
- [UML](https://www.omg.org/spec/UML), [C4](https://c4model.com/), [arc42](https://arc42.org/)
- [PMI standards](https://www.pmi.org/standards), [PRINCE2 methodology](https://www.prince2.com/uk/prince2-methodology), [Scrum Guide](https://scrumguides.org/)
- [SEI ATAM](https://www.sei.cmu.edu/library/atam-method-for-architecture-evaluation/)
- [ERPNext/Frappe REST API](https://docs.frappe.io/framework/user/en/api/rest), [Paperless-ngx REST API](https://docs.paperless-ngx.com/api/)

Public kaynaktaki overview ile tüm telifli standard/yönteme erişim farklıdır. Version/licence/access/runtime uyumluluğu uygulama gününde kontrol edilir; sertifikasyon/evaluation/license agreement kullanıcı adına otomatik kabul edilmez. Teknik ürün, model/case ve access gap evidence'ı ayrı tutulur.
