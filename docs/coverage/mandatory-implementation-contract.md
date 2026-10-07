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

Day 48 Backend/Full Stack ara audit'idir; Day 99, her zorunlu konunun iki projenin en az birinde uygulama+test kanıtını kontrol eder. Comparison veya Design Only, zorunlu konu satırını tamamlandı yapmaz. Bu karar günlük programın kapsam yükümlülüğüdür; yeni konular bugün çalıştırıldı anlamına gelmez.


## Full Stack roadmap kapsamı

Aynı öğrenme+gerçek uygulama+test yükümlülüğü [Full Stack matrisine](full-stack-coverage.md) de uygulanır. Node.js backend ve Basic AWS Services ile bağlı AWS alt dalları kullanıcının explicit istisnasıdır. npm build tooling local runtime gerektirir; bu backend Node eğitimi değildir. Matrix'in 17 uygulanabilir ana başlığı ve mavi Frontend/Backend/DevOps sorumlulukları iki projede en az birinde yerine getirilir. Snapshot mor/yeşil legend taşımıyorsa varmış gibi sınıflandırılmaz; eksik frontend ve işletim konuları günlük görevlere eklenir. Emlak değiştirilmez.


## System Design kapsamı

[System Design matrisi](system-design-coverage.md) kullanıcı talebiyle ayrıca kapsamdır. 27 ana konu + 120 alt konu occurrence'ı + Backend/Software Architect/DevOps mavi konuları görev sahibine bağlanır. Snapshot mor/yeşil tik taşımadığı için tikler uydurulmaz; bütün alt konular öğrenme, uygulama ve runtime test kapsamındadır. Node ID bazında kapsama denetimi yapılır; tekrar etiketlerde ortak evidence kullanılabilir.

Day 49–63 eksik deneyleri uygular; Day 64 Backend/Full Stack/System Design ara checkpoint; Day 78 dört roadmap ara checkpoint; Day 99 beş roadmap final audit'idir. Emlak mevcut uygulamaları evidence ile karşılar; karşılanmayan zorunlu konu araçta açık görev kalır. Geodes/stamps/CDN/leader seçim deneylerinin yerel sınırları ve correctness/failure sözleşmeleri saklanır; cloud sağlayıcı kullanılması zorunlu değildir.


## DevOps kapsamı ve yeni final gate

[DevOps matrisi](devops-coverage.md) explicit kullanıcı talebiyle scope'tur. 22 sarı/topic, 46 mor ve 6 mavi occurrence owner/görev/statü sahibidir. Ücretsiz local ortamla uygulanabilen ürün-spesifik mor başlıklar aynı ürün üzerinde gerçek deneyle karşılanır; yalnız rol alternatifi aynı literal ürünün uygulaması sayılmaz.

Daha önce kabul edilen local/no-cloud sınırı korunur: AWS/Azure/GCP provider runtime **açık kapsam istisnası**, Cloudflare/AWS Lambda local runtime **Limited/Partial**, CircleCI ve Datadog actual hizmet kullanımı erişim yoksa **açık gap**. [İstisna belgesi](devops-cloud-exceptions.md) literal kapsamın tamamlanmadığını saklamaz. Ürün koşulları/licence/source değişirse sessiz dropping veya paid/trial'a geçiş olmaz.

Day 48 Backend/Full Stack ara audit; Day 64 Backend/Full Stack/System Design ara checkpoint; **Day 78 dört roadmap ara checkpoint**'idir. Yeşil ürünlerde seçilmiş uygulama ve comparison ayrılır. Full coverage raporu actual runtime ile istisna/gap sayısını ayrı verir; bütün mor ürünlerin birebir kullanıldığı açık engeller varken iddia edilmez.


## Frontend kapsamı ve yürürlükteki final gate

[Frontend matrisi](frontend-coverage.md) explicit kullanıcı talebidir. Desktop/Mobile parent/child occurrence'ları hariç; 30 sarı + 35 mor + 7 mavi = 72 required occurrence gerçek günlük owner/göreve bağlanır. PWA web kapsamıdır; native mobile/desktop framework'leri uygulanmaz.

Mor product'lar literal öğrenme/temsilî uygulama/runtime test ister: Next.js SSR, TanStack Start SSR, Astro SSG, esbuild direct build, Apollo client, Vitest/Playwright ve local Claude Code bunlar arasındadır. Dependency adı, static export veya comparison yanlış capability'nin uygulaması sayılmaz.

Node business-backend eğitim istisnası korunur; Frontend mavi Nodejs ve SSR explicit talebi için yalnız frontend rendering/lifecycle role'ü Day 91–92/97'de gerçek runtime görevidir. Java business owner/authorization/persistence canonical kalır. Önceki CSR fazının “tooling only” sınırı artık bu ayrı frontend rendering role'ü ile birlikte okunur.

Day 48 iki roadmap, Day 64 üç roadmap, Day 78 dört roadmap ara checkpoint; **Day 99 beş roadmap final audit**. Önceki bölümlerdeki final gate ifadeleri kendi tarihsel checkpoint kapsamıdır; yürürlükte nihai gate Day 99'dur. Required ve seçilmiş green satırlar implementation/browser/runtime evidence ile kapanır; Cloudflare/Pages/Claude Code erişim engelleri açık gap/Partial olarak raporlanır.
