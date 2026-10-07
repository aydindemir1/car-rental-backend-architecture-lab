# Proje kararları

Karar tarihi: 2026-10-07. Kullanıcı isteği: emlak projesini büyütmeden eksikleri araç kiralama projesinde uygulamak; yeni yaygın alternatifleri seçmek. Bu dosya plan kararlarıdır, uygulama kanıtı değildir.

1. Emlak repo/branch'lerinde bu çalışma kapsamında değişiklik yapılmaz. Eski 85 gün korunur.
2. İkinci proje ana mimarisi microservices'tir. Monolit de birden fazla DB kullanabilir; microservice seçimi öğrenme ve bağımsız capability sahipliği içindir. Day 09–12 aynı temsilî capability üzerinde monolit/extraction deneyini yapar; iki aktif canonical owner bırakmaz.
3. Java/Spring Boot/Spring Cloud ana backend; React/TypeScript ile gerçek frontend ve HTML/CSS temeli. Her language alternatifinin uygulanması zorunlu değildir. JavaScript frontend üzerinden ayrıca kullanılır; Go/Python karşılaştırma kapsamı.
4. Neo 4 j, Firebase Realtime Database emulator, InfluxDB ve ClickHouse zorunlu yeni öğrenme capability'leridir. Emulator production Firebase değildir; GCP/cloud billing veya gerçek project credentials gerekmez. Emulator host yoksa cloud'a sessiz fallback yapılmaz.
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

Canlı graph'ta 27 topic, 120 subtopic occurrence'ı ve 3 mavi bağlantı vardır; mor/yeşil tik bilgisi yoktur. Atlamamak için tüm alt konular günlük öğrenme/uygulama/test kapsamındadır. Aynı etiketin farklı graph düğümleri ayrı ID ile eşleştirilir; aynı doğrulanmış kanıt paylaşılabilir.

Önceden seçilmiş Java/Spring/Kubernetes ve datastore/broker ürünleri korunur. Emlak Cassandra/MongoDB/Redis/Event Sourcing/CQRS görevleri için gerçek evidence yeniden kullanılır; yalnız plan satırı yeterli değildir. Eksik evidence/görev araçta açık kalır. Yeni CoreDNS, HAProxy ve mevcut Nginx profilleri ayrı DNS/L 4/L 7 eğitim rollerine aittir; aynı ingress/resource için competing controller kurulmaz. Cloud pattern'leri yerel uygulamalarla öğrenilir; Azure/AWS/GCP hesabı gerekmez. Geode deneyi iki local read replica ve tek canonical write owner ile sınırlandırılır; üretim multi-region active-active write uygulanmış sayılmaz.


## DevOps roadmap genişletmesi — 2026-10-07

