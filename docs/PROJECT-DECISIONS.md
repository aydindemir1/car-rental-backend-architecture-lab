# Proje kararları

Karar tarihi: 2026-10-07. Kullanıcı isteği: emlak projesini büyütmeden eksikleri araç kiralama projesinde uygulamak; yeni yaygın alternatifleri seçmek. Bu dosya plan kararlarıdır, uygulama kanıtı değildir.

1. Emlak repo/branch'lerinde bu çalışma kapsamında değişiklik yapılmaz. Eski 85 gün korunur.
2. İkinci proje ana mimarisi microservices'tir. Monolit de birden fazla DB kullanabilir; microservice seçimi öğrenme ve bağımsız capability sahipliği içindir. Day 09–12 aynı temsilî capability üzerinde monolit/extraction deneyini yapar; iki aktif canonical owner bırakmaz.
3. Java/Spring Boot/Spring Cloud ana backend; React/TypeScript ile gerçek frontend ve HTML/CSS temeli. Her language alternatifinin uygulanması zorunlu değildir. JavaScript frontend üzerinden ayrıca kullanılır; Go/Python karşılaştırma kapsamı.
4. Neo4j, Firebase Realtime Database emulator, InfluxDB ve ClickHouse zorunlu yeni öğrenme capability'leridir. Emulator production Firebase değildir; GCP/cloud billing veya gerçek project credentials gerekmez. Emulator host yoksa cloud'a sessiz fallback yapılmaz.
5. Yeni yaygın alternatifler: MariaDB, Memcached, Solr, Nginx, Consul, GitHub Actions full CI, Flux, Linkerd. Emlak counterpart'larıyla farklı repolar üzerinden karşılaştırılır. Aynı runtime/resource nesnesinin competing controller'ları kurulmaz.
6. Ücretli provider şartı yok. AI Spring AI + local Ollama modeliyle yapılır. Model ve embedding lisansı/resource bütçesi kurulurken incelenir. Claude Code/Gemini/OpenAI/Anthropic kullanım örnekleri comparison veya optional provider contract seviyesindedir; paid subscription/API harcaması varsayılmaz.
7. Sarı/mor/mavi bütün konular coverage satırına sahip olur. Konu coverage ile listedeki her alternatif ürünü kurmak farklıdır. Bir dil seç, bir eşdeğer ürün seç gibi başlıklar tek seçimle karşılanır. Yeşil ürünlerden seçilmiş subset uygulanır; diğerleri requirement/uygunluk karşılaştırması. Renk tikleri proficiency certification değildir.
8. Gri API/database konuları da matriste korunur. Sharding/replication toy lab sınırı, gerçek production scale testinden açıkça ayrılır.
9. Snapshot sabittir; web roadmap değişirse sessiz scope genişlemesi olmaz. Coverage diff ve yeni ADR ile program değişir.
10. Her milestone CI→local runtime→evidence→docs/Knowledge Base sırasıyla kapanır. Immutable image promotion, canonical ownership, reliable messaging, idempotency, minimum privilege ve fail-closed güvenlik geçerlidir.

## Status standardı

Planlandı, Implemented, Integrated, Verified, Comparison ve Design Only ayrı tutulur. Bir dosya veya dependency bulunması integration verification değildir. İki projenin tamamı için kapsam tamamlandı ancak gerekli evidence matrisi kapanınca denir.

## Repo/branch kararı

Önerilen repo `aydindemir1/car-rental-backend-architecture-lab`; varsayılan main yalnız başlangıç belgeleri, canonical plan branch'i `docs/car-rental-roadmap-design`. Her implementation milestone önceki kapanmış günün birikimli snapshot'ından türetilir; eski day branch'lerine sonraki kod taşınmaz. Public/private görünürlük repo oluşturma ekranında açıkça belirtilir; dokümanlarda secret yoktur. Repo henüz GitHub'da oluşturulmadıysa oluşturuldu iddiası yapılmaz.
