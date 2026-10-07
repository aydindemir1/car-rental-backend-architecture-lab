# Araç Kiralama — Frontend genişletme programı

**Planlandı.** [Frontend matrisi](coverage/frontend-coverage.md) ve [snapshot](coverage/frontend-roadmap-snapshot.json) kullanıcı talebiyle programa dahil. **Desktop Apps ve Mobile Apps hariç.** Emlak 85 gün değişmez; araç programı yeni mimari fazıyla 117 milestone'dır. Bir milestone birden fazla takvim gününe yayılabilir.

## Amaç ve mimari sınır

HTML/CSS/JavaScript/TypeScript, browser platformu, farklı frontend/rendering yaklaşımları, testing/security/accessibility/performance ve AI ile gerçek eğitim yapmak. Ana portal React/TypeScript; Java/Spring Boot/Spring Cloud business backend ve canonical datastore/messaging ownership korunur.

Day 06/45 CSR portalı Nginx'ten sunulmaya devam eder. Yeni Frontend scope'unda Next/TanStack Start ve seçilmiş alternatif SSR için Node frontend renderer profili vardır. Bu ayrı presentation role'ü önceki Node business-backend eğitim istisnasını kaldırmaz; Express/Nest/business persistence/booking correctness Node'a taşınmaz. Önceki “tooling only” static-faz sınırı yeni scoped SSR role ile birlikte okunur. Mavi Nodejs burada process/env/module/event-loop/HTTP/lifecycle/render görevleriyle öğrenilir; bütün Node roadmap'i otomatik scope olmaz.

PWA browser/web kapsamıdır; native Mobile/Desktop Apps kapsamı açılmaz. Responsive/mobile viewport testleri yapılabilir; Electron/Tauri/React Native/Flutter/Ionic implementation görevleri yoktur.

## Seçimler ve ayrı eğitim profilleri

| Sorumluluk | Ana seçim | Ek gerçek deney / sınır |
|---|---|---|
| UI | React/TypeScript | Angular, Vue/Nuxt, Svelte/SvelteKit, Solid küçük ayrı read UI |
| Styling | CSS + Tailwind | Token/component design system ve plain CSS fixture |
| Package manager | npm | pnpm/yarn/Bun ayrı fixture/lockfile; main tek owner |
| Build | Vite | Direct esbuild; Parcel/Rollup/SWC; actual Rolldown usage |
| Lint/format | ESLint + Prettier | Biome ayrı profile; main çift formatter yok |
| Testing | Vitest + Playwright | Jest/Cypress ayrı bounded failure contract testleri |
| Web platform | HTML/DOM/Web APIs | Custom Elements/Templates/Shadow DOM gerçek React integration |
| GraphQL | Java API + Apollo | Relay compiler/client ayrı read fixture |
| SSR | Next.js ve TanStack Start ayrı profiller | Java read API, request-time HTML/hydration; Node presentation only |
| SSG | Astro | Next export, Eleventy, VuePress, Nuxt generate; statik içerik freshness ayrı |
| Web offline | PWA/Service Worker/IndexedDB draft | Canonical booking offline kesinleşmez |
| Deploy | Local Nginx/Docker/release pipeline | Pages actual ücretsiz public fake demo; Cloudflare local Partial |
| AI | Local Ollama/Spring AI/Claude Code | Frontend stream/eval/MCP/skills/bounded agent; paid provider şart değil |

## Günlük sıra

| Day | Milestone |
|---|---|
| [79](roadmap/day-79.md) | Internet, semantic HTML ve erişilebilirlik temeli |
| [80](roadmap/day-80.md) | CSS, responsive layout ve Tailwind |
| [81](roadmap/day-81.md) | JavaScript ve browser Web APIs |
| [82](roadmap/day-82.md) | TypeScript ve runtime contract sınırları |
| [83](roadmap/day-83.md) | React uygulama mimarisi ve route/state tasarımı |
| [84](roadmap/day-84.md) | npm, pnpm, yarn ve Bun paket deneyleri |
| [85](roadmap/day-85.md) | Vite, esbuild ve bundler/compiler lab'ı |
| [86](roadmap/day-86.md) | ESLint, Prettier ve Biome kalite gate'leri |
| [87](roadmap/day-87.md) | Vitest, Playwright ve test alternatifleri |
| [88](roadmap/day-88.md) | Design System ve Web Components |
| [89](roadmap/day-89.md) | Frontend authentication ve web security |
| [90](roadmap/day-90.md) | GraphQL: Apollo ve Relay Modern |
| [91](roadmap/day-91.md) | Next.js ile gerçek SSR ve Node render sınırı |
| [92](roadmap/day-92.md) | TanStack Start ile SSR/streaming karşılaştırması |
| [93](roadmap/day-93.md) | Astro, SSG ve statik içerik modelleri |
| [94](roadmap/day-94.md) | Frontend performance, cache ve Lighthouse |
| [95](roadmap/day-95.md) | PWA, service worker ve offline taslaklar |
| [96](roadmap/day-96.md) | Frontend deployment ve hosting kapsamı |
| [97](roadmap/day-97.md) | Yeşil frontend framework alternatifleri |
| [98](roadmap/day-98.md) | Frontend AI, prompting, MCP, skills ve agents |
| [99](roadmap/day-99.md) | Beş roadmap ve iki proje final audit |

Day 79–98 programın yeni eğitim deneyleri; Day 99 önceki beş roadmap ara checkpoint. Day 48/64/78 önceki scope checkpoint'leri olarak kalır.

## Kapanış standardı

- Gereksinim/threat model ve ADR; owner/component/runtime boundary; meaningful success/failure/recovery tests; build/CI; actual local browser/API; redakte evidence/runbook sırası izlenir.
- CSR/SSR/SSG/PWA ve framework/product-specific capability ayrı doğrulanır; static export SSR diye, dependency ürünü uygulandı diye gösterilmez.
- Actual API testleri ile fake/mocked dataset testleri ayrı raporlanır. Browser UI client guard Java authorization yerine geçmez.
- Cancellation/cleanup, cache/private data, accessibility ve resource bütçesi her ilgili use-case'te değerlendirilir. Automatic a11y/Lighthouse score tek başına production uygunluk/field performance kanıtı değildir.
- Ücretsiz local hosting/model/platform kararı korunur. Account/billing/ücretli/trial erişimi otomatik oluşturulmaz; actual managed deployment yoksa product gap/Partial korunur.
- Versiyon/lisans/security/compatibility uygulama gününde kontrol edilip pin edilir; özellikle Vite actual bundler, SSR adapter ve AI client/model tool capability doğrulanır.


## Software Architect fazı sonrası nihai gate

[Software Architect kapsamı](coverage/software-architect-coverage.md) eklendi. Day 99 önceki beş roadmap ara checkpoint; Day 117 altı roadmap final audit. Önceki teknik profiller, erişim ve ownership sınırları korunur; runtime ve case validation ayrı raporlanır.
