# Zorunlu öğrenme ve uygulama sözleşmesi

Karar: 2026-10-07. Hedef farklı mimari, yaklaşım, prensip, pattern ve teknolojileri öğrenmek ve uygulamaktır. Emlak projesi 85 gün olarak korunur; eksik scope araç kiralama projesinin programına aittir.

## Kapsam yükümlülüğü

1. Backend snapshot'ındaki 23 sarı ana başlığın, mor tikli alt başlıkların ve mavi konuların en az bir projede açık öğrenme + gerçek temsilî uygulama + runtime doğrulama görevi bulunur.
2. Yalnız başlık kaydı, karşılaştırma belgesi veya dependency eklemek uygulama yerine geçmez. Product-specific mor seçimlerde ürünün kendisi öğrenilir: Nginx ve Claude Code örnekleri.
3. Her konu satırında owner proje/milestone, öğrenme çıktısı, uygulama commit'i, başarı/hata testi ve evidence bulunur. Planlama aşamasında bunlar future task'tır; günü geldiğinde yapılır.
4. Emlakta zaten planlanan konu araç kiralamada sırf sayısal çeşitlilik için tekrar kurulmaz. Emlak kapsamının yeterliliği runtime evidence ile denetlenir; eksik zorunlu görev gerektiğinde araç kiralama programına bağlanır.
5. Yeşil alternatiflerden requirement'ı anlamlı olanlar öğrenilir ve uygulanır; mevcut seçilenler MariaDB/Memcached/Solr/SQLite/TimescaleDB/CouchDB'dir. Aynı capability'ye iki competing canonical owner verilmez.
6. Gri/tiksiz konular planlanan ek kapsamda izlenir; yeşil ürünlerin tamamını kurmak zorunlu değildir.

## Başlık anlamı ve local eğitim sınırı

- “Bir backend dili seç”: Java/Spring Boot seçimi başlığı karşılar. Frontend JavaScript/TypeScript ayrıca uygulanır. Mor Go/Python seçenekleri tüm dilleri aynı anda seçme zorunluluğu değildir.
- Mavi Docker/Kubernetes/System Design/Full Stack/Prompt Engineering/AI Agents gibi konular için gerçek görevler bulunur. Başka roadmap'e bağlantı verilmesi o roadmap'in bütün alt dallarını sessizce bu kapsamın parçası yapmaz.
- Firebase local emulator kullanımında gerçek Realtime Database davranışı/Security Rules deneyleri yapılır; production cloud işletimi veya feature parity iddiası yoktur.
- Serverless için Knative scale-to-zero/cold-start gerçekten ölçülür; cloud hesabı zorunlu değildir.
- Claude Code için yerel Ollama model kullanılır; client/model lisansı, compatible tools/context ve makine kapasitesi kontrol edilir. Free local koşullar nedeniyle çalıştırılamazsa açık gap bırakılır, “comparison yeterli” denmez.
- Semantik veya yasal/lisans/resource engeli konuyu silently dropping gerekçesi değildir: sahibi, gerekçe ve çözüm işi programda açık kalır.

## Kapanış

Day 48 Backend/Full Stack ara audit'idir; Day 64, her zorunlu konunun iki projenin en az birinde uygulama+test kanıtını kontrol eder. Comparison veya Design Only, zorunlu konu satırını tamamlandı yapmaz. Bu karar günlük programın kapsam yükümlülüğüdür; yeni konular bugün çalıştırıldı anlamına gelmez.


## Full Stack roadmap kapsamı

Aynı öğrenme+gerçek uygulama+test yükümlülüğü [Full Stack matrisine](full-stack-coverage.md) de uygulanır. Node.js backend ve Basic AWS Services ile bağlı AWS alt dalları kullanıcının explicit istisnasıdır. npm build tooling local runtime gerektirir; bu backend Node eğitimi değildir. Matrix'in 17 uygulanabilir ana başlığı ve mavi Frontend/Backend/DevOps sorumlulukları iki projede en az birinde yerine getirilir. Snapshot mor/yeşil legend taşımıyorsa varmış gibi sınıflandırılmaz; eksik frontend ve işletim konuları günlük görevlere eklenir. Emlak değiştirilmez.


## System Design kapsamı

[System Design matrisi](system-design-coverage.md) kullanıcı talebiyle ayrıca kapsamdır. 27 ana konu + 120 alt konu occurrence'ı + Backend/Software Architect/DevOps mavi konuları görev sahibine bağlanır. Snapshot mor/yeşil tik taşımadığı için tikler uydurulmaz; bütün alt konular öğrenme, uygulama ve runtime test kapsamındadır. Node ID bazında kapsama denetimi yapılır; tekrar etiketlerde ortak evidence kullanılabilir.

Day 49–63 eksik deneyleri uygular; Day 64 Backend/Full Stack/System Design final audit'idir. Emlak mevcut uygulamaları evidence ile karşılar; karşılanmayan zorunlu konu araçta açık görev kalır. Geodes/stamps/CDN/leader seçim deneylerinin yerel sınırları ve correctness/failure sözleşmeleri saklanır; cloud sağlayıcı kullanılması zorunlu değildir.
