# Day 98 — Frontend AI, prompting, MCP, skills ve agents

Durum: **Planlandı**. Bu eğitim milestone'ı birden fazla takvim gününe yayılabilir. Kod/runtime evidence henüz oluşturulmadı.

## Önkoşul ve kapsam

[Day 97](day-97.md) kapanır; önceki birikimli implementation snapshot'ından `day/98` türetilir. Emlak repo/85 günlük planı değişmez. [Frontend ortak planı](../FRONTEND-ROADMAP-EXTENSION.md), [coverage matrisi](../coverage/frontend-coverage.md) ve [uygulama sözleşmesi](../coverage/mandatory-implementation-contract.md) esas alınır.

Desktop Apps/Mobile Apps ve ilgili native framework/runtime'lar kapsam dışıdır. Web PWA ve responsive browser deneyleri kapsamda kalır. Java/Spring business backend ve canonical veri sahipliği korunur.

## Öğrenme ve uygulama görevleri

Roadmap etiketleri: `Learn the Basics`, `How LLMs work`, `AI vs Traditional Coding`, `AI Assisted Coding`, `Claude Code`, `Code Reviews`, `Docs Generation`, `Refactoring`, `Prompting Techniques`, `Prompt Engineering`, `Implementing AI`, `Applications`, `Agents`, `MCP`, `Skills`, `AI Agents Roadmap`.

1. Day 39–44 local Ollama/Spring AI/Claude Code görevlerini frontend UI üzerinden evidence ile kullan; model/API erişimi olmayan ürün Comparison ile zorunlu tamamlandı yapılmaz.
2. LLM çalışma mantığı, token/context, hallucination, prompt/grounding ve evaluation konularını örnek frontend task'ında ölç; AI vs traditional workflow farkını kaydet.
3. Claude Code + local model ile bounded component refactor, code review ve docs generation yap; developer review ve Vitest/Playwright doğrulaması olmadan değişikliği güvenilir sayma.
4. Java/Spring AI local API'dan browser streaming UI kur; cancellation, malformed output, latency, fallback ve accessible status/error feedback testlerini uygula.
5. MCP için restricted read-only schema/docs tool; Skills için reusable task yönergesi; Agent için bounded step/budget, approval boundary ve audit trail uygula. Agent credential/booking mutation yetkisi varsayılmaz.
6. Prompt injection, untrusted tool output, context/data leakage ve denied action testlerini yap. Copilot/Cursor/Antigravity/Gemini/OpenAI/Anthropic ürünleri paid API gerektirmeyen karşılaştırma kapsamıdır.

## Planlanan dosyalar

- `labs/frontend/ai-workflow/`
- `docs/frontend/ai-evaluation-and-tool-boundaries.md`
- `docs/evidence/day-98/` — sürüm/edition, exact komut, browser/runtime, fixture, expected/actual, ölçüm ve recovery.

Bunlar aday implementation çıktılarıdır; dosya/dependency varlığı Verified değildir.

## Commit sırası

1. `docs(day-98): frontend gereksinim ve sınırları tanımla`
2. `feat(day-98): temsilî UI ve eğitim profillerini uygula`
3. `test(day-98): browser contract hata ve toparlanmayı doğrula`
4. `docs(day-98): evidence runbook ve karşılaştırmayı kapat`

Mevcut verified uygulama yeterliyse aynı sorumluluğu tekrar kurma/boş feat commit üretme; actual SHA/evidence ve eksik testleri bağla. Green ürün profilleri ana app'in aynı state/build/controller kaynağına competing owner olmaz.

## Doğrulama ve kapanış

- [ ] AI task actual local tool/model çağrısı, developer review ve regression evidence'ına sahiptir.
- [ ] Streaming/cancel/injection/denied-tool davranışı gerçek UI/API'da gözlenir; secrets veya kullanıcı verisi modele gönderilmez.
- [ ] Konu/product/blue etiketleri öğrenme + gerçek temsilî uygulama + runtime evidence ile veya explicit erişim gap'inde izleniyor.
- [ ] Değişen kod için uygun type/lint/unit/integration/build check; ardından gerçek browser/API/local runtime doğrulaması yapıldı.
- [ ] Accessibility, auth/privacy, cancellation/cleanup ve bounded resource davranışı ilgili use-case'te test edildi.
- [ ] Sürüm/lisans/compatibility gün başında doğrulanıp pin edildi; source maps/env/artifact secret sızdırmıyor.
- [ ] Local/managed provider, mock/real API ve CSR/SSR/SSG/PWA kanıtları ayrı raporlandı.
- [ ] Coverage actual duruma güncellendi; yalnız comparison veya static export SSR implementation sayılmadı.

Ücretli cloud/model API/hosting zorunluluğu yoktur; hesap/billing/remote deployment bugün yapılmaz. Local lab production SLA/scale, arama sıralaması veya mesleki unvan kanıtı değildir.
