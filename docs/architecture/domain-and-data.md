# Domain ve datastore sahipliği

| Capability | Planlanan owner/store | Gerekçe ve invariant |
|---|---|---|
| Booking/Rental | BookingService / MariaDB | Rezervasyon zaman çakışması, fiyat sözleşmesi, teslim/iade lifecycle; DB constraint/transaction |
| Pricing | PricingService / MariaDB ayrı schema/credential | Canonical tarife ve quote; Memcached yalnız türetilmiş hızlandırma |
| Fleet ilişkileri | FleetGraphService / Neo4j | Şube/araç/özellik/bakım graph traversal; booking mutation yapmaz |
| Araç sample telemetrisi | TelemetryService / InfluxDB | Time window/sensor retention/cardinality; canonical booking verisi değil |
| Kiralama analytics | AnalyticsService / ClickHouse | Utilization/gelir projection ve OLAP aggregation; replay edilebilir |
| Canlı durum panosu | RealtimeService / Firebase Realtime Database emulator | Auth kontrollü status projection; gerçek availability owner değil |
| Araç arama | SearchService / Solr | Full-text/filter derived projection; booking öncesi canonical availability doğrulanır |
| Web/AI composition | BFF ve Assistant | Canonical business state owner değil; tool action owner serviste kontrol edilir |

Inter-service database query/join yok; API/event/projection kullanılır. Çift rezervasyon sadece graf veya cache okumasıyla engellenmez. MariaDB transaction içinde remote broker/network çağrısı yok; Outbox durable publication, inbox/dedup ve bounded retry/replay davranışı test edilir. Telemetry/analytics/Firebase projection gecikmesi business correctness bozamaz.

Ödeme initial scope'ta açıkça mock adapter'dır; gerçek card/PII ya da ticari araç kiralama hizmeti sunulduğu iddia edilmez. Kişi, contract, payment için yeni servis ancak use-case ve owner gerçekten gerektirirse eklenir.
