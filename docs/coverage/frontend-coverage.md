# Frontend — İki proje kapsam matrisi

Kaynak: [roadmap.sh/frontend](https://roadmap.sh/frontend), canlı graph **2026-10-07**. [Snapshot](frontend-roadmap-snapshot.json), [ortak plan](../FRONTEND-ROADMAP-EXTENSION.md), [günlük görevler](../roadmap/README.md).

## Kapsam

| Sınıf | Occurrence sayısı | Yükümlülük |
|---|---:|---|
| Sarı ana konu | 30 | Öğrenme + temsilî uygulama + test |
| Mor konu/alt konu | 35 | Ürün-spesifik gerçek deney; erişim gap'leri açık |
| Mavi konu | 7 | Nodejs, Fullstack, Backend, Design System, TypeScript, Prompt Engineering, AI Agents Roadmap |
| Yeşil alternatif | 31 | Seçilmiş gerçek profiller; diğerleri gerekçeli Comparison |
| Gri | 4 | Web Components altları ve PWAs; ayrıca gerçek görevler |
| Tiksiz alt konu | 12 | AI ve SSR alt görevleri; scope/status açık |
| **Toplam** | **119** | **72 required occurrence + 47 diğer** |

Graph'taki topic sınıfı her zaman sarı değildir: React/GraphQL mor; Vue.js/SvelteKit yeşil; PWAs gri topic'tir. Renk/legend preserved; aynı ürün farklı SSR/SSG dalında farklı node ID ile bulunabilir. **Desktop Apps/Mobile Apps ve bağlı native ürünleri 8 occurrence olarak hariç**; 5 navigasyon button'ı eğitim konusu değildir.

Emlak frontend içermez; 85 günlük planı büyütülmez. Çoğu frontend sahibi araç kiralamadır; mevcut Java API/security/DevOps/AI evidence'ı yeniden kullanılabilir. Referans emlak branch HEAD'i `a84beefb0d8d932a01056fbd4542910856129a28`. Araç Day 78 dört roadmap ara checkpoint; Day 79–98 ek deneyler; Day 99 beş roadmap final audit. Bütün mevcut/yeni ürün görevleri **Planlandı**; matriste bulunmaları bugün öğrenilip uygulanmış oldukları anlamına gelmez.

## Sarı ana başlıkların günlük owner'ı

| Konu | Mevcut temel | Günlük uygulama/test | Durum |
|---|---|---|---|
| Internet | Araç Day 02–03/52/68 | [Day 79](../roadmap/day-79.md) | Planlandı / evidence yok |
| HTML | Araç Day 04/45 | [Day 79](../roadmap/day-79.md) | Planlandı / evidence yok |
| CSS | Araç Day 05 | [Day 80](../roadmap/day-80.md) | Planlandı / evidence yok |
| JavaScript | Araç Day 06 | [Day 81](../roadmap/day-81.md) | Planlandı / evidence yok |
| VCS Hosting | Araç Day 07/34 | [Day 84](../roadmap/day-84.md) | Planlandı / evidence yok |
| Version Control | Araç Day 07/34 | [Day 84](../roadmap/day-84.md) | Planlandı / evidence yok |
| Package Managers | Araç Day 06 | [Day 84](../roadmap/day-84.md) | Planlandı / evidence yok |
| Learn a Framework | Araç Day 06 | [Day 83](../roadmap/day-83.md) | Planlandı / evidence yok |
| CSS Frameworks | Araç Day 05 | [Day 80](../roadmap/day-80.md) | Planlandı / evidence yok |
| Linters & Formatters | Yeni açık frontend görevi | [Day 86](../roadmap/day-86.md) | Planlandı / evidence yok |
| Module Bundlers | Yeni açık frontend görevi | [Day 85](../roadmap/day-85.md) | Planlandı / evidence yok |
| Testing | Yeni açık frontend görevi | [Day 87](../roadmap/day-87.md) | Planlandı / evidence yok |
| Auth Strategies | Araç Day 14/16–18/38/63 | [Day 89](../roadmap/day-89.md) | Planlandı / evidence yok |
| Web Security | Araç Day 14/16–18/38/63 | [Day 89](../roadmap/day-89.md) | Planlandı / evidence yok |
| Web Components | Yeni açık frontend görevi | [Day 88](../roadmap/day-88.md) | Planlandı / evidence yok |
| Type Checkers | Araç Day 06 | [Day 82](../roadmap/day-82.md) | Planlandı / evidence yok |
| SSR | Yeni açık frontend görevi | [Day 91](../roadmap/day-91.md) | Planlandı / evidence yok |
| SSG | Yeni açık frontend görevi | [Day 93](../roadmap/day-93.md) | Planlandı / evidence yok |
| Deployment | Yeni açık frontend görevi | [Day 96](../roadmap/day-96.md) | Planlandı / evidence yok |
| Performance | Yeni açık frontend görevi | [Day 94](../roadmap/day-94.md) | Planlandı / evidence yok |
| Design Systems | Yeni açık frontend görevi | [Day 88](../roadmap/day-88.md) | Planlandı / evidence yok |
| Web APIs | Yeni açık frontend görevi | [Day 81](../roadmap/day-81.md) | Planlandı / evidence yok |
| Accessibility | Araç Day 04/45 | [Day 79](../roadmap/day-79.md) | Planlandı / evidence yok |
| Learn the Basics | Araç Day 39–44 | [Day 98](../roadmap/day-98.md) | Planlandı / evidence yok |
| AI Assisted Coding | Araç Day 39–44 | [Day 98](../roadmap/day-98.md) | Planlandı / evidence yok |
| Prompting Techniques | Araç Day 39–44 | [Day 98](../roadmap/day-98.md) | Planlandı / evidence yok |
| Implementing AI | Araç Day 39–44 | [Day 98](../roadmap/day-98.md) | Planlandı / evidence yok |
| Agents | Araç Day 39–44 | [Day 98](../roadmap/day-98.md) | Planlandı / evidence yok |
| MCP | Araç Day 39–44 | [Day 98](../roadmap/day-98.md) | Planlandı / evidence yok |
| Skills | Araç Day 39–44 | [Day 98](../roadmap/day-98.md) | Planlandı / evidence yok |

## Yeni günlük program

| Day | Öğrenme/uygulama | Doğrulama |
|---|---|---|
| [79](../roadmap/day-79.md) | Internet, semantic HTML ve erişilebilirlik temeli | Arama formu keyboard ve en az bir uygun screen reader akışında kullanılabilir; error doğru kontrolle ilişkilidir. Request/render waterfall ile semantik HTML ve private index/cache sınırı actual browser'da gözlenir. |
| [80](../roadmap/day-80.md) | CSS, responsive layout ve Tailwind | Dar/geniş viewport, zoom, uzun Türkçe metin ve keyboard focus'ta layout kullanılabilir. CSS production build beklenen sınıfları korur; gereksiz CSS ve contrast sorunları ölçülür. |
| [81](../roadmap/day-81.md) | JavaScript ve browser Web APIs | Eski/cancelled request yeni UI sonucunu ezmez; event/observer/worker unmount sonrası temizlenir. Storage quota/permission/unsupported API ve offline durumunda kontrollü fallback vardır. |
| [82](../roadmap/day-82.md) | TypeScript ve runtime contract sınırları | Kasıtlı type error gate'i kırar; malformed API payload runtime'da reddedilir. Loading/success/error union'ları exhaustiveness kontrolüne sahiptir; browser artifact'ta server credential yoktur. |
| [83](../roadmap/day-83.md) | React uygulama mimarisi ve route/state tasarımı | Deep link/back/forward ve hızlı filtre değişimi tutarlı state üretir. Route/error/unmount ve yetkisiz akışlarda resource cleanup ve backend authorization korunur. |
| [84](../roadmap/day-84.md) | npm, pnpm, yarn ve Bun paket deneyleri | Dört uygun profil fixture'ı build eder veya explicit compatibility gap kaydeder; geçerli lockfile ve clean install testlidir. Hatalı lock/dependency CI gate'ini kırar; secret veya generated dependency tree Git'e taşınmaz. |
| [85](../roadmap/day-85.md) | Vite, esbuild ve bundler/compiler lab'ı | Her seçilmiş araç için gerçek transform/bundle artifact ve browser runtime sonucu vardır. Broken chunk/env/source-map ve incompatible config testleri kontrollü hata üretir; build ölçüm koşulları sabittir. |
| [86](../roadmap/day-86.md) | ESLint, Prettier ve Biome kalite gate'leri | Kasıtlı bug/format ihlali doğru gate'i kırar; düzeltme sonrası gate geçer. Biome karşılaştırması gerçek output ile kaydedilir; ana repo tek formatting policy'ye sahiptir. |
| [87](../roadmap/day-87.md) | Vitest, Playwright ve test alternatifleri | Kasıtlı validation/auth/idempotency regression testleri kırar; gerçek Java integration ayrı evidence'a sahiptir. Dört ürünün seçilmiş gerçek test koşusu kayıtlıdır; flaky retry bug'ı sessiz gizlemez. |
| [88](../roadmap/day-88.md) | Design System ve Web Components | Design system component'leri keyboard/screen reader testine sahiptir. Web Component template/shadow/style/event/lifecycle davranışı gerçek React browser integration'da çalışır. |
| [89](../roadmap/day-89.md) | Frontend authentication ve web security | Unauthorized/expired session/CSRF/origin/XSS fixture'ları beklenen 401/403/block davranışını üretir. Cross-user cache/token disclosure oluşmaz; Java backend authorization browser guard bypass'ta da çalışır. |
| [90](../roadmap/day-90.md) | GraphQL: Apollo ve Relay Modern | Apollo pagination/cache/auth ve server error gerçek Java API'da doğrulanır. Relay compiler/read UI runtime ve schema drift gate'i actual evidence'a sahiptir. |
| [91](../roadmap/day-91.md) | Next.js ile gerçek SSR ve Node render sınırı | Java read fixture request-time değişince SSR initial HTML değişir; JS kapalıyken public veri görünür. Hydration/streaming ve SSR failure/recovery gerçek runtime'da gözlenir; cross-user credential/cache sızıntısı yoktur. |
| [92](../roadmap/day-92.md) | TanStack Start ile SSR/streaming karşılaştırması | TanStack Start initial HTML/hydration/request-time read gerçek runtime'da çalışır. Client disconnect/upstream error sonrası renderer cleanup olur; streaming beklenen zaman/byte davranışını gösterir. |
| [93](../roadmap/day-93.md) | Astro, SSG ve statik içerik modelleri | Astro/Next export/Eleventy/VuePress artifact'ı clean build ve local web server'da çalışır. Build sonrası API verisi değişince statik içerik otomatik güncelmiş gibi davranmaz; private veri artifact'a girmez. |
| [94](../roadmap/day-94.md) | Frontend performance, cache ve Lighthouse | Seçilmiş performance hipotezi aynı koşullarda önce/sonra ölçülür; invariant/UI davranışı korunur. Stale chunk/cache/private response ve memory cleanup testleri çalışır; field/lab sınırı raporlanır. |
| [95](../roadmap/day-95.md) | PWA, service worker ve offline taslaklar | Offline readonly/taslak çalışır; booking mutation online owner onayı olmadan kesinleşmez. Worker upgrade/cache cleanup ve logout sonrası private data isolation doğrulanır. |
| [96](../roadmap/day-96.md) | Frontend deployment ve hosting kapsamı | Local static/SSR deploy, deep link/asset/cache/rollback gerçek browser'da doğrulanır. Pages actual deploy varsa public URL evidence kaydedilir; Cloudflare local/managed ve erişim gap'leri birbirine karıştırılmaz. |
| [97](../roadmap/day-97.md) | Yeşil frontend framework alternatifleri | Dört framework ailesinin selected UI/browser error/cancel/cleanup evidence'ı vardır. Nuxt/SvelteKit SSR initial HTML request-time değişir; Angular SSR ayrıca kanıtlanmadıysa SSR occurrence Partial kalır. |
| [98](../roadmap/day-98.md) | Frontend AI, prompting, MCP, skills ve agents | AI task actual local tool/model çağrısı, developer review ve regression evidence'ına sahiptir. Streaming/cancel/injection/denied-tool davranışı gerçek UI/API'da gözlenir; secrets veya kullanıcı verisi modele gönderilmez. |
| [99](../roadmap/day-99.md) | Beş roadmap ve iki proje final audit | Beş roadmap satırlarında açık ownersız required konu yoktur; actual evidence olmadan Verified yoktur. Browser E2E/recovery ve a11y/security/cache invariants doğru; Desktop/Mobile native uygulaması scope'a sızmaz. |

## 119 düğümün tam eşleştirmesi

Owner günü somut implementation, browser/API/runtime success/failure/recovery ve commit sırası içerir. Tekrar label aynı evidence'ı ancak ilgili capability gerçekten karşılanıyorsa paylaşabilir: React CSR routing SSR değildir; Next static export SSR değildir; Astro SSG SSR değildir.

| Node ID | Renk | Roadmap etiketi | Mevcut temel | Owner / görev | Status / sınır |
|---|---|---|---|---|---|
| `VlNNwIEDWqQXtqkHWJYzC` | Sarı | Internet | Araç Day 02–03/52/68 | [Day 79](../roadmap/day-79.md) | Planlandı / evidence yok |
| `yCnn-NfSxIybUQ2iTuUGq` | Mor | How does the internet work? | Araç Day 02–03/52/68 | [Day 79](../roadmap/day-79.md) | Planlandı / evidence yok |
| `R12sArWVpbIs_PHxBqVaR` | Mor | What is HTTP? | Araç Day 02–03/52/68 | [Day 79](../roadmap/day-79.md) | Planlandı / evidence yok |
| `ZhSuu2VArnzPDp6dPQQSC` | Mor | What is Domain Name? | Araç Day 02–03/52/68 | [Day 79](../roadmap/day-79.md) | Planlandı / evidence yok |
| `aqMaEY8gkKMikiqleV5EP` | Mor | What is hosting? | Araç Day 02–03/52/68 | [Day 79](../roadmap/day-79.md) | Planlandı / evidence yok |
| `hkxw9jPGYphmjhTjw8766` | Mor | DNS and how it works? | Araç Day 02–03/52/68 | [Day 79](../roadmap/day-79.md) | Planlandı / evidence yok |
| `P82WFaTPgQEPNp5IIuZ1Y` | Mor | Browsers and how they work? | Araç Day 02–03/52/68 | [Day 79](../roadmap/day-79.md) | Planlandı / evidence yok |
| `yWG2VUkaF5IJVVut6AiSy` | Sarı | HTML | Araç Day 04/45 | [Day 79](../roadmap/day-79.md) | Planlandı / evidence yok |
| `ZhJhf1M2OphYbEmduFq-9` | Sarı | CSS | Araç Day 05 | [Day 80](../roadmap/day-80.md) | Planlandı / evidence yok |
| `ODcfFEorkfJNupoQygM53` | Sarı | JavaScript | Araç Day 06 | [Day 81](../roadmap/day-81.md) | Planlandı / evidence yok |
| `MXnFhZlNB1zTsBFDyni9H` | Sarı | VCS Hosting | Araç Day 07/34 | [Day 84](../roadmap/day-84.md) | Planlandı / evidence yok |
| `NIY7c4TQEEHx0hATu-k5C` | Sarı | Version Control | Araç Day 07/34 | [Day 84](../roadmap/day-84.md) | Planlandı / evidence yok |
| `R_I4SGYqLk5zze5I1zS_E` | Mor | Git | Araç Day 07/34 | [Day 84](../roadmap/day-84.md) | Planlandı / evidence yok |
| `IqvS1V-98cxko3e9sBQgP` | Sarı | Package Managers | Araç Day 06 | [Day 84](../roadmap/day-84.md) | Planlandı / evidence yok |
| `qmTVMJDsEhNIkiwE_UTYu` | Mor | GitHub | Araç Day 07/34 | [Day 84](../roadmap/day-84.md) | Planlandı / evidence yok |
| `zIoSJMX3cuzCgDYHjgbEh` | Yeşil | GitLab | Araç Day 69 local GitLab | [Day 84](../roadmap/day-84.md) | Planlandı / evidence yok |
| `yrq3nOwFREzl-9EKnpU-e` | Yeşil | yarn | Yeni açık frontend görevi | [Day 84](../roadmap/day-84.md) | Planlandı / evidence yok |
| `SLxA5qJFp_28TRzr1BjxZ` | Yeşil | pnpm | Yeni açık frontend görevi | [Day 84](../roadmap/day-84.md) | Planlandı / evidence yok |
| `ib_FHinhrw8VuSet-xMF7` | Mor | npm | Araç Day 06 | [Day 84](../roadmap/day-84.md) | Planlandı / evidence yok |
| `eXezX7CVNyC1RuyU_I4yP` | Sarı | Learn a Framework | Araç Day 06 | [Day 83](../roadmap/day-83.md) | Planlandı / evidence yok |
| `-bHFIiXnoUQSov64WI9yo` | Yeşil | Angular | Yeni açık frontend görevi | [Day 97](../roadmap/day-97.md) | Planlandı / evidence yok |
| `ERAdwL1G9M1bnx-fOm5ZA` | Yeşil | Vue.js | Yeni açık frontend görevi | [Day 97](../roadmap/day-97.md) | Planlandı / evidence yok |
| `tG5v3O4lNIFc2uCnacPak` | Mor | React | Araç Day 06 | [Day 83](../roadmap/day-83.md) | Planlandı / evidence yok |
| `ZR-qZ2Lcbu3FtqaMd3wM4` | Yeşil | Svelte | Yeni açık frontend görevi | [Day 97](../roadmap/day-97.md) | Planlandı / evidence yok |
| `DxOSKnqAjZOPP-dq_U7oP` | Yeşil | Solid JS | Yeni açık frontend görevi | [Day 97](../roadmap/day-97.md) | Planlandı / evidence yok |
| `XDTD8el6OwuQ55wC-X4iV` | Sarı | CSS Frameworks | Araç Day 05 | [Day 80](../roadmap/day-80.md) | Planlandı / evidence yok |
| `eghnfG4p7i-EDWfp3CQXC` | Mor | Tailwind | Araç Day 05 | [Day 80](../roadmap/day-80.md) | Planlandı / evidence yok |
| `9VcGfDBBD8YcKatj4VcH1` | Sarı | Linters & Formatters | Yeni açık frontend görevi | [Day 86](../roadmap/day-86.md) | Planlandı / evidence yok |
| `hkSc_1x09m7-7BO7WzlDT` | Sarı | Module Bundlers | Yeni açık frontend görevi | [Day 85](../roadmap/day-85.md) | Planlandı / evidence yok |
| `NS-hwaWa5ebSmNNRoxFDp` | Yeşil | Parcel | Yeni açık frontend görevi | [Day 85](../roadmap/day-85.md) | Planlandı / evidence yok |
| `sCjErk7rfWAUvhl8Kfm3n` | Yeşil | Rollup | Yeni açık frontend görevi | [Day 85](../roadmap/day-85.md) | Planlandı / evidence yok |
| `4W7UXfdKIUsm1bUrjdTVT` | Mor | esbuild | Yeni açık frontend görevi | [Day 85](../roadmap/day-85.md) | Planlandı / evidence yok |
| `0Awx3zEI5_gYEIrD7IVX6` | Mor | Vite | Yeni açık frontend görevi | [Day 85](../roadmap/day-85.md) | Planlandı / evidence yok |
| `zbkpu_gvQ4mgCiZKzS1xv` | Mor | Prettier | Yeni açık frontend görevi | [Day 86](../roadmap/day-86.md) | Planlandı / evidence yok |
| `NFjsI712_qP0IOmjuqXar` | Mor | ESLint | Yeni açık frontend görevi | [Day 86](../roadmap/day-86.md) | Planlandı / evidence yok |
| `igg4_hb3XE3vuvY8ufV-4` | Sarı | Testing | Yeni açık frontend görevi | [Day 87](../roadmap/day-87.md) | Planlandı / evidence yok |
| `hVQ89f6G0LXEgHIOKHDYq` | Mor | Vitest | Yeni açık frontend görevi | [Day 87](../roadmap/day-87.md) | Planlandı / evidence yok |
| `g5itUjgRXd9vs9ujHezFl` | Yeşil | Jest | Yeni açık frontend görevi | [Day 87](../roadmap/day-87.md) | Planlandı / evidence yok |
| `jramLk8FGuaEH4YpHIyZT` | Mor | Playwright | Yeni açık frontend görevi | [Day 87](../roadmap/day-87.md) | Planlandı / evidence yok |
| `DaynCz5RR26gjT6N6gTDL` | Yeşil | Cypress | Yeni açık frontend görevi | [Day 87](../roadmap/day-87.md) | Planlandı / evidence yok |
| `U5mD5FmVx7VWeKxDpQxB5` | Sarı | Auth Strategies | Araç Day 14/16–18/38/63 | [Day 89](../roadmap/day-89.md) | Planlandı / evidence yok |
| `RDWbG3Iui6IPgp0shvXtg` | Sarı | Web Security | Araç Day 14/16–18/38/63 | [Day 89](../roadmap/day-89.md) | Planlandı / evidence yok |
| `AfH2zCbqzw0Nisg1yyISS` | Mor | CORS | Araç Day 14/16–18/38/63 | [Day 89](../roadmap/day-89.md) | Planlandı / evidence yok |
| `uum7vOhOUR38vLuGZy8Oa` | Mor | HTTPS | Araç Day 14/16–18/38/63 | [Day 89](../roadmap/day-89.md) | Planlandı / evidence yok |
| `rmcm0CZbtNVC9LZ14-H6h` | Mor | CSP | Araç Day 14/16–18/38/63 | [Day 89](../roadmap/day-89.md) | Planlandı / evidence yok |
| `JanR7I_lNnUCXhCMGLdn-` | Mor | OWASP Risks | Araç Day 14/16–18/38/63 | [Day 89](../roadmap/day-89.md) | Planlandı / evidence yok |
| `ruoFa3M4bUE3Dg6GXSiUI` | Sarı | Web Components | Yeni açık frontend görevi | [Day 88](../roadmap/day-88.md) | Planlandı / evidence yok |
| `NQ95TJCe3E1IwEuBa__D6` | Sarı | Type Checkers | Araç Day 06 | [Day 82](../roadmap/day-82.md) | Planlandı / evidence yok |
| `VxiQPgcYDFAT6WgSRWpIA` | Gri | Custom Elements | Yeni açık frontend görevi | [Day 88](../roadmap/day-88.md) | Planlandı / evidence yok |
| `Hk8AVonOd693_y1sykPqd` | Gri | HTML Templates | Yeni açık frontend görevi | [Day 88](../roadmap/day-88.md) | Planlandı / evidence yok |
| `-SpsNeOZBkQfDA-rwzgPg` | Gri | Shadow DOM | Yeni açık frontend görevi | [Day 88](../roadmap/day-88.md) | Planlandı / evidence yok |
| `Cxspmb14_0i1tfw-ZLxEu` | Sarı | SSR | Yeni açık frontend görevi | [Day 91](../roadmap/day-91.md) | Planlandı / evidence yok |
| `OL8I6nOZ8hGGWmtxg_Mv8` | Tiksiz | Svelte | Yeni açık frontend görevi | [Day 97](../roadmap/day-97.md) | Planlandı / evidence yok |
| `3TE_iYvbklXK0be-5f2M7` | Yeşil | Vue.js | Yeni açık frontend görevi | [Day 97](../roadmap/day-97.md) | Planlandı / evidence yok |
| `k6rp6Ua9qUEW_DA_fOg5u` | Yeşil | Angular | Yeni açık frontend görevi | [Day 97](../roadmap/day-97.md) | Planlandı: SSR uygunluğu gate; yoksa Partial |
| `SGDf_rbfmFSHlxI-Czzlz` | Mor | React | Araç Day 06 | [Day 91](../roadmap/day-91.md) | Planlandı / evidence yok |
| `KJRkrFZIihCUBrOf579EU` | Yeşil | react-router | Yeni açık frontend görevi | [Day 97](../roadmap/day-97.md) | Planlandı / evidence yok |
| `zNFYAJaSq0YZXL5Rpx1NX` | Mor | Next.js | Yeni açık frontend görevi | [Day 91](../roadmap/day-91.md) | Planlandı / evidence yok |
| `BBsXxkbbEG-gnbM1xXKrj` | Tiksiz | Nuxt.js | Yeni açık frontend görevi | [Day 97](../roadmap/day-97.md) | Planlandı / evidence yok |
| `P4st_telfCwKLSAU2WsQP` | Yeşil | SvelteKit | Yeni açık frontend görevi | [Day 97](../roadmap/day-97.md) | Planlandı / evidence yok |
| `L7AllJfKvClaam3y-u6DP` | Mor | GraphQL | Java read API Day 38; frontend client deneyi ek | [Day 90](../roadmap/day-90.md) | Planlandı / evidence yok |
| `5eUbDdOTOfaOhUlZAmmXW` | Mor | Apollo | Java read API Day 38; frontend client deneyi ek | [Day 90](../roadmap/day-90.md) | Planlandı / evidence yok |
| `0moPO23ol33WsjVXSpTGf` | Yeşil | Relay Modern | Yeni açık frontend görevi | [Day 90](../roadmap/day-90.md) | Planlandı / evidence yok |
| `n0q32YhWEIAUwbGXexoqV` | Sarı | SSG | Yeni açık frontend görevi | [Day 93](../roadmap/day-93.md) | Planlandı / evidence yok |
| `CMrss8E2W0eA6DVEqtPjT` | Yeşil | Vuepress | Yeni açık frontend görevi | [Day 93](../roadmap/day-93.md) | Planlandı / evidence yok |
| `XWJxV42Dpu2D3xDK10Pn3` | Yeşil | Nuxt.js | Yeni açık frontend görevi | [Day 97](../roadmap/day-97.md) | Planlandı / evidence yok |
| `iUxXq7beg55y76dkwhM13` | Mor | Astro | Yeni açık frontend görevi | [Day 93](../roadmap/day-93.md) | Planlandı / evidence yok |
| `io0RHJWIcVxDhcYkV9d38` | Yeşil | Eleventy | Yeni açık frontend görevi | [Day 93](../roadmap/day-93.md) | Planlandı / evidence yok |
| `V70884VcuXkfrfHyLGtUg` | Yeşil | Next.js | Yeni açık frontend görevi | [Day 93](../roadmap/day-93.md) | Planlandı / evidence yok |
| `PoM77O2OtxPELxfrW1wtl` | Gri | PWAs | Yeni açık frontend görevi | [Day 95](../roadmap/day-95.md) | Planlandı / evidence yok |
| `qXKNK_IsGS8-JgLK-Q9oU` | Mavi | Nodejs | Yeni açık frontend görevi | [Day 91](../roadmap/day-91.md) | Planlandı / evidence yok |
| `h26uS3muFCabe6ekElZcI` | Yeşil | SWC | Yeni açık frontend görevi | [Day 85](../roadmap/day-85.md) | Planlandı / evidence yok |
| `wA2fSYsbBYU02VJXAvUz8` | Yeşil | Astro | Yeni açık frontend görevi | [Day 93](../roadmap/day-93.md) | Planlandı / evidence yok |
| `slf6jmim4p9ti6ZRHOZe_` | Mavi | Fullstack | Araç Day 45 uçtan uca | [Day 99](../roadmap/day-99.md) | Planlandı / evidence yok |
| `j2H1qGosbveayviOCVkUs` | Yeşil | Bun | Yeni açık frontend görevi | [Day 84](../roadmap/day-84.md) | Planlandı / evidence yok |
| `UvCVChB6NZ_yUg0RdIJ2o` | Yeşil | Biome | Yeni açık frontend görevi | [Day 86](../roadmap/day-86.md) | Planlandı / evidence yok |
| `hE-DbpBpYrfB8tmBEjTnG` | Tiksiz | Rolldown | Yeni açık frontend görevi | [Day 85](../roadmap/day-85.md) | Planlandı / evidence yok |
| `f9zlP6lGhfe6HBHVYiySu` | Mor | Tanstack Start | Yeni açık frontend görevi | [Day 92](../roadmap/day-92.md) | Planlandı / evidence yok |
| `A1ZUy16cVRYqmHxoCtUb0` | Sarı | Deployment | Yeni açık frontend görevi | [Day 96](../roadmap/day-96.md) | Planlandı / evidence yok |
| `vpzh9bNXCxgdDFQLsot2_` | Mor | GitHub Pages | Yeni açık frontend görevi | [Day 96](../roadmap/day-96.md) | Planlandı: gerçek ücretsiz deploy evidence; erişim yoksa gap |
| `kPJ0jZo5AbOzvZgv0zwp0` | Yeşil | Vercel | Yeni açık frontend görevi | [Day 96](../roadmap/day-96.md) | Comparison: ücretli erişim zorunlu değil |
| `_Uh-UFNe2wP2TV0x2lKY_` | Mor | Cloudflare | Araç Day 75 local runtime | [Day 96](../roadmap/day-96.md) | Planlandı: local Partial; managed deploy gap |
| `o8GstE5gxcGByh-D7lwqT` | Yeşil | Netlify | Yeni açık frontend görevi | [Day 96](../roadmap/day-96.md) | Comparison: ücretli erişim zorunlu değil |
| `PJRsqg5Vx9gQTodxaeZfz` | Yeşil | Railway | Yeni açık frontend görevi | [Day 96](../roadmap/day-96.md) | Comparison: ücretli erişim zorunlu değil |
| `wfGz8pshGQARZ7qStGoSD` | Yeşil | Render | Yeni açık frontend görevi | [Day 96](../roadmap/day-96.md) | Comparison: ücretli erişim zorunlu değil |
| `6d8cjWZ4BuUjwT0seiuzJ` | Sarı | Performance | Yeni açık frontend görevi | [Day 94](../roadmap/day-94.md) | Planlandı / evidence yok |
| `dz7_QXoO7X0WmS5xuAhhJ` | Mor | Lighthouse | Yeni açık frontend görevi | [Day 94](../roadmap/day-94.md) | Planlandı / evidence yok |
| `JWU9jc12_ewaIKt3qWLcp` | Mor | DevTools Usage | Yeni açık frontend görevi | [Day 94](../roadmap/day-94.md) | Planlandı / evidence yok |
| `66ya3WdtlkjQyBTc3Lein` | Mor | Service Workers | Yeni açık frontend görevi | [Day 95](../roadmap/day-95.md) | Planlandı / evidence yok |
| `FyNXhHq1VIASNq-LI7JIu` | Mor | Streamed Responses | Yeni açık frontend görevi | [Day 92](../roadmap/day-92.md) | Planlandı / evidence yok |
| `ap4h4v5Sr4jBH3GwWSH8x` | Sarı | Design Systems | Yeni açık frontend görevi | [Day 88](../roadmap/day-88.md) | Planlandı / evidence yok |
| `3HgiMfqihjWceSxd6ei8s` | Sarı | Web APIs | Yeni açık frontend görevi | [Day 81](../roadmap/day-81.md) | Planlandı / evidence yok |
| `e-k6EhoxYG9h0x6vWOrDh` | Sarı | Accessibility | Araç Day 04/45 | [Day 79](../roadmap/day-79.md) | Planlandı / evidence yok |
| `Df3nTlTvSQkMGzpufRo9q` | Mavi | Backend | Emlak backend; araç Java/Spring Day 07–38 | [Day 99](../roadmap/day-99.md) | Planlandı / evidence yok |
| `-sFboM4eFUMVq1tlPl-fV` | Mavi | Design System | Yeni açık frontend görevi | [Day 88](../roadmap/day-88.md) | Planlandı / evidence yok |
| `6kWlgayUZQnr9z88fUOkk` | Mavi | TypeScript | Araç Day 06 | [Day 82](../roadmap/day-82.md) | Planlandı / evidence yok |
| `tWDmeXItfQDxB8Jij_V4L` | Mor | Cache-Control | Yeni açık frontend görevi | [Day 94](../roadmap/day-94.md) | Planlandı / evidence yok |
| `RcC1fVuePQZ59AsJfeTdR` | Mor | Claude Code | Araç Day 39–44 | [Day 98](../roadmap/day-98.md) | Planlandı: Day 40 local model evidence; erişim yoksa gap |
| `HQrxxDxKN8gizvXRU5psW` | Yeşil | Copilot | Yeni açık frontend görevi | [Day 98](../roadmap/day-98.md) | Comparison: ücretli erişim zorunlu değil |
| `CKlkVK_7GZ7xzIUHJqZr8` | Yeşil | Cursor | Yeni açık frontend görevi | [Day 98](../roadmap/day-98.md) | Comparison: ücretli erişim zorunlu değil |
| `E7-LveK7jO2npxVTLUDfw` | Yeşil | Antigravity | Yeni açık frontend görevi | [Day 98](../roadmap/day-98.md) | Comparison: ücretli erişim zorunlu değil |
| `yKNdBbahm_h81xdMDT-qx` | Tiksiz | How LLMs work | Araç Day 39–44 | [Day 98](../roadmap/day-98.md) | Planlandı / evidence yok |
| `IZKl6PxbvgNkryAkdy3-p` | Tiksiz | AI vs Traditional Coding | Araç Day 39–44 | [Day 98](../roadmap/day-98.md) | Planlandı / evidence yok |
| `0TMdly8yiqnNR8sx36iqc` | Tiksiz | Code Reviews | Araç Day 39–44 | [Day 98](../roadmap/day-98.md) | Planlandı / evidence yok |
| `q7NpwqQXUp4wt2to-yFiP` | Tiksiz | Docs Generation | Araç Day 39–44 | [Day 98](../roadmap/day-98.md) | Planlandı / evidence yok |
| `UTupdqjOyLh7-56_0SXJ8` | Sarı | Learn the Basics | Araç Day 39–44 | [Day 98](../roadmap/day-98.md) | Planlandı / evidence yok |
| `ipcNHz8KbfpE57kNP15hP` | Sarı | AI Assisted Coding | Araç Day 39–44 | [Day 98](../roadmap/day-98.md) | Planlandı / evidence yok |
| `Gv_g4gK6pZK6l_0xAn34X` | Sarı | Prompting Techniques | Araç Day 39–44 | [Day 98](../roadmap/day-98.md) | Planlandı / evidence yok |
| `Bic4PHhz-YqzPWRimJO83` | Tiksiz | Gemini | Yeni açık frontend görevi | [Day 98](../roadmap/day-98.md) | Comparison: ücretli erişim zorunlu değil |
| `-ye5ZtYFDoYGpj-UJaBP8` | Tiksiz | OpenAI | Yeni açık frontend görevi | [Day 98](../roadmap/day-98.md) | Comparison: ücretli erişim zorunlu değil |
| `Lw2nR7x8PYgq1P5CxPAxi` | Tiksiz | Anthropic | Yeni açık frontend görevi | [Day 98](../roadmap/day-98.md) | Comparison: ücretli erişim zorunlu değil |
| `MdYPIf_9ezbIp6Dm5Fyme` | Sarı | Implementing AI | Araç Day 39–44 | [Day 98](../roadmap/day-98.md) | Planlandı / evidence yok |
| `EYT2rTLZ8tUW2u8DOnAWF` | Tiksiz | Refactoring | Araç Day 39–44 | [Day 98](../roadmap/day-98.md) | Planlandı / evidence yok |
| `Nx7mjvYgqLpmJ0_iSx5of` | Tiksiz | Applications | Araç Day 39–44 | [Day 98](../roadmap/day-98.md) | Planlandı / evidence yok |
| `k4hMVVBMatedUq5EKiMo4` | Mavi | Prompt Engineering | Araç Day 39–44 | [Day 98](../roadmap/day-98.md) | Planlandı / evidence yok |
| `vpimgXt10UQFBDVHR21IU` | Mavi | AI Agents Roadmap | Araç Day 39–44 | [Day 98](../roadmap/day-98.md) | Planlandı / evidence yok |
| `e4j6u0e_WqK1vfrUwJJ4M` | Sarı | Agents | Araç Day 39–44 | [Day 98](../roadmap/day-98.md) | Planlandı / evidence yok |
| `XFy2gj7DmXeaCoc6MZo_j` | Sarı | MCP | Araç Day 39–44 | [Day 98](../roadmap/day-98.md) | Planlandı / evidence yok |
| `xL8d-uHMpJKwUvT8z-Jia` | Sarı | Skills | Araç Day 39–44 | [Day 98](../roadmap/day-98.md) | Planlandı / evidence yok |

## Desktop/Mobile hariç düğümler

| Node ID | Hariç başlık/ürün | Gerekçe |
|---|---|---|
| `VOGKiG2EZVfCBAaa7Df0W` | Mobile Apps | Kullanıcının Desktop Apps/Mobile Apps istisnası |
| `dsTegXTyupjS8iU6I7Xiv` | React Native | Kullanıcının Desktop Apps/Mobile Apps istisnası |
| `dIQXjFEUAJAGxxfAYceHU` | Flutter | Kullanıcının Desktop Apps/Mobile Apps istisnası |
| `Pxyk3nBlWbgmMjsA93E70` | Ionic | Kullanıcının Desktop Apps/Mobile Apps istisnası |
| `KMA7NkxFbPoUDtFnGBFnj` | Desktop Apps | Kullanıcının Desktop Apps/Mobile Apps istisnası |
| `mQHpSyMR4Rra4mqAslgiS` | Electron | Kullanıcının Desktop Apps/Mobile Apps istisnası |
| `GJctl0tVXe4B70s35RkLT` | Tauri | Kullanıcının Desktop Apps/Mobile Apps istisnası |
| `2MRvAK9G9RGM_auWytcKh` | Flutter | Kullanıcının Desktop Apps/Mobile Apps istisnası |

Responsive viewport/PWA testleri native mobile/desktop uygulama geliştirme değildir. Electron/Tauri/React Native/Flutter/Ionic kurulum/uygulama görevi açılmaz.

## Green seçimleri ve capability ayrımı

- Ana React portalı değiştirilmez. Angular, Vue/Nuxt, Svelte/SvelteKit, Solid ayrı aynı bounded read UI fixture'larıdır; SSR branch'leri için request-time HTML ayrıca test edilir.
- pnpm/yarn/Bun, Parcel/Rollup/SWC/Rolldown, Biome/Jest/Cypress, Relay Modern, React Router, VuePress/Eleventy ve Astro/Next static alternatif occurrence'ları gerçek ayrı output/runtime profillerine bağlıdır.
- Ana package/build/format/test/cache/resource aynı anda bütün alternatiflerin competing sahibi olmaz.
- Vercel/Netlify/Railway/Render ve Copilot/Cursor/Antigravity ücretli hizmet kullanımı zorunlu olmadan Comparison kapsamındadır. AI provider isimleri local Ollama kullanımıyla aynı literal ürün gibi sayılmaz.
- Nodejs mavi konu frontend renderer lifecycle/HTTP ve SSR üzerinden uygulanır. Node business-backend kursu/Express/Nest/business DB owner açılmaz; Java backend korunur.

## Erişim ve final gate

GitHub Pages actual ücretsiz public static deploy evidence ister; erişim yoksa gap. Cloudflare local runtime **Partial**; actual managed deploy doğrulanmadı. Önceki cloud/SaaS istisnaları korunur. Claude Code actual local tool/model çalıştırılmadan Verified olmaz.

Day 99, 72 required frontend occurrence ve beş roadmap matrisini implementation SHA, learning note, actual browser/runtime test, sürüm ve recovery evidence ile denetler. Gap/istisna/Partial/Comparison, full literal Verified sayısına karıştırılmaz. Mavi linked roadmap'in bütün alt dalları otomatik scope değildir; konu için burada tanımlı gerçek görevler esastır.
