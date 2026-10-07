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
