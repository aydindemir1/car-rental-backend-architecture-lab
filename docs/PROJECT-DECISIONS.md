# Proje kararları

Karar tarihi: 2026-10-07. Kullanıcı isteği: emlak projesini büyütmeden eksikleri araç kiralama projesinde uygulamak; yeni yaygın alternatifleri seçmek. Bu dosya plan kararlarıdır, uygulama kanıtı değildir.

1. Emlak repo/branch'lerinde bu çalışma kapsamında değişiklik yapılmaz. Eski 85 gün korunur.
2. İkinci proje ana mimarisi microservices'tir. Monolit de birden fazla DB kullanabilir; microservice seçimi öğrenme ve bağımsız capability sahipliği içindir. Day 09–12 aynı temsilî capability üzerinde monolit/extraction deneyini yapar; iki aktif canonical owner bırakmaz.
3. Java/Spring Boot/Spring Cloud ana backend; React/TypeScript ile gerçek frontend ve HTML/CSS temeli. Her language alternatifinin uygulanması zorunlu değildir. JavaScript frontend üzerinden ayrıca kullanılır; Go/Python karşılaştırma kapsamı.
4. Neo4j, Firebase Realtime Database emulator, InfluxDB ve ClickHouse zorunlu yeni öğrenme capability'leridir. Emulator production Firebase değildir; GCP/cloud billing veya gerçek project credentials gerekmez. Emulator host yoksa cloud'a sessiz fallback yapılmaz.
5. Yeni yaygın alternatifler: MariaDB, Memcached, Solr, Nginx, Consul, GitHub Actions full CI, Flux, Linkerd. Emlak counterpart'larıyla farklı repolar üzerinden karşılaştırılır. Aynı runtime/resource nesnesinin competing controller'ları kurulmaz.
6. Ücretli provider şartı yok. AI Spring AI + local Ollama modeliyle yapılır. Model ve embedding lisansı/resource bütçesi kurulurken incelenir. Claude Code Day 40'ta Ollama'nın yerel Anthropic-compatible endpoint'i ve yerel model ile gerçekten kullanılır; cloud model veya ücretli Anthropic API zorunlu değildir. CLI/model lisansı, sürüm ve resource uyumluluğu gün başında doğrulanır; kullanılamazsa konu Comparison ile kapatılmaz, açık gap kalır. Gemini/OpenAI/Anthropic provider seçenekleri ayrı comparison kapsamıdır.
7. Sarı/mor/mavi bütün konular en az bir projenin günlük programında açık öğrenme, temsilî uygulama ve doğrulama görevine sahip olmalıdır. Yalnız coverage satırı veya karşılaştırma belgesi zorunlu konunun tamamlanması için yeterli değildir. Konu coverage ile listedeki her alternatif ürünü kurmak farklıdır. Bir dil seç, bir eşdeğer ürün seç gibi başlıklar tek seçimle karşılanır. Yeşil ürünlerden MariaDB/Memcached/Solr yanında SQLite, TimescaleDB ve CouchDB de ayrı eğitim use-case'lerinde uygulanır; diğerleri requirement/uygunluk karşılaştırması. Renk tikleri proficiency certification değildir.
8. Gri API/database konuları da matriste korunur. Sharding/replication toy lab sınırı, gerçek production scale testinden açıkça ayrılır.
9. Snapshot sabittir; web roadmap değişirse sessiz scope genişlemesi olmaz. Coverage diff ve yeni ADR ile program değişir.
10. Her milestone CI→local runtime→evidence→docs/Knowledge Base sırasıyla kapanır. Immutable image promotion, canonical ownership, reliable messaging, idempotency, minimum privilege ve fail-closed güvenlik geçerlidir.

## Status standardı

Planlandı, Implemented, Integrated, Verified, Comparison ve Design Only ayrı tutulur. Bir dosya veya dependency bulunması integration verification değildir. İki projenin tamamı için kapsam tamamlandı ancak gerekli evidence matrisi kapanınca denir.

## Repo/branch kararı

