# System Design — İki proje kapsam matrisi

Kaynak: [roadmap.sh/system-design](https://roadmap.sh/system-design). Canlı graph snapshot tarihi **2026-10-07**. [Makineyle okunabilir envanter](system-design-roadmap-snapshot.json); [günlük plan](../roadmap/README.md).

## Kapsam ve durum

**27 ana konu + 120 alt konu occurrence'ı + 3 mavi konu = 150 kapsam düğümü.** Gri `roadmap.sh` navigasyon düğümü eğitim konusu değildir. Canlı graph topic/subtopic sınıfını ve mavi button rengini içerir; mor/yeşil tik metadata'sı yoktur. Bu nedenle mor/yeşil tik varmış gibi etiket üretilmez; kullanıcının istediği kapsamı atlamamak için **bütün alt konular** günlük öğrenme/uygulama/runtime test görevine bağlanmıştır. Tekrarlanan etiketler node ID ile ayrı satırdır.

Bütün satırlar şimdilik **Planlandı / runtime evidence yok**. “Programa dahil” ile “öğrenildi/uygulandı” farklıdır. [Zorunlu uygulama sözleşmesi](mandatory-implementation-contract.md) geçerlidir: comparison, dependency veya ADR tek başına zorunlu konuyu kapatmaz.

Emlak 85 günlük programında değişiklik yapılmaz. Araç Day 01–47 korunur; Day 48 Backend/Full Stack ara audit; yeni Day 49–63 System Design deneyleri; Day 64 üç roadmap ara checkpoint; Day 78 dört roadmap ara checkpoint; Day 99 beş roadmap ara checkpoint; Day 117 altı roadmap final audit'idir. Önceki uygulama aynı sorumluluğu kanıtlı karşılıyorsa yeniden kurulmaz. Evidence yoksa araç milestone'ındaki gerçek görev kapanmadan konu Verified olmaz.

## Ana başlıklar

| Ana başlık | Araç görevi | Öğrenme/uygulama sınırı |
|---|---|---|
| Introduction | [Day 49](../roadmap/day-49.md) | Gereksinimden kapasite modeline geç; latency/throughput, performance/scalability ve partition sırasında availability/consistency tercihlerini ayır. |
| Performance vs Scalability | [Day 49](../roadmap/day-49.md) | Gereksinimden kapasite modeline geç; latency/throughput, performance/scalability ve partition sırasında availability/consistency tercihlerini ayır. |
| Latency vs Throughput | [Day 49](../roadmap/day-49.md) | Gereksinimden kapasite modeline geç; latency/throughput, performance/scalability ve partition sırasında availability/consistency tercihlerini ayır. |
| Availability vs Consistency | [Day 49](../roadmap/day-49.md) | Gereksinimden kapasite modeline geç; latency/throughput, performance/scalability ve partition sırasında availability/consistency tercihlerini ayır. |
| Consistency Patterns | [Day 50](../roadmap/day-50.md) | Tutarlılığı işlem ve veri sahibi bazında tanımla; transaction isolation, read-after-write ve replica freshness farklı garantilerdir. |
| Availability Patterns | [Day 51](../roadmap/day-51.md) | Replica, failover, leader seçimi ve fencing farklı sorumluluklardır; tek makine tatbikatı fiziksel HA kanıtı değildir. |
| Background Jobs | [Day 55](../roadmap/day-55.md) | Event/schedule tetiklemesi, görev kuyruğu ve mesaj yayını; async sonuç alma ve işi yöneten supervisor sorumluluklarını uygula. |
| Domain Name System | [Day 52](../roadmap/day-52.md) | DNS çözümleme ile içerik dağıtımını ayır; pull origin fetch ve push önceden içerik dağıtımını yerel edge lab'ında uygula. |
| Content Delivery Networks | [Day 52](../roadmap/day-52.md) | DNS çözümleme ile içerik dağıtımını ayır; pull origin fetch ve push önceden içerik dağıtımını yerel edge lab'ında uygula. |
| Load Balancers | [Day 53](../roadmap/day-53.md) | Reverse proxy rolü ile load balancing işlevini ayır; TCP connection ve HTTP request dağıtımı aynı ölçüm değildir. |
| Application Layer | [Day 59](../roadmap/day-59.md) | Cloud design pattern'lerinin sağlayıcıdan bağımsız rollerini mevcut Spring/Kubernetes sisteminde gerçek istek akışıyla göster. |
| Databases | [Day 57](../roadmap/day-57.md) | Datastore sınıfını sorgu/invariant gereksinimine göre seç; federation, replication ve sharding farklı topolojilerdir. |
| Caching | [Day 54](../roadmap/day-54.md) | Cache-aside, write-through, write-behind ve refresh-ahead hata/tutarlılık sözleşmelerini aynı non-critical read use-case üzerinde karşılaştır. |
| Asynchronism | [Day 55](../roadmap/day-55.md) | Event/schedule tetiklemesi, görev kuyruğu ve mesaj yayını; async sonuç alma ve işi yöneten supervisor sorumluluklarını uygula. |
| Idempotent Operations | [Day 56](../roadmap/day-56.md) | Transport garantileri, framing, API modeli ve business idempotency farklı katmanlardır. |
| Communication | [Day 56](../roadmap/day-56.md) | Transport garantileri, framing, API modeli ve business idempotency farklı katmanlardır. |
| Performance Antipatterns | [Day 58](../roadmap/day-58.md) | Her antipattern için kötü fixture, ölçülen belirti, düzeltme ve correctness regression evidence'ı oluştur. |
| Monitoring | [Day 61](../roadmap/day-61.md) | Retry/circuit/bulkhead/compensation ile ölçüm ve alert'i aynı failure senaryosunda doğrula; health başarıyla domain doğruluğu aynı değildir. |
| Cloud Design Patterns | [Day 59](../roadmap/day-59.md) | Cloud design pattern'lerinin sağlayıcıdan bağımsız rollerini mevcut Spring/Kubernetes sisteminde gerçek istek akışıyla göster. |
| Messaging | [Day 60](../roadmap/day-60.md) | Mesaj sırası, consumer sahipliği, event log ve projection sorumluluklarını birbirine karıştırmadan uygula. |
| Data Management | [Day 60](../roadmap/day-60.md) | Mesaj sırası, consumer sahipliği, event log ve projection sorumluluklarını birbirine karıştırmadan uygula. |
| Design & Implementation | [Day 59](../roadmap/day-59.md) | Cloud design pattern'lerinin sağlayıcıdan bağımsız rollerini mevcut Spring/Kubernetes sisteminde gerçek istek akışıyla göster. |
| Reliability Patterns | [Day 61](../roadmap/day-61.md) | Retry/circuit/bulkhead/compensation ile ölçüm ve alert'i aynı failure senaryosunda doğrula; health başarıyla domain doğruluğu aynı değildir. |
| Availability | [Day 62](../roadmap/day-62.md) | Bağımsız tenant/capacity stamp'i ile aynı veriyi sunabilen geode arasındaki farkı yerel iki kurulumla uygula. |
| High Availability | [Day 62](../roadmap/day-62.md) | Bağımsız tenant/capacity stamp'i ile aynı veriyi sunabilen geode arasındaki farkı yerel iki kurulumla uygula. |
| Resiliency | [Day 61](../roadmap/day-61.md) | Retry/circuit/bulkhead/compensation ile ölçüm ve alert'i aynı failure senaryosunda doğrula; health başarıyla domain doğruluğu aynı değildir. |
| Security | [Day 63](../roadmap/day-63.md) | Federated identity, giriş güvenlik sınırı ve kısıtlı storage erişim anahtarı için least privilege uygulamasını doğrula. |

## Mavi konular

| Konu | En az bir proje uygulaması ve audit |
|---|---|
| Backend | Java/Spring domain, API, persistence ve integration test'leri; Day 64 evidence |
| Software Architect | Gereksinim/capacity, ADR, owner sınırları, pattern/failure deneyleri; Day 49–63 ve Day 64 |
| DevOps | Build, Docker/Kubernetes deploy, GitOps, telemetry ve restore; emlak Day 46–85 veya araç Day 31–36/46; Day 64 |

Bu üç bağlantının konusu uygulanır; başka linked roadmap'in bütün alt dalları kendiliğinden yeni yükümlülük olmaz. Backend/Full Stack/System Design burada ayrı kullanıcı talebiyle kapsamdır. Önceki Node.js backend ve Basic AWS Services istisnaları korunur; ücretli cloud şartı yoktur.

## Eksik deneyler için yeni günlük sahiplik

| Day | Eğitim deneyleri | Doğrulama |
|---|---|---|
| [49](../roadmap/day-49.md) | System Design süreci ve sayısal hedefler | Yük eğrisi ve iki worker sonucu aynı koşullarda tekrar üretilebilir; hızlanma yoksa bottleneck açıkça raporlanır. Partition deneyinde kabul edilen/reddedilen işlemler ve toparlanma gözlenir; SLA sağlandı iddiası yerine ölçülen pencere yazılır. |
| [50](../roadmap/day-50.md) | Weak, eventual ve strong consistency deneyleri | Weak sayaç kaybı yalnız izin verilen non-critical veride görülür. Aynı araca çakışan iki kesinleşmiş booking oluşmaz; stale projection toparlanır; freshness isteyen read stale replica'ya sessiz yönlenmez. |
| [51](../roadmap/day-51.md) | Failover, replication ve leader election | Yeni lider devralır; stale liderin fenced işi kabul edilmez. Promotion sırasında acknowledged veri kaybı/lag ve downtime ölçülür; seçilen asynchronous replication için RPO=0 varsayılmaz. |
| [52](../roadmap/day-52.md) | DNS, pull/push CDN ve static hosting | Pull cold/hot isteklerinde origin hit sayısı değişir; push edge doğru hash'li artifact'ı sunar. TTL/NXDOMAIN ve private response testleri beklenen sonucu verir; rollout sonrası eski/yeni asset davranışı kaydedilir. |
| [53](../roadmap/day-53.md) | L 4/L 7 load balancing ve horizontal scaling | Her algoritmada backend dağılımı gerçek sayımla raporlanır; eşit trafik beklentisinin koşulları yazılır. Unhealthy backend çıkarılır; session ve in-flight istek davranışı, toparlanma ve kaynak bütçesi belgelenir. |
| [54](../roadmap/day-54.md) | Cache katmanları ve yazma stratejileri | Her strateji için success, cache loss, stale read ve invalidation sonucu ayrı ölçülür. Write-behind durable kabulü crash sonrası geri gelir; booking invariant cache kaybında korunur; private response sızmaz. |
| [55](../roadmap/day-55.md) | Background jobs, back pressure ve supervisor | 202 ile kabul edilen işin durum/sonucu restart sonrası bulunur; yetkisiz polling reddedilir. Stalled agent devralınır; duplicate tetik bir logical job üretir; overload sınırsız bellek/sonsuz retry oluşturmaz. |
| [56](../roadmap/day-56.md) | TCP/UDP, RPC ve API iletişim sözleşmeleri | TCP frame sınırları/partial read ve UDP kayıp sırası gözlenir; public port veya dış hedef gerekmez. Retry booking'i çoğaltmaz; farklı payload aynı key ile reddedilir; her API'de yetkisiz/timeout isteği doğru sonlanır. |
| [57](../roadmap/day-57.md) | Datastore modelleri, sharding ve federation | Yanlış shard'a yazı ve cross-owner mutable state oluşmaz; shard outage davranışı belgelenir. Index/view canonical veriden rebuild olur; federation kısmi hata cevabı sözleşmeye uyar; dört datastore sınıfı için runtime evidence vardır. |
| [58](../roadmap/day-58.md) | On performance antipattern'i ölç ve düzelt | On antipattern'in her biri için gözlenebilir önce/sonra ve başarısızlık yolu vardır; iyileşmeyen ölçüm gizlenmez. Düzeltme sonucu booking correctness, API contract ve resource cleanup korunur; tek cold/warm farkı genel speedup diye sunulmaz. |
| [59](../roadmap/day-59.md) | Design ve implementation pattern'leri | Cutover/rollback, legacy mapping ve discovery gerçek çağrılarla doğrulanır. BFF/gateway/config/ambassador hata deneyleri contract'a uyar; consolidation'da resource sınırları ve contention ölçülür. |
| [60](../roadmap/day-60.md) | Data management ve messaging pattern'leri | Aynı ID sırası ve farklı ID parallel işleme gözlenir; duplicate yan etki yaratmaz. Priority starvation önlemi, blob lifecycle ve poison mesaj recovery kanıtlıdır; event log optimistic concurrency ve replay projection'ı doğru üretir. |
| [61](../roadmap/day-61.md) | Reliability, resiliency ve gözlemlenebilirlik | Bulkhead bir dependency hatasını sınırlar; retry budget/circuit recovery ölçülür; compensation tekrarında çift yan etki yoktur. Beş monitoring türü için gerçek sinyal ve test alert'i oluşur/çözülür; probe sonucu domain invariant testiyle birlikte değerlendirilir. |
| [62](../roadmap/day-62.md) | Availability, deployment stamps ve geodes | Bir tenant stamp hatası diğer tenant'ı etkilemez; misrouting testi veri sızıntısını engeller. İki geode read dataset'i converge eder; owner kesintisinde çakışan write kabul edilmez; RPO/RTO ve freshness sınırı ölçülür. |
| [63](../roadmap/day-63.md) | Federated identity, Gatekeeper ve Valet Key | Federation sonunda doğru principal/scope oluşur; yanlış issuer/audience ve yetkisiz edge bypass reddedilir. Valet Key sadece izinli object/action için çalışır; expiry/tamper/size/replay testleri ve cleanup kanıtlıdır. |
| [64](../roadmap/day-64.md) | Üç roadmap ve iki proje final audit | Her zorunlu kapsam satırının implementation/runtime kanıtı vardır ya da explicit gap'tir; gap varken tamamlama iddiası yapılmaz. E 2 E ve restore sonrası domain invariant korunur; deployment, versiyon ve ölçüm tekrar üretilebilir. |

## Düğüm bazında tam eşleştirme

Aşağıdaki Day bağlantısı yalnız genel bir başlık değildir: ilgili günlük dosyada **öğrenme çıktısı, gerçek uygulama görevleri, başarı/hata/recovery ölçütleri ve commit sırası** vardır. Her satır uygulama sırasında implementation SHA ve evidence path ile güncellenir. Aynı pattern'in tekrar düğümleri ortak evidence paylaşabilir.

| Node ID | Canlı sınıf | Roadmap etiketi | Mevcut temel / yeniden kullanım | Araç owner / uygulama ve test | Durum |
|---|---|---|---|---|---|
| `_hYN0gEi9BL24nptEtXWU` | Ana konu (topic) | Introduction | Mevcut temel görevler üzerinde açık System Design deneyi | [Day 49](../roadmap/day-49.md) | Planlandı |
| `idLHBxhvcIqZTqmh_E8Az` | Alt konu (tik metadata yok) | What is System Design? | Mevcut temel görevler üzerinde açık System Design deneyi | [Day 49](../roadmap/day-49.md) | Planlandı |
| `os3Pa6W9SSNEzgmlBbglQ` | Alt konu (tik metadata yok) | How to approach System Design? | Mevcut temel görevler üzerinde açık System Design deneyi | [Day 49](../roadmap/day-49.md) | Planlandı |
| `e_15lymUjFc6VWqzPnKxG` | Ana konu (topic) | Performance vs Scalability | Mevcut temel görevler üzerinde açık System Design deneyi | [Day 49](../roadmap/day-49.md) | Planlandı |
| `O3wAHLnzrkvLWr4afHDdr` | Ana konu (topic) | Latency vs Throughput | Mevcut temel görevler üzerinde açık System Design deneyi | [Day 49](../roadmap/day-49.md) | Planlandı |
| `uJc27BNAuP321HQNbjftn` | Ana konu (topic) | Availability vs Consistency | Mevcut temel görevler üzerinde açık System Design deneyi | [Day 49](../roadmap/day-49.md) | Planlandı |
| `tcGdVQsCEobdV9hgOq3eG` | Alt konu (tik metadata yok) | CAP Theorem | Mevcut temel görevler üzerinde açık System Design deneyi | [Day 49](../roadmap/day-49.md) | Planlandı |
| `GHe8V-REu1loRpDnHbyUn` | Ana konu (topic) | Consistency Patterns | Mevcut temel görevler üzerinde açık System Design deneyi | [Day 50](../roadmap/day-50.md) | Planlandı |
| `EKD5AikZtwjtsEYRPJhQ2` | Alt konu (tik metadata yok) | Weak Consistency | Mevcut temel görevler üzerinde açık System Design deneyi | [Day 50](../roadmap/day-50.md) | Planlandı |
| `rRDGVynX43inSeQ9lR_FS` | Alt konu (tik metadata yok) | Eventual Consistency | Mevcut temel görevler üzerinde açık System Design deneyi | [Day 50](../roadmap/day-50.md) | Planlandı |
| `JjB7eB8gdRCAYf5M0RcT7` | Alt konu (tik metadata yok) | Strong Consistency | Mevcut temel görevler üzerinde açık System Design deneyi | [Day 50](../roadmap/day-50.md) | Planlandı |
| `ezptoTqeaepByegxS5kHL` | Ana konu (topic) | Availability Patterns | Mevcut temel görevler üzerinde açık System Design deneyi | [Day 51](../roadmap/day-51.md) | Planlandı |
| `L_jRfjvMGjFbHEbozeVQl` | Alt konu (tik metadata yok) | Fail-Over | Mevcut temel görevler üzerinde açık System Design deneyi | [Day 51](../roadmap/day-51.md) | Planlandı |
| `0RQ5jzZKdadYY0h_QZ0Bb` | Alt konu (tik metadata yok) | Replication | Araç Day 11/37; açık deney genişletmesi | [Day 51](../roadmap/day-51.md) | Planlandı |
| `uHdrZllrZFAnVkwIB3y5-` | Alt konu (tik metadata yok) | Availability in Numbers | Mevcut temel görevler üzerinde açık System Design deneyi | [Day 49](../roadmap/day-49.md) | Planlandı |
| `DOESIlBThd_wp2uOSd_CS` | Ana konu (topic) | Background Jobs | Mevcut temel görevler üzerinde açık System Design deneyi | [Day 55](../roadmap/day-55.md) | Planlandı |
| `NEsPjQifNDlZJE-2YLVl1` | Alt konu (tik metadata yok) | Event-Driven | Mevcut temel görevler üzerinde açık System Design deneyi | [Day 55](../roadmap/day-55.md) | Planlandı |
| `zoViI4kzpKIxpU20T89K_` | Alt konu (tik metadata yok) | Schedule Driven | Mevcut temel görevler üzerinde açık System Design deneyi | [Day 55](../roadmap/day-55.md) | Planlandı |
| `2gRIstNT-fTkv5GZ692gx` | Alt konu (tik metadata yok) | Returning Results | Mevcut temel görevler üzerinde açık System Design deneyi | [Day 55](../roadmap/day-55.md) | Planlandı |
| `Uk6J8JRcKVEFz4_8rLfnQ` | Ana konu (topic) | Domain Name System | Mevcut temel görevler üzerinde açık System Design deneyi | [Day 52](../roadmap/day-52.md) | Planlandı |
| `O730v5Ww3ByAiBSs6fwyM` | Ana konu (topic) | Content Delivery Networks | Mevcut temel görevler üzerinde açık System Design deneyi | [Day 52](../roadmap/day-52.md) | Planlandı |
| `uIerrf_oziiLg-KEyz8WM` | Alt konu (tik metadata yok) | Push CDNs | Mevcut temel görevler üzerinde açık System Design deneyi | [Day 52](../roadmap/day-52.md) | Planlandı |
| `HkXiEMLqxJoQyAHav3ccL` | Alt konu (tik metadata yok) | Pull CDNs | Mevcut temel görevler üzerinde açık System Design deneyi | [Day 52](../roadmap/day-52.md) | Planlandı |
| `14KqLKgh090Rb3MDwelWY` | Ana konu (topic) | Load Balancers | Mevcut temel görevler üzerinde açık System Design deneyi | [Day 53](../roadmap/day-53.md) | Planlandı |
| `ocdcbhHrwjJX0KWgmsOL6` | Alt konu (tik metadata yok) | LB vs Reverse Proxy | Mevcut temel görevler üzerinde açık System Design deneyi | [Day 53](../roadmap/day-53.md) | Planlandı |
| `urSjLyLTE5IIz0TFxMBWL` | Alt konu (tik metadata yok) | Load Balancing Algorithms | Mevcut temel görevler üzerinde açık System Design deneyi | [Day 53](../roadmap/day-53.md) | Planlandı |
| `e69-JVbDj7dqV_p1j1kML` | Alt konu (tik metadata yok) | Layer 7 Load Balancing | Mevcut temel görevler üzerinde açık System Design deneyi | [Day 53](../roadmap/day-53.md) | Planlandı |
| `MpM9rT1-_LGD7YbnBjqOk` | Alt konu (tik metadata yok) | Layer 4 Load Balancing | Mevcut temel görevler üzerinde açık System Design deneyi | [Day 53](../roadmap/day-53.md) | Planlandı |
| `IkUCfSWNY-02wg2WCo1c6` | Alt konu (tik metadata yok) | Horizontal Scaling | Mevcut temel görevler üzerinde açık System Design deneyi | [Day 53](../roadmap/day-53.md) | Planlandı |
| `XXuzTrP5UNVwSpAk-tAGr` | Ana konu (topic) | Application Layer | Mevcut temel görevler üzerinde açık System Design deneyi | [Day 59](../roadmap/day-59.md) | Planlandı |
| `UKTiaHCzYXnrNw31lHriv` | Alt konu (tik metadata yok) | Microservices | Araç Day 12–13 | [Day 59](../roadmap/day-59.md) | Planlandı |
| `Nt0HUWLOl4O77elF8Is1S` | Alt konu (tik metadata yok) | Service Discovery | Araç Day 12–13 | [Day 59](../roadmap/day-59.md) | Planlandı |
| `5FXwwRMNBhG7LT5ub6t2L` | Ana konu (topic) | Databases | Mevcut temel görevler üzerinde açık System Design deneyi | [Day 57](../roadmap/day-57.md) | Planlandı |
| `KLnpMR2FxlQkCHZP6-tZm` | Alt konu (tik metadata yok) | SQL vs NoSQL | Mevcut temel görevler üzerinde açık System Design deneyi | [Day 57](../roadmap/day-57.md) | Planlandı |
| `dc-aIbBwUdlwgwQKGrq49` | Alt konu (tik metadata yok) | Replication | Araç Day 11/37; açık deney genişletmesi | [Day 51](../roadmap/day-51.md) | Planlandı |
| `FX6dcV_93zOfbZMdM_-li` | Alt konu (tik metadata yok) | Sharding | Mevcut temel görevler üzerinde açık System Design deneyi | [Day 57](../roadmap/day-57.md) | Planlandı |
| `DGmVRI7oWdSOeIUn_g0rI` | Alt konu (tik metadata yok) | Federation | Mevcut temel görevler üzerinde açık System Design deneyi | [Day 57](../roadmap/day-57.md) | Planlandı |
| `Zp9D4--DgtlAjE2nIfaO_` | Alt konu (tik metadata yok) | Denormalization | Araç Day 11/37; açık deney genişletmesi | [Day 57](../roadmap/day-57.md) | Planlandı |
| `fY8zgbB13wxZ1CFtMSdZZ` | Alt konu (tik metadata yok) | SQL Tuning | Araç Day 11/37; açık deney genişletmesi | [Day 57](../roadmap/day-57.md) | Planlandı |
| `KFtdmmce4bRkDyvFXZzLN` | Alt konu (tik metadata yok) | Key-Value Store | Emlak Redis Day 13; araç Memcached Day 15 | [Day 57](../roadmap/day-57.md) | Planlandı |
| `didEznSlVHqqlijtyOSr3` | Alt konu (tik metadata yok) | Document Store | Emlak MongoDB Day 11; araç CouchDB Day 22 | [Day 57](../roadmap/day-57.md) | Planlandı |
| `WHq1AdISkcgthaugE9uY7` | Alt konu (tik metadata yok) | Wide Column Store | Emlak Cassandra Day 10/20; evidence yoksa araç Day 57 fixture | [Day 57](../roadmap/day-57.md) | Planlandı |
| `6RLgnL8qLBzYkllHeaI-Z` | Alt konu (tik metadata yok) | Graph Databases | Araç Neo 4 j Day 19 | [Day 57](../roadmap/day-57.md) | Planlandı |
| `-X4g8kljgVBOBcf1DDzgi` | Ana konu (topic) | Caching | Emlak Redis Day 13; araç HTTP/Memcached Day 15 | [Day 54](../roadmap/day-54.md) | Planlandı |
| `Bgqgl67FK56ioLNFivIsc` | Alt konu (tik metadata yok) | Refresh Ahead | Mevcut temel görevler üzerinde açık System Design deneyi | [Day 54](../roadmap/day-54.md) | Planlandı |
| `vNndJ-MWetcbaF2d-3-JP` | Alt konu (tik metadata yok) | Write-behind | Mevcut temel görevler üzerinde açık System Design deneyi | [Day 54](../roadmap/day-54.md) | Planlandı |
| `RNITLR1FUQWkRbSBXTD_z` | Alt konu (tik metadata yok) | Write-through | Mevcut temel görevler üzerinde açık System Design deneyi | [Day 54](../roadmap/day-54.md) | Planlandı |
| `bffJlvoLHFldS0CluWifP` | Alt konu (tik metadata yok) | Cache Aside | Emlak Redis Day 13; araç HTTP/Memcached Day 15 | [Day 54](../roadmap/day-54.md) | Planlandı |
| `RHNRb6QWiGvCK3KQOPK3u` | Alt konu (tik metadata yok) | Client Caching | Emlak Redis Day 13; araç HTTP/Memcached Day 15 | [Day 54](../roadmap/day-54.md) | Planlandı |
| `Kisvxlrjb7XnKFCOdxRtb` | Alt konu (tik metadata yok) | CDN Caching | Mevcut temel görevler üzerinde açık System Design deneyi | [Day 52](../roadmap/day-52.md) | Planlandı |
| `o532nPnL-d2vXJn9k6vMl` | Alt konu (tik metadata yok) | Web Server Caching | Emlak Redis Day 13; araç HTTP/Memcached Day 15 | [Day 54](../roadmap/day-54.md) | Planlandı |
| `BeIg4jzbij2cwc_a_VpYG` | Alt konu (tik metadata yok) | Database Caching | Mevcut temel görevler üzerinde açık System Design deneyi | [Day 54](../roadmap/day-54.md) | Planlandı |
| `5Ux_JBDOkflCaIm4tVBgO` | Alt konu (tik metadata yok) | Application Caching | Emlak Redis Day 13; araç HTTP/Memcached Day 15 | [Day 54](../roadmap/day-54.md) | Planlandı |
| `84N4XY31PwXRntXX1sdCU` | Ana konu (topic) | Asynchronism | Mevcut temel görevler üzerinde açık System Design deneyi | [Day 55](../roadmap/day-55.md) | Planlandı |
| `YiYRZFE_zwPMiCZxz9FnP` | Alt konu (tik metadata yok) | Back Pressure | Mevcut temel görevler üzerinde açık System Design deneyi | [Day 55](../roadmap/day-55.md) | Planlandı |
| `a9wGW_H1HpvvdYCXoS-Rf` | Alt konu (tik metadata yok) | Task Queues | Mevcut temel görevler üzerinde açık System Design deneyi | [Day 55](../roadmap/day-55.md) | Planlandı |
| `37X1_9eCmkZkz5RDudE5N` | Alt konu (tik metadata yok) | Message Queues | Mevcut temel görevler üzerinde açık System Design deneyi | [Day 55](../roadmap/day-55.md) | Planlandı |
| `3pRi8M4xQXsehkdfUNtYL` | Ana konu (topic) | Idempotent Operations | Mevcut temel görevler üzerinde açık System Design deneyi | [Day 56](../roadmap/day-56.md) | Planlandı |
| `uQFzD_ryd-8Dr1ppjorYJ` | Ana konu (topic) | Communication | Mevcut temel görevler üzerinde açık System Design deneyi | [Day 56](../roadmap/day-56.md) | Planlandı |
| `I_nR6EwjNXSG7_hw-_VhX` | Alt konu (tik metadata yok) | HTTP | Emlak/araç mevcut API planları; transport deneyi ek | [Day 56](../roadmap/day-56.md) | Planlandı |
| `2nF5uC6fYKbf0RFgGNHiP` | Alt konu (tik metadata yok) | TCP | Mevcut temel görevler üzerinde açık System Design deneyi | [Day 56](../roadmap/day-56.md) | Planlandı |
| `LC5aTmUKNiw9RuSUt3fSE` | Alt konu (tik metadata yok) | UDP | Mevcut temel görevler üzerinde açık System Design deneyi | [Day 56](../roadmap/day-56.md) | Planlandı |
| `ixqucoAkgnphWYAFnsMe-` | Alt konu (tik metadata yok) | RPC | Emlak/araç mevcut API planları; transport deneyi ek | [Day 56](../roadmap/day-56.md) | Planlandı |
| `6-bgmfDTAQ9zABhpmVoHV` | Alt konu (tik metadata yok) | REST | Emlak/araç mevcut API planları; transport deneyi ek | [Day 56](../roadmap/day-56.md) | Planlandı |
| `Hw2v1rCYn24qxBhhmdc28` | Alt konu (tik metadata yok) | gRPC | Emlak/araç mevcut API planları; transport deneyi ek | [Day 56](../roadmap/day-56.md) | Planlandı |
| `jwv2g2Yeq-6Xv5zSd746R` | Alt konu (tik metadata yok) | GraphQL | Emlak/araç mevcut API planları; transport deneyi ek | [Day 56](../roadmap/day-56.md) | Planlandı |
| `p--uEm6klLx_hKxKJiXE5` | Ana konu (topic) | Performance Antipatterns | Mevcut temel görevler üzerinde açık System Design deneyi | [Day 58](../roadmap/day-58.md) | Planlandı |
| `hxiV2uF7tvhZKe4K-4fTn` | Alt konu (tik metadata yok) | Busy Database | Mevcut temel görevler üzerinde açık System Design deneyi | [Day 58](../roadmap/day-58.md) | Planlandı |
| `i_2M3VloG-xTgWDWp4ngt` | Alt konu (tik metadata yok) | Busy Frontend | Mevcut temel görevler üzerinde açık System Design deneyi | [Day 58](../roadmap/day-58.md) | Planlandı |
| `0IzQwuYi_E00bJwxDuw2B` | Alt konu (tik metadata yok) | Chatty I/O | Mevcut temel görevler üzerinde açık System Design deneyi | [Day 58](../roadmap/day-58.md) | Planlandı |
| `6u3XmtJFWyJnyZUnJcGYb` | Alt konu (tik metadata yok) | Extraneous Fetching | Mevcut temel görevler üzerinde açık System Design deneyi | [Day 58](../roadmap/day-58.md) | Planlandı |
| `lwMs4yiUHF3nQwcvauers` | Alt konu (tik metadata yok) | Improper Instantiation | Mevcut temel görevler üzerinde açık System Design deneyi | [Day 58](../roadmap/day-58.md) | Planlandı |
| `p1QhCptnwzTGUXVMnz_Oz` | Alt konu (tik metadata yok) | Monolithic Persistence | Mevcut temel görevler üzerinde açık System Design deneyi | [Day 58](../roadmap/day-58.md) | Planlandı |
| `klvHk1_e03Jarn5T46QNi` | Alt konu (tik metadata yok) | No Caching | Mevcut temel görevler üzerinde açık System Design deneyi | [Day 58](../roadmap/day-58.md) | Planlandı |
| `r7uQxmurvfsYtTCieHqly` | Alt konu (tik metadata yok) | Noisy Neighbor | Mevcut temel görevler üzerinde açık System Design deneyi | [Day 58](../roadmap/day-58.md) | Planlandı |
| `LNmAJmh2ndFtOQIpvX_ga` | Alt konu (tik metadata yok) | Retry Storm | Mevcut temel görevler üzerinde açık System Design deneyi | [Day 58](../roadmap/day-58.md) | Planlandı |
| `Ihnmxo_bVgZABDwg1QGGk` | Alt konu (tik metadata yok) | Synchronous I/O | Mevcut temel görevler üzerinde açık System Design deneyi | [Day 58](../roadmap/day-58.md) | Planlandı |
| `hDFYlGFYwcwWXLmrxodFX` | Ana konu (topic) | Monitoring | Emlak DevOps kapsamı; araç Day 36/46 | [Day 61](../roadmap/day-61.md) | Planlandı |
| `hkjYvLoVt9xKDzubm0Jy3` | Alt konu (tik metadata yok) | Health Monitoring | Mevcut temel görevler üzerinde açık System Design deneyi | [Day 61](../roadmap/day-61.md) | Planlandı |
| `rVrwaioGURvrqNBufF2dj` | Alt konu (tik metadata yok) | Availability Monitoring | Mevcut temel görevler üzerinde açık System Design deneyi | [Day 61](../roadmap/day-61.md) | Planlandı |
| `x1i3qWFtNNjd00-kAvFHw` | Alt konu (tik metadata yok) | Performance Monitoring | Mevcut temel görevler üzerinde açık System Design deneyi | [Day 61](../roadmap/day-61.md) | Planlandı |
| `I_NfmDcBph8-oyFVFTknL` | Alt konu (tik metadata yok) | Security Monitoring | Mevcut temel görevler üzerinde açık System Design deneyi | [Day 61](../roadmap/day-61.md) | Planlandı |
| `eSZq74lROh5lllLyTBK5a` | Alt konu (tik metadata yok) | Usage Monitoring | Mevcut temel görevler üzerinde açık System Design deneyi | [Day 61](../roadmap/day-61.md) | Planlandı |
| `Q0fKphqmPwjTD0dhqiP6K` | Alt konu (tik metadata yok) | Instrumentation | Emlak DevOps kapsamı; araç Day 36/46 | [Day 61](../roadmap/day-61.md) | Planlandı |
| `IwMOTpsYHApdvHZOhXtIw` | Alt konu (tik metadata yok) | Visualization & Alerts | Emlak DevOps kapsamı; araç Day 36/46 | [Day 61](../roadmap/day-61.md) | Planlandı |
| `THlzcZTNnPGLRiHPWT-Jv` | Ana konu (topic) | Cloud Design Patterns | Mevcut temel görevler üzerinde açık System Design deneyi | [Day 59](../roadmap/day-59.md) | Planlandı |
| `dsWpta3WIBvv2K9pNVPo0` | Ana konu (topic) | Messaging | Mevcut temel görevler üzerinde açık System Design deneyi | [Day 60](../roadmap/day-60.md) | Planlandı |
| `VgvUWAC6JYFyPZKBRoEqf` | Alt konu (tik metadata yok) | Sequential Convoy | Mevcut temel görevler üzerinde açık System Design deneyi | [Day 60](../roadmap/day-60.md) | Planlandı |
| `uR1fU6pm7zTtdBcNgSRi4` | Alt konu (tik metadata yok) | Scheduling Agent Supervisor | Mevcut temel görevler üzerinde açık System Design deneyi | [Day 55](../roadmap/day-55.md) | Planlandı |
| `LncTxPg-wx8loy55r5NmV` | Alt konu (tik metadata yok) | Queue-Based Load Leveling | Mevcut temel görevler üzerinde açık System Design deneyi | [Day 60](../roadmap/day-60.md) | Planlandı |
| `2ryzJhRDTo98gGgn9mAxR` | Alt konu (tik metadata yok) | Publisher/Subscriber | Mevcut temel görevler üzerinde açık System Design deneyi | [Day 60](../roadmap/day-60.md) | Planlandı |
| `DZcZEOi7h3u0744YhASet` | Alt konu (tik metadata yok) | Priority Queue | Mevcut temel görevler üzerinde açık System Design deneyi | [Day 60](../roadmap/day-60.md) | Planlandı |
| `siXdR3TB9-4wx_qWieJ5w` | Alt konu (tik metadata yok) | Pipes and Filters | Mevcut temel görevler üzerinde açık System Design deneyi | [Day 60](../roadmap/day-60.md) | Planlandı |
| `9Ld07KLOqP0ICtXEjngYM` | Alt konu (tik metadata yok) | Competing Consumers | Mevcut temel görevler üzerinde açık System Design deneyi | [Day 60](../roadmap/day-60.md) | Planlandı |
| `aCzRgUkVBvtHUeLU6p5ZH` | Alt konu (tik metadata yok) | Choreography | Mevcut temel görevler üzerinde açık System Design deneyi | [Day 60](../roadmap/day-60.md) | Planlandı |
| `kl4upCnnZvJSf2uII1Pa0` | Alt konu (tik metadata yok) | Claim Check | Mevcut temel görevler üzerinde açık System Design deneyi | [Day 60](../roadmap/day-60.md) | Planlandı |
| `eNFNXPsFiryVxFe4unVxk` | Alt konu (tik metadata yok) | Async Request Reply | Mevcut temel görevler üzerinde açık System Design deneyi | [Day 55](../roadmap/day-55.md) | Planlandı |
| `W0cUCrhiwH_Nrzxw50x3L` | Ana konu (topic) | Data Management | Mevcut temel görevler üzerinde açık System Design deneyi | [Day 60](../roadmap/day-60.md) | Planlandı |
| `stZOcr8EUBOK_ZB48uToj` | Alt konu (tik metadata yok) | Valet Key | Mevcut temel görevler üzerinde açık System Design deneyi | [Day 63](../roadmap/day-63.md) | Planlandı |
| `-lKq-LT7EPK7r3xbXLgwS` | Alt konu (tik metadata yok) | Static Content Hosting | Mevcut temel görevler üzerinde açık System Design deneyi | [Day 52](../roadmap/day-52.md) | Planlandı |
| `R6YehzA3X6DDo6oGBoBAx` | Alt konu (tik metadata yok) | Sharding | Mevcut temel görevler üzerinde açık System Design deneyi | [Day 57](../roadmap/day-57.md) | Planlandı |
| `WB7vQ4IJ0TPh2MbZvxP6V` | Alt konu (tik metadata yok) | Materialized View | Mevcut temel görevler üzerinde açık System Design deneyi | [Day 57](../roadmap/day-57.md) | Planlandı |
| `AH0nVeVsfYOjcI3vZvcdz` | Alt konu (tik metadata yok) | Index Table | Mevcut temel görevler üzerinde açık System Design deneyi | [Day 57](../roadmap/day-57.md) | Planlandı |
| `7OgRKlwFqrk3XO2z49EI1` | Alt konu (tik metadata yok) | Event Sourcing | Emlak Day 21/35–36; araç Day 24; evidence gap'inde Day 60 | [Day 60](../roadmap/day-60.md) | Planlandı |
| `LTD3dn05c0ruUJW0IQO7z` | Alt konu (tik metadata yok) | CQRS | Emlak Day 21/35–36; araç Day 24; evidence gap'inde Day 60 | [Day 60](../roadmap/day-60.md) | Planlandı |
| `PK4V9OWNVi8StdA2N13X2` | Alt konu (tik metadata yok) | Cache-Aside | Emlak Redis Day 13; araç HTTP/Memcached Day 15 | [Day 54](../roadmap/day-54.md) | Planlandı |
| `PtJ7-v1VCLsyaWWYHYujV` | Ana konu (topic) | Design & Implementation | Mevcut temel görevler üzerinde açık System Design deneyi | [Day 59](../roadmap/day-59.md) | Planlandı |
| `VIbXf7Jh9PbQ9L-g6pHUG` | Alt konu (tik metadata yok) | Strangler Fig | Emlak Day 34; araç Day 12 | [Day 59](../roadmap/day-59.md) | Planlandı |
| `izPT8NfJy1JC6h3i7GJYl` | Alt konu (tik metadata yok) | Static Content Hosting | Mevcut temel görevler üzerinde açık System Design deneyi | [Day 52](../roadmap/day-52.md) | Planlandı |
| `AAgOGrra5Yz3_eG6tD2Fx` | Alt konu (tik metadata yok) | Sidecar | Araç Linkerd Day 36 | [Day 59](../roadmap/day-59.md) | Planlandı |
| `WkoFezOXLf1H2XI9AtBtv` | Alt konu (tik metadata yok) | Pipes & Filters | Mevcut temel görevler üzerinde açık System Design deneyi | [Day 60](../roadmap/day-60.md) | Planlandı |
| `beWKUIB6Za27yhxQwEYe3` | Alt konu (tik metadata yok) | Leader Election | Mevcut temel görevler üzerinde açık System Design deneyi | [Day 51](../roadmap/day-51.md) | Planlandı |
| `LXH_mDlILqcyIKtMYTWqy` | Alt konu (tik metadata yok) | Gateway Routing | Mevcut temel görevler üzerinde açık System Design deneyi | [Day 59](../roadmap/day-59.md) | Planlandı |
| `0SOWAA8hrLM-WsG5k66fd` | Alt konu (tik metadata yok) | Gateway Offloading | Mevcut temel görevler üzerinde açık System Design deneyi | [Day 59](../roadmap/day-59.md) | Planlandı |
| `bANGLm_5zR9mqMd6Oox8s` | Alt konu (tik metadata yok) | Gateway Aggregation | Mevcut temel görevler üzerinde açık System Design deneyi | [Day 59](../roadmap/day-59.md) | Planlandı |
| `BrgXwf7g2F-6Rqfjryvpj` | Alt konu (tik metadata yok) | External Config Store | Mevcut temel görevler üzerinde açık System Design deneyi | [Day 59](../roadmap/day-59.md) | Planlandı |
| `ODjVoXnvJasPvCS2A5iMO` | Alt konu (tik metadata yok) | Compute Resource Consolidation | Mevcut temel görevler üzerinde açık System Design deneyi | [Day 59](../roadmap/day-59.md) | Planlandı |
| `ivr3mh0OES5n86FI1PN4N` | Alt konu (tik metadata yok) | CQRS | Emlak Day 21/35–36; araç Day 24; evidence gap'inde Day 60 | [Day 60](../roadmap/day-60.md) | Planlandı |
| `n4It-lr7FFtSY83DcGydX` | Alt konu (tik metadata yok) | Backends for Frontend | Mevcut temel görevler üzerinde açık System Design deneyi | [Day 59](../roadmap/day-59.md) | Planlandı |
| `4hi7LvjLcv8eR6m-uk8XQ` | Alt konu (tik metadata yok) | Anti-Corruption Layer | Emlak Day 34; araç SOA Day 27 | [Day 59](../roadmap/day-59.md) | Planlandı |
| `Hja4YF3JcgM6CPwB1mxmo` | Alt konu (tik metadata yok) | Ambassador | Mevcut temel görevler üzerinde açık System Design deneyi | [Day 59](../roadmap/day-59.md) | Planlandı |
| `DYkdM_L7T2GcTPAoZNnUR` | Ana konu (topic) | Reliability Patterns | Mevcut temel görevler üzerinde açık System Design deneyi | [Day 61](../roadmap/day-61.md) | Planlandı |
| `Xzkvf4naveszLGV9b-8ih` | Ana konu (topic) | Availability | Mevcut temel görevler üzerinde açık System Design deneyi | [Day 62](../roadmap/day-62.md) | Planlandı |
| `FPPJw-I1cw8OxKwmDh0dT` | Alt konu (tik metadata yok) | Deployment Stamps | Mevcut temel görevler üzerinde açık System Design deneyi | [Day 62](../roadmap/day-62.md) | Planlandı |
| `Ml9lPDGjRAJTHkBnX51Un` | Alt konu (tik metadata yok) | Geodes | Mevcut temel görevler üzerinde açık System Design deneyi | [Day 62](../roadmap/day-62.md) | Planlandı |
| `cNJQoMNZmxNygWAJIA8HI` | Alt konu (tik metadata yok) | Health Endpoint Monitoring | Mevcut temel görevler üzerinde açık System Design deneyi | [Day 61](../roadmap/day-61.md) | Planlandı |
| `-M3Zd8w79sKBAY6_aJRE8` | Alt konu (tik metadata yok) | Queue-Based Load Leveling | Mevcut temel görevler üzerinde açık System Design deneyi | [Day 60](../roadmap/day-60.md) | Planlandı |
| `6YVkguDOtwveyeP4Z1NL3` | Alt konu (tik metadata yok) | Throttling | Mevcut temel görevler üzerinde açık System Design deneyi | [Day 61](../roadmap/day-61.md) | Planlandı |
| `wPe7Xlwqws7tEpTAVvYjr` | Ana konu (topic) | High Availability | Mevcut temel görevler üzerinde açık System Design deneyi | [Day 62](../roadmap/day-62.md) | Planlandı |
| `Ze471tPbAwlwZyU4oIzH9` | Alt konu (tik metadata yok) | Deployment Stamps | Mevcut temel görevler üzerinde açık System Design deneyi | [Day 62](../roadmap/day-62.md) | Planlandı |
| `6hOSEZJZ7yezVN67h5gmS` | Alt konu (tik metadata yok) | Geodes | Mevcut temel görevler üzerinde açık System Design deneyi | [Day 62](../roadmap/day-62.md) | Planlandı |
| `uK5o7NgDvr2pV0ulF0Fh9` | Alt konu (tik metadata yok) | Health Endpoint Monitoring | Mevcut temel görevler üzerinde açık System Design deneyi | [Day 61](../roadmap/day-61.md) | Planlandı |
| `IR2_kgs2U9rnAJiDBmpqK` | Alt konu (tik metadata yok) | Bulkhead | Mevcut temel görevler üzerinde açık System Design deneyi | [Day 61](../roadmap/day-61.md) | Planlandı |
| `D1OmCoqvd3-_af3u0ciHr` | Alt konu (tik metadata yok) | Circuit Breaker | Mevcut temel görevler üzerinde açık System Design deneyi | [Day 61](../roadmap/day-61.md) | Planlandı |
| `wlAWMjxZF6yav3ZXOScxH` | Ana konu (topic) | Resiliency | Mevcut temel görevler üzerinde açık System Design deneyi | [Day 61](../roadmap/day-61.md) | Planlandı |
| `PLn9TF9GYnPcbpTdDMQbG` | Alt konu (tik metadata yok) | Bulkhead | Mevcut temel görevler üzerinde açık System Design deneyi | [Day 61](../roadmap/day-61.md) | Planlandı |
| `O4zYDqvVWD7sMI27k_0Nl` | Alt konu (tik metadata yok) | Circuit Breaker | Mevcut temel görevler üzerinde açık System Design deneyi | [Day 61](../roadmap/day-61.md) | Planlandı |
| `MNlWNjrG8eh5OzPVlbb9t` | Alt konu (tik metadata yok) | Compensating Transaction | Mevcut temel görevler üzerinde açık System Design deneyi | [Day 61](../roadmap/day-61.md) | Planlandı |
| `CKCNk3obx4u43rBqUj2Yf` | Alt konu (tik metadata yok) | Health Endpoint Monitoring | Mevcut temel görevler üzerinde açık System Design deneyi | [Day 61](../roadmap/day-61.md) | Planlandı |
| `AJLBFyAsEdQYF6ygO0MmQ` | Alt konu (tik metadata yok) | Leader Election | Mevcut temel görevler üzerinde açık System Design deneyi | [Day 51](../roadmap/day-51.md) | Planlandı |
| `NybkOwl1lgaglZPRJQJ_Z` | Alt konu (tik metadata yok) | Queue-Based Load Leveling | Mevcut temel görevler üzerinde açık System Design deneyi | [Day 60](../roadmap/day-60.md) | Planlandı |
| `xX_9VGUaOkBYFH3jPjnww` | Alt konu (tik metadata yok) | Retry | Mevcut temel görevler üzerinde açık System Design deneyi | [Day 61](../roadmap/day-61.md) | Planlandı |
| `RTEJHZ26znfBLrpQPtNvn` | Alt konu (tik metadata yok) | Scheduler Agent Supervisor | Mevcut temel görevler üzerinde açık System Design deneyi | [Day 55](../roadmap/day-55.md) | Planlandı |
| `ZvYpE6-N5dAtRDIwqcAu6` | Ana konu (topic) | Security | Araç Day 14/16–18/38 | [Day 63](../roadmap/day-63.md) | Planlandı |
| `lHPl-kr1ArblR7bJeQEB9` | Alt konu (tik metadata yok) | Federated Identity | Araç Day 14/16–18/38 | [Day 63](../roadmap/day-63.md) | Planlandı |
| `DTQJu0AvgWOhMFcOYqzTD` | Alt konu (tik metadata yok) | Gatekeeper | Mevcut temel görevler üzerinde açık System Design deneyi | [Day 63](../roadmap/day-63.md) | Planlandı |
| `VltZgIrApHOwZ8YHvdmHB` | Alt konu (tik metadata yok) | Valet Key | Mevcut temel görevler üzerinde açık System Design deneyi | [Day 63](../roadmap/day-63.md) | Planlandı |
| `OIcmPSbdsuWapb6HZ4BEi` | Mavi bağlantı | Backend | Emlak backend + araç Day 07–29 | [Day 64](../roadmap/day-64.md) | Planlandı |
| `CH_K6mmFX_GdSzi2n1ID7` | Mavi bağlantı | Software Architect | İki projede architecture; araç Day 49–63 | [Day 64](../roadmap/day-64.md) | Planlandı |
| `-sFboM4eFUMVq1tlPl-fV` | Mavi bağlantı | DevOps | Emlak Day 46–85; araç Day 31–36/46 | [Day 64](../roadmap/day-64.md) | Planlandı |

## Ürün seçimi ve yerel sınırlar

- Önceki Java/Spring Boot/Spring Cloud/Docker/Kubernetes ekseni, canonical veri sahipliği ve seçilmiş alternatifler korunur. Aynı capability için yalnız ürün çeşitliliği amacıyla competing owner/controller kurulmaz.
- Emlak Cassandra wide-column, MongoDB document, Redis key-value ve Event Sourcing/CQRS planları evidence ile karşılanır. Evidence eksikse araç Day 57/60'taki conditional gerçek implementation görevi çalıştırılır; comparison ile kapanmaz.
- CoreDNS yerel DNS deneyi; HAProxy izole L 4; mevcut Nginx L 7/edge/static içerik deneyidir. Bunlar farklı responsibility profilleridir. Güncel compatibility/license uygulama sırasında kontrol edilir.
- Cloud design pattern isimleri Azure/AWS/GCP hesabı veya ücretli ürün zorunluluğu değildir. Geodes/stamps iki local kurulum; CDN yerel origin/edge; leader seçim local Lease + durable fencing deneyidir. Aynı host/cluster, bağımsız coğrafi/fiziksel fault domain değildir.
- Geode lab'ı shared read dataset ve tek canonical write owner kullanır; multi-region active-active güçlü tutarlı write veya production SLA/scale doğrulanmış sayılmaz.
- Yeşil alternatif ürünler varsa requirement'a göre seçilir; Backend matrisindeki seçilmiş MariaDB/Memcached/Solr/SQLite/TimescaleDB/CouchDB uygulama görevleri korunur. Bu System Design snapshot'ında olmayan yeşil tik listesi uydurulmaz.

## Final gate

Day 64 ara checkpoint ve Day 78 final audit'te 150 düğümün her biri öğrenme notu, owner, implementation commit, runtime başarı/hata/toparlanma evidence ve local sınırı ile denetlenir. Requirement/capacity değerlendirmesi gibi kavramlar gerçek proje ölçümü/deneyiyle doğrulanır; sırf kod satırı yazmak her kavramın öğrenildiğini göstermez. Açık gap varken bütün kapsam tamamlandı denmez.


## DevOps genişletmesi sonrası final sahiplik

System Design günlük görevleri/150 eşleştirme korunur. [DevOps kapsamı](devops-coverage.md) eklenince Day 64 üç roadmap ara checkpoint olarak kalır; dört roadmap'in nihai audit'i Day 78'dir. DevOps paid/provider istisnaları ayrı raporlanır.


## Frontend genişletmesi sonrası nihai audit

[Frontend kapsamı](frontend-coverage.md) ayrıca kullanıcı talebiyle eklendi. Day 78 önceki dört roadmap için ara checkpoint olarak korunur; **Day 99** Backend/Full Stack/System Design/DevOps/Frontend final audit'idir. Önceki ürün görevleri ve cloud/SaaS erişim sınırları değişmez. Desktop/Mobile frontend branch'leri kapsam dışıdır; Node business backend hariç kalırken yalnız yeni frontend SSR render role'ü uygulanır.


## Software Architect fazı sonrası nihai audit

[Software Architect kapsamı](software-architect-coverage.md) explicit kullanıcı talebiyle eklendi. Day 99 önceki beş roadmap ara checkpoint; **Day 117** Backend/Full Stack/System Design/DevOps/Frontend/Software Architect final audit'idir. Önceki actual ürün görevleri ve erişim/istisna sınırları korunur; case validation ile teknik runtime evidence ayrı raporlanır.


## Yeni explicit kapsam ve final gün güncellemesi — 2026-10-08

[Software Design & Architecture](software-design-architecture-coverage.md) ayrıca 97 node scope'tur. Bu matristeki eski milestone/evidence owner'ları korunur. Day 48/64/78/99/117 kendi roadmap checkpoint'leridir; **[Day 131](../roadmap/day-131.md) yedi-roadmap final audit** yürürlüktedir. Emlak 85 günlük programı değişmez; yeni araç görevleri Planlandı'dır.
