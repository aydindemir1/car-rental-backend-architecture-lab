# Full Stack roadmap — iki proje kapsamı

Kaynak: [roadmap.sh/full-stack](https://roadmap.sh/full-stack); snapshot tarihi 2026-10-07. Kullanıcı kararı: Node.js ve Basic AWS Services hariç, sarı/mor/mavi konuların en az bir projede gerçek öğrenme ve uygulama görevi bulunur. Emlak 85 günlük programı değiştirilmez; eksikler araç kiralamaya eklenir.

## Envanter ve istisnalar

Canlı snapshot 19 ana topic düğümü içerir; Node.js ve Basic AWS Services çıkarıldığında 17 zorunlu ana konu kalır. Bu sürümde topic/subtopic düğümlerinde mor/yeşil legend verisi bulunmuyor; renkli tik varmış gibi sınıflandırma yapılmaz. Bütün uygulanabilir ana konular, checkpoint'ler ve mavi Frontend/Backend/DevOps kutuları matrise alınır. Mavi AWS ve Route53/SES/EC2/VPC/S3 alt dalları Basic AWS Services istisnasıyla kapsam dışıdır.

Node.js backend/framework/API geliştirme konusu yoktur. npm/Vite frontend tooling'in gerektirdiği yerel Node executable yalnız build/test aracıdır; Node.js backend öğrenildi veya kullanıldı olarak işaretlenmez. Java/Spring Boot/Spring Cloud backend kalır. Ücretli AWS/cloud hesapları açılmaz.

## Ana konu matrisi

| Full Stack ana konusu | Emlak planı | Araç kiralama görevi | Kapanış kanıtı |
|---|---|---|---|
| HTML | Frontend yok | Day 04 | Semantic ekran/form ve keyboard/a11y test |
| CSS | Frontend yok | Day 05 | Responsive grid/flex ve focus durumları |
| JavaScript | Backend Java | Day 06 | DOM/event/async/fetch/cancellation ve failure UX |
| npm | Yok | Day 05 bootstrap + Day 06 kapsamlı | Manifest/lockfile/scripts, clean npm ci/build/test |
| Tailwind CSS | Yok | Day 05 | Gerçek frontend compiled CSS, responsive/focus tests |
| React | Yok | Day 06 + Day 45 | Component/state/forms/router/API entegrasyonu ve browser E2E |
| Git | Bütün günlerde | Bütün günlerde; Day 07 | Branch/commit/diff, review ve conflict resolution fixture |
| GitHub | Bütün günlerde | Day 07,34 | PR/checks ve secretsız CI workflow |
| Node.js | Kapsam dışı | Kapsam dışı | Java backend seçildi; CLI checkpoint Java ile |
| PostgreSQL | Auth/UserProfile baseline | Yeni DB zorunlu değil; iki proje audit | Emlak gerçek PostgreSQL persistence/migration/test kanıtı |
| RESTful APIs | Day 12 ve servisler | Day 08,45 | API contract, validation/pagination ve negatif test |
| JWT Auth | Mevcut auth + Day 14 | Day 13,16,18,45 | Issuer/signature/expiry/scope doğrulama, 401/403 |
| Redis | Day 13,23 | Memcached alternatif; Redis emlakta | Cache/invalidation ve rate limit actual test |
| Linux Basics | Day 46 | Day 02,31,46 | Process/port/permission/filesystem ve troubleshooting |
| Basic AWS Services | Kapsam dışı | Kapsam dışı | Local deploy; AWS alt dalları uygulanmaz |
| Monit | Yok | Day 46 | İzole host process/HTTP/file check + bounded recovery |
| GitHub Actions | Mevcut hafif CI | Day 34 full CI | Build/test/security/artifact gate ve negative failure |
| Ansible | Day 63,65,84 | Tekrar kurma zorunlu değil | Yerel host idempotence ve rebuild evidence |
| Terraform | Day 64,65,84 | Tekrar kurma zorunlu değil | Somut local kaynak, plan/apply/drift/rebuild evidence |

## Checkpoint görevleri

| Checkpoint | Gün / sahibi | Gerçek uygulama |
|---|---|---|
| Static Webpages | Araç 04–05 | Araç listesi/detay/rezervasyon formu; backend gerekmeyen başlangıç |
| Interactivity | Araç 06 | Filtre/form/event/fetch ve hata durumları |
| External Packages | Araç 06 | Lisansı/dependency rolü belgelenmiş npm package, lockfile ve tekrar build |
| Collaborative Work | Araç 07,34 | Branch→PR→review/checks; kişi yoksa solo review simülasyonu açıkça etiketlenir |
| Frontend Apps | Araç 06,45 | React route/form/API portalı; unit ve browser testi |
| CLI Apps | Araç 07 | Java/Spring Boot kısa bakım CLI'si; Node.js backend yerine geçmez |
| Simple CRUD Apps | Araç 08,10–11 | MariaDB üzerinde Booking API CRUD/state guard; PostgreSQL ürünü emlakta |
| Complete App | Araç 45 | Browser→edge→BFF/Gateway→canonical write→derived read gerçek E2E |
| Deployment | Araç 14,31–32,35 | Nginx static portal ve local Docker/K8s; AWS deploy yok |
| Automation | Emlak 63–65 + Araç 34–35 | Idempotent host/IaC + CI/GitOps; evidence referansları |
| Monitoring | Araç 36,46 | OTel dashboard ve Monit bounded host checks; farklı görevler |
| CI/CD | Araç 34–35 | GitHub Actions/Flux commit→artifact→local deployment zinciri |
| Infrastructure | Emlak 63–65 + Araç 31–32 | Local network/storage/cluster ve yeniden oluşturma |

## Mavi başlıklar

| Başlık | Uygulama kapsamı |
|---|---|
| Frontend | Araç Day 04–06,14–18,29,45; HTML/CSS/JS/npm/Tailwind/React |
| Backend | Emlak Day 1–45 ve araç Day 07–30,38–44; Java/Spring |
| DevOps | Emlak Day 46–85 ve araç Day 31–36,46 |
| AWS | Kullanıcının Basic AWS Services istisnasıyla kapsam dışı |

Bu kutuların başka roadmap'e bağlantı vermesi bağlı roadmap'in bütün dallarını sessizce yeni scope yapmaz; Full Stack snapshot'ın uygulanabilir konuları burada somutlaştırılır.

## Kapanış yükümlülüğü

Bütün satırlar bugün **Planlandı** kapsamındadır. Konu yalnız belgede geçtiği için kapanmaz; sahibi projede implementation SHA, runtime success/failure testi ve evidence gerekir. Day 48 hem Backend hem Full Stack matrisini kontrol eder. Emlakta aynı konunun planı var ancak uygulama kanıtı eksikse eksik görev araç kiralama programında tutulur; emlak planı büyütülmez.