Önerilen repo `aydindemir1/car-rental-backend-architecture-lab`; varsayılan main yalnız başlangıç belgeleri, canonical plan branch'i `docs/car-rental-roadmap-design`. Her implementation milestone önceki kapanmış günün birikimli snapshot'ından türetilir; eski day branch'lerine sonraki kod taşınmaz. Public/private görünürlük repo oluşturma ekranında açıkça belirtilir; dokümanlarda secret yoktur. Repo henüz GitHub'da oluşturulmadıysa oluşturuldu iddiası yapılmaz.


## Zorunlu kapsamın kapanış kararı — 2026-10-07

Emlak projesinin 85 günü değişmez. Eksik zorunlu konunun uygulama sorumluluğu araç kiralama projesindedir. Sarı başlık ve mavi konu yalnız ad olarak kayıtlı bırakılmaz; günlük görev ve ölçülebilir test bulunur. Mor tikli ürün (örneğin Nginx/Claude Code) sırf başka araç kullanıldı diye kendiliğinden karşılanmış sayılmaz.

“Bir backend dili seç” başlığında Java seçimi yeterlidir; Go/Python gibi diğer dil seçeneklerini birlikte zorunlu yapmak başlığın anlamıyla çelişir. Mavi bağlantıda istenen konu gerçekten uygulanır; bağlantı verilen başka roadmap'in bütün alt dalları sessizce yeni scope olmaz. Bu iki semantik sınır [zorunlu uygulama sözleşmesinde](coverage/mandatory-implementation-contract.md) kayıtlıdır.


## Full Stack kapsam kararı — 2026-10-07

