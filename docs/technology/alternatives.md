# Seçilmiş alternatifler

Seçim tanınırlık/Java ekosistem fit/ücretsiz local kullanım/öğrenme değeriyle yapılır; küresel pazar payı liderliği iddia edilmez.

| Önceki proje | Yeni proje seçimi | Scope |
|---|---|---|
| PostgreSQL/MySQL | MariaDB | Canonical booking OLTP; yeşil alternatif uygulama |
| Redis cache | Memcached | Noncanonical read cache; durable idempotency orada tutulmaz |
| Elasticsearch | Solr | Derived search adapter |
| Traefik edge | Nginx | Static frontend, proxy, TLS ve HTTP cache; mor tikli ürün |
| Eureka | Consul / Spring Cloud Consul | K8s geçişinde ownership ADR; aynı service için dual authority yok |
| Jenkins full CI | GitHub Actions full CI | Local run/resource budget ve trust isolation; paid tier zorunlu değil |
| Argo CD | Flux | GitOps controller alternatif; aynı resource'ta ikisi yok |
| Istio | Linkerd | Temsilî mesh identity/telemetry; ücretsiz local kapsam |
| Existing data stack | Neo4j/InfluxDB/ClickHouse/Firebase emulator | Yeni veri türleri/requirement'lar; dört store birbirinin eşdeğer alternatifi değil |

## Seçilmeyen roadmap alternatifleri

MS SQL/Oracle/SQLite, CouchDB, DynamoDB, ScyllaDB, DGraph, RethinkDB, TimescaleDB, AWS Neptune ve Apache/Caddy/IIS için veri modeli/operasyon/lisans/Java fit comparison notu hazırlanır; hepsi kurulmaz. Cloud ürünleri production olarak local taklit edilmiş sayılmaz. TimescaleDB ve InfluxDB farklı query/relational fit ile karşılaştırılır; ClickHouse doğrudan Firebase alternatifi değildir. Go/Python/Rust/PHP/Ruby/C# için ecosystem comparison; dil seçimi Java kalır. GitLab repo hosting alternatifidir; GitHub kullanımı yeterlidir.

İhtiyaç olmadan örneğin Graph için Neo4j yanında DGraph, cache için Memcached yanında Redis, search için Solr yanında Elasticsearch ikinci runtime owner olmaz. SOAP/HATEOAS/polling gibi protokol karşılaştırma adapter'ları sınırlı lab'da aynı canonical service'i çağırır.