[roadmap.sh/devops](https://roadmap.sh/devops) kullanıcı talebiyle ayrıca scope'tur. Emlak mevcut 85 günlük programa dokunulmaz; araç 64→78 milestone'a genişler. Day 64 önceki üç roadmap ara checkpoint; Day 78 dört roadmap final audit. Eski fazlarda “final” ifadesi kendi checkpoint kapsamını belirtir; yeni nihai owner Day 78'dir.

Live graph: 22 topic, 46 mor, 58 yeşil, 9 gri, 4 tiksiz subtopic; 6 mavi button occurrence'ı (Network Engineer iki kez). Başlangıç/navigasyon button'ları hariç 145 coverage satırı. Her required satırın sahibi/görevi/status'u vardır; paid/cloud istisnaları sessizce alternatifle tamamlanmış sayılmaz.

Python/Go backend migration için değil ayrı operasyon CLI'larıdır. Ubuntu/RHEL türevi/FreeBSD ve GitLab CI/Artifactory/Consul mesh ayrı geçici eğitim profilleridir. Ürün-spesifik mor satırlarda gerekli farklı deneyler uygulanır; canonical runtime/registry/CI/controller seçimi değişmez. Nexus/Harbor ve Terraform/Ansible/Jenkins/Argo/Istio emlak kararları korunur. Yeşil ESO/SOPS için ayrı secret lifecycle sahipliği kullanılır.

Ücretsiz local/self-hosted sınırı daha önce verilmiş karardır. Cloud Providers ve AWS/Azure/GCP gerçek provider kullanımı bu çalışma kapsamında istisna; serverless local SAM/workerd kapsamı Limited/Partial. CircleCI güncel CLI v 1 local execute desteklemez; actual managed pipeline olmadan ürün Verified olmaz. Datadog local agent SaaS monitor yerine geçmez. Ücretsiz ve ücret riski olmayan ürün erişimi yoksa açık gap tutulur; paid/trial/HCP/hesap oluşturma otomatik yapılmaz. Artifactory OSS ücretsiz güncel uygun distribution erişimi uygulama gününde kontrol edilir; yoksa gap kalır.


## Frontend kapsam kararı — 2026-10-07

[roadmap.sh/frontend](https://roadmap.sh/frontend) ayrıca kullanıcı talebiyle scope'tur. **Desktop Apps ve Mobile Apps**, React Native/Flutter/Ionic/Electron/Tauri child occurrence'larıyla hariçtir. PWA responsive web uygulaması olarak kapsamda kalır. Emlak 85 gün değişmez; araç 78→99 milestone'a genişler. Day 78 önceki dört roadmap ara checkpoint; Day 99 beş roadmap final audit'tir.

Snapshot: 30 sarı, 35 mor, 7 mavi, 31 yeşil, 4 gri, 12 tiksiz = 119 eğitim düğümü. Desktop/Mobile 8 düğüm; 5 navigasyon button'ı hariç. Topic sınıfındaki mor/yeşil/gri başlıklar ayrı renk olarak sayılır; her topic otomatik sarı değildir.

React/TypeScript ana portal korunur. Mor Next.js/TanStack Start SSR ve Astro SSG gerçek ayrı profillerdir. Nodejs mavi konu için frontend request-time rendering/lifecycle görevi eklendi; Java business backend/DB owner değişmez. Önceki Full Stack Node business-backend istisnası kalır; önceki statik portal fazının “Node yalnız tooling” ifadesi Day 91 sonrası SSR rendering role'ünü engellemez. Linked Node roadmap'in tamamı kapsam değildir.

Yeşil pnpm/yarn/Bun, Rollup/Parcel/SWC/Rolldown, Biome/Jest/Cypress, Relay, React Router ve Angular/Vue/Nuxt/SvelteKit/Solid/Eleventy/VuePress için bounded gerçek lab'lar planlanır. Same responsibility profilleri ayrı output/runtime'a sahiptir; bir portalda hepsi aynı anda zorunlu dependency/owner olmaz. Copilot/Cursor/Antigravity ve hosting/provider alternatifleri paid erişimsiz Comparison olabilir.

GitHub Pages sahte public static artifact için gerçek ücretsiz deployment evidence ister; uygun erişim yoksa ürün gap'i. Cloudflare yerel runtime Partial'dır; gerçek managed deployment yerel sonuçla doğrulanmış sayılmaz. Ücretli cloud/SaaS/model API ve otomatik account/billing yoktur.


## Software Architect kapsam kararı — 2026-10-08

[roadmap.sh/software-architect](https://roadmap.sh/software-architect) ayrıca scope'tur. Emlak 85 gün değişmez; araç 99→117 milestone. Day 99 önceki beş roadmap ara checkpoint; Day 117 altı roadmap nihai audit. Bu explicit istek önceden linked mavi Software Architect başlığı için gereken representative capability'nin ötesinde bu snapshot'ı ayrıca scope yapar.

Canlı graph 18 topic occurrence (Tools iki kez), 95 tiksiz subtopic ve 4 blue düğüm; navigasyon hariç 117. Mor/yeşil legend yoktur; bu renkler uydurulmaz. Listedeki her language/enterprise product birlikte zorunlu kurulmaz: Java ve seçilmiş Kotlin/ops/frontend dil profilleri; enterprise topic için actual ücretsiz OSS integration, exact ticari vendor'lar ayrı Comparison/access gap.

Teknik konularda actual implementation/runtime/hata/recovery; sorumluluk/communication/framework/management için actual proje case artifact+review+revision kanıtı kullanılır. Bu farklı konu türlerinde “sırf ADR tamamlandı” ile “teknik capability uygulandı” karıştırılmaz. Statüler: Planlandı, Implemented/Integrated/Verified (runtime), Case Applied (vaka+review doğrulandı), Comparison, Design Only, Partial/Access Gap. Şu an tüm yeni görevler Planlandı'dır.

Actors Apache Pekko; ETL Spark Java local; Hadoop MapReduce/HDFS separate bounded lab; ESB Apache Camel; BPM Flowable OSS; enterprise reference ERPNext/Paperless-ngx ayrı local profile olarak planlanır. Exact sürüm/licence/driver/Java/engine/resource compatibility gün başında kontrol edilir. Bunlar canonical booking ownership'i devralmaz. Framework proprietary kaynakları repo'ya kopyalanmaz; paid training/cert/trial/account veya license acceptance otomatik yapılmaz.

BPMN Flowable uygulaması BPEL executed demek değildir; ücretsiz desteklenen engine yoksa BPEL runtime gap. OSS ERP/DMS SAP/Dynamics/Salesforce/IBM/EMC exact ürün deneyimi değildir. Softskill/management workshop eğitim simülasyonuysa bunu gerçek team/enterprise tecrübesi diye sunmayız. Önceki Node backend/native Desktop-Mobile/cloud/SaaS sınırları korunur.


## Software Design & Architecture kapsam kararı — 2026-10-08

[roadmap.sh/software-design-architecture](https://roadmap.sh/software-design-architecture) explicit kullanıcı talebiyle ayrıca scope'tur. Emlak 85 gün, repo ve branch'leri değişmez. Araç 117→**131 milestone**; Day 117 altı-roadmap ara checkpoint; Day 118–130 yeni design lab'ları; Day 131 yedi-roadmap final audit. Önceki kararların final günü kendi tarihsel kapsamıyla okunur; yürürlükte final gate Day 131'dir.

Kaynak 13 topic (9 ana+4 highlighted grup),81 subtopic (9 minimap+72 ayrıntılı) ve 3 renkli roadmap kutusu=97 eğitim occurrence. Mor/yeşil legend yoktur; tüm alt konular node ID ile günlük learning/kod/test sahibidir. Harici Khalil guide ve roadmap.sh navigasyon capability değildir.

Yeni ürün yarışı yerine Java ve mevcut Spring/DB/broker araçlarıyla bounded fixture'lar:23 GoF, seçilmiş PoSA structure/event/concurrency,6 component principle,3 local peer,ServiceLoader plugin microkernel,blackboard,ORMidentitymap/UoW ve ES/CQRS audit. İzole eğitim örneği production default değildir. PoSA bütün kitap serisinin tüm pattern'leri değil explicit seçilmiş pattern ailesi code+kaynak kapsamı katalog kapsamıdır.

Mevcut verified implementation kesin SHA/evidence ile iki projeden birinde yeniden kullanılır; emlak plan satırı tek başına tamamlanmış sayılmaz. Eksik gerçek test/evidence için araç görevleri açıktır. Java/Spring core, ücretsiz local,self-hosted ve tek canonical owner,Node business-backend/native Desktop-Mobile ve provider istisnaları aynen korunur. Bütün yeni işler şu an Planlandı'dır.


## Design System kapsam kararı — 2026-10-08

[roadmap.sh/design-system](https://roadmap.sh/design-system) explicit iki proje kapsamıdır. Emlak 85 gün ve repo/branch/kod/doküman değişmez. Araç 131→**143 milestone**; Day 131 yedi-roadmap ara checkpoint; Day 132–142 eksik tasarım deneyleri; Day 143 sekiz-roadmap final audit. Önceki final ifadeleri tarihsel kapsamıyla okunur; yürürlükteki nihai gate Day 143'tür.

Kaynak 9 topic+115 subtopic+3 renkli roadmap bağlantısı=127 eğitim occurrence;14 context label ayrıca bağlı. Mor/yeşil tik metadata'sı yok; tekrar Accessibility/Documentation/Guidelines/Avatar vb node ID'leri bağlamıyla ayrı tutulur. UX Design mavi bağlantısı representative journey/prototype/task/review/revision kapsamıdır; tüm UX roadmap otomatik yeni kapsam değildir.

Mevcut Day 88 ve React/TS/Java/Spring/CI/telemetry/test kararları korunur. Storybook local catalog; Style Dictionary canonical Git JSON→CSS/TS; ücretsiz local design editor için self-hosted Penpot ve gerçek bounded TypeScript plugin. Figma/Sketch karşılaştırma, ücretli editor/plugin/Chromatic/model API/managed cloud zorunlu değil. Kesin sürüm/API/license/resource uyumluluğu gün başında pin edilir; erişim engeli varsa açık gap, sessiz paid/hosted fallback yok.

20 core component state/keyboard/focus/role/error/test; design language/logo/microcopy; scratch+existing pilot/regional/local A/B; governance/release/contribution/adoption/metrics/communication gerçek teknik veya vaka görevleridir. Design System sadece component library değildir. Automated a11y pass tam WCAG certification; sentetik A/B gerçek conversion; solo simulation gerçek participant/enterprise ekip tecrübesi sayılmaz. Yeni görevlerin tamamı **Planlandı**.