[roadmap.sh/full-stack](https://roadmap.sh/full-stack) da iki proje kapsamına eklenmiştir. Node.js backend eğitimi/uygulaması ve Basic AWS Services tamamen istisnadır; AWS alt ürünleri ve mavi AWS kutusu da kapsam dışıdır. npm/frontend build/test için gereken yerel Node executable araç zinciri rolündedir, backend platformu değildir. Backend Java/Spring Boot/Spring Cloud kalır. Sarı ana konuların ve uygulanabilir mavi başlıkların sahibi [Full Stack matrisinde](coverage/full-stack-coverage.md) kayıtlıdır. Eksik npm, Tailwind ve Monit görevleri araç Day 05–06 ve Day 46'ya eklenmiştir. Emlak 85 günlük programı değişmez. Yeşil alternatifler varsa requirement ile seçilir; bu snapshot'ta olmayan tik/ürünler uydurulmaz.


## System Design kapsam kararı — 2026-10-07

Kullanıcının açık talebiyle [System Design roadmap](https://roadmap.sh/system-design) bağımsız kapsam olarak eklendi. Araç kiralama programı 48'den **64 milestone**'a genişler; emlak 85 gün değişmez. Day 48 ara Backend/Full Stack audit; Day 64 üç roadmap final audit. Bu genişleme başka bir mavi roadmap bağlantısından çıkarılan örtük scope değildir.

Canlı graph'ta 27 topic, 120 subtopic occurrence'ı ve 3 mavi bağlantı vardır; mor/yeşil tik bilgisi yoktur. Atlamamak için tüm alt konular günlük öğrenme/uygulama/test kapsamındadır. Aynı etiketin farklı graph düğümleri ayrı ID ile eşleştirilir; aynı verified evidence paylaşılabilir.

Önceden seçilmiş Java/Spring/Kubernetes ve datastore/broker ürünleri korunur. Emlak Cassandra/MongoDB/Redis/Event Sourcing/CQRS görevleri için gerçek evidence yeniden kullanılır; yalnız plan satırı yeterli değildir. Eksik evidence/görev araçta açık kalır. Yeni CoreDNS, HAProxy ve mevcut Nginx profilleri ayrı DNS/L4/L7 eğitim rollerine aittir; aynı ingress/resource için competing controller kurulmaz. Cloud pattern'leri yerel uygulamalarla öğrenilir; Azure/AWS/GCP hesabı gerekmez. Geode deneyi iki local read replica ve tek canonical write owner ile sınırlandırılır; üretim multi-region active-active write uygulanmış sayılmaz.


## DevOps roadmap genişletmesi — 2026-10-07

[roadmap.sh/devops](https://roadmap.sh/devops) kullanıcı talebiyle ayrıca scope'tur. Emlak mevcut 85 günlük programa dokunulmaz; araç 64→78 milestone'a genişler. Day 64 önceki üç roadmap ara checkpoint; Day 78 dört roadmap final audit. Eski fazlarda “final” ifadesi kendi checkpoint kapsamını belirtir; yeni nihai owner Day 78'dir.

Live graph: 22 topic, 46 mor, 58 yeşil, 9 gri, 4 tiksiz subtopic; 6 mavi button occurrence'ı (Network Engineer iki kez). Başlangıç/navigasyon button'ları hariç 145 coverage satırı. Her required satırın sahibi/görevi/status'u vardır; paid/cloud istisnaları sessizce alternatifle tamamlanmış sayılmaz.

Python/Go backend migration için değil ayrı operasyon CLI'larıdır. Ubuntu/RHEL türevi/FreeBSD ve GitLab CI/Artifactory/Consul mesh ayrı geçici eğitim profilleridir. Ürün-spesifik mor satırlarda gerekli farklı deneyler uygulanır; canonical runtime/registry/CI/controller seçimi değişmez. Nexus/Harbor ve Terraform/Ansible/Jenkins/Argo/Istio emlak kararları korunur. Yeşil ESO/SOPS için ayrı secret lifecycle sahipliği kullanılır.

Ücretsiz local/self-hosted sınırı daha önce verilmiş karardır. Cloud Providers ve AWS/Azure/GCP gerçek provider kullanımı bu çalışma kapsamında istisna; serverless local SAM/workerd kapsamı Limited/Partial. CircleCI güncel CLI v1 local execute desteklemez; actual managed pipeline olmadan ürün Verified olmaz. Datadog local agent SaaS monitor yerine geçmez. Ücretsiz ve ücret riski olmayan ürün erişimi yoksa açık gap tutulur; paid/trial/HCP/hesap oluşturma otomatik yapılmaz. Artifactory OSS ücretsiz güncel uygun distribution erişimi uygulama gününde kontrol edilir; yoksa gap kalır.


## Frontend kapsam kararı — 2026-10-07

[roadmap.sh/frontend](https://roadmap.sh/frontend) ayrıca kullanıcı talebiyle scope'tur. **Desktop Apps ve Mobile Apps**, React Native/Flutter/Ionic/Electron/Tauri child occurrence'larıyla hariçtir. PWA responsive web uygulaması olarak kapsamda kalır. Emlak 85 gün değişmez; araç 78→99 milestone'a genişler. Day 78 önceki dört roadmap ara checkpoint; Day 99 beş roadmap final audit'tir.

Snapshot: 30 sarı, 35 mor, 7 mavi, 31 yeşil, 4 gri, 12 tiksiz = 119 eğitim düğümü. Desktop/Mobile 8 düğüm; 5 navigasyon button'ı hariç. Topic sınıfındaki mor/yeşil/gri başlıklar ayrı renk olarak sayılır; her topic otomatik sarı değildir.

React/TypeScript ana portal korunur. Mor Next.js/TanStack Start SSR ve Astro SSG gerçek ayrı profillerdir. Nodejs mavi konu için frontend request-time rendering/lifecycle görevi eklendi; Java business backend/DB owner değişmez. Önceki Full Stack Node business-backend istisnası kalır; önceki statik portal fazının “Node yalnız tooling” ifadesi Day 91 sonrası SSR rendering role'ünü engellemez. Linked Node roadmap'in tamamı kapsam değildir.

Yeşil pnpm/yarn/Bun, Rollup/Parcel/SWC/Rolldown, Biome/Jest/Cypress, Relay, React Router ve Angular/Vue/Nuxt/SvelteKit/Solid/Eleventy/VuePress için bounded gerçek lab'lar planlanır. Same responsibility profilleri ayrı output/runtime'a sahiptir; bir portalda hepsi aynı anda zorunlu dependency/owner olmaz. Copilot/Cursor/Antigravity ve hosting/provider alternatifleri paid erişimsiz Comparison olabilir.

GitHub Pages sahte public static artifact için gerçek ücretsiz deployment evidence ister; uygun erişim yoksa ürün gap'i. Cloudflare yerel runtime Partial'dır; gerçek managed deployment yerel sonuçla doğrulanmış sayılmaz. Ücretli cloud/SaaS/model API ve otomatik account/billing yoktur.
