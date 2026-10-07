# Araç Kiralama — Design System genişletmesi

**Planlandı.** Kullanıcının açık talebiyle [Design System roadmap](https://roadmap.sh/design-system) ayrıca iki proje kapsamıdır. Emlak 85 gün ve repo/branch/kod/doküman değişmez. Araç 131→**143 milestone**; Day 131 yedi-roadmap ara checkpoint, Day 132–142 yeni deneyler, Day 143 sekiz-roadmap final audit. Bir milestone birden fazla takvim gününe yayılabilir.

[127 eğitim düğümünün matrisi](coverage/design-system-coverage.md) ve [snapshot](coverage/design-system-roadmap-snapshot.json):9 ana,115 alt,3 roadmap kutusu. Ayrıca14 grup label bağlamı korunur. Mor/yeşil tik metadata'sı yoktur; bütün alt konular explicit task/evidence owner taşır.

## Mevcut kapsam ve seçilmiş araçlar

Day 88 design tokens, küçük component set'i, accessibility ve Web Components baseline'ı değiştirilmeden genişletilir. Day 79–98 HTML/CSS/TS/React/SSR/build/tests/performance mevcut gerçek kanıt'ı yeniden kullanılabilir; plan satırı yeterli değildir.

| Rol | Seçim | Sınır |
|---|---|---|
| Component implementation | Mevcut React/TypeScript | İş/API state owner Java/Spring'de |
| Catalog/documentation | Storybook local | Public SaaS/Chromatic zorunlu değil |
| Token build | Style Dictionary + Git JSON/CSS/TS | Tek token canonical owner; DTCG edition/tool compatibility |
| Test | Mevcut Vitest/Testing Library/Playwright + axe-core | Otomatik scan ve manuel keyboard/screen-reader ayrı |
| Design editor/UI kit | Penpot self-hosted | Local/free kararı; gerçek design+plugin lab; Figma/Sketch comparison |
| Release/operations | Mevcut Git/CI/artifact/telemetry | Aynı controller/registry owner'ını çoğaltma; public package publish gerekmez |

Penpot ücretsiz local/self-hosted sınırını karşılayan bilinçli seçimdir; Figma'nın pazar yaygınlığı hakkında kaynaksız sıralama iddiası yoktur. Aynı role alternatif editörleri zorunlu birlikte kurmayız. Ürün sürüm/API/lisans/RAM bütçesi implementation gününde kontrol edilir.

## Günlük program

| Gün | Kapsam |
|---|---|
| [132](roadmap/day-132.md) | Design System temelleri, terminoloji ve görsel audit |
| [133](roadmap/day-133.md) | Tasarım dili, marka, logo ve içerik kuralları |
| [134](roadmap/day-134.md) | Design token'ları: renk, dark mode ve layout |
| [135](roadmap/day-135.md) | Typography ve iconography sistemi |
| [136](roadmap/day-136.md) | Core components — görünüm, eylem ve metin girdileri |
| [137](roadmap/day-137.md) | Core components — seçim ve form etkileşimleri |
| [138](roadmap/day-138.md) | Core components — navigation, overlay ve feedback |
| [139](roadmap/day-139.md) | Storybook, testler, sürümleme ve katkı süreci |
| [140](roadmap/day-140.md) | Ücretsiz local design editor, plugin ve design-code traceability |
| [141](roadmap/day-141.md) | Pilot uygulama, UX, bölgesel gereksinimler ve A/B deneyi |
| [142](roadmap/day-142.md) | Design System proje yönetimi, adoption ve gözlemlenebilirlik |
| [143](roadmap/day-143.md) | Sekiz roadmap ve iki proje final kapsam audit'i |

## Öğrenme ve gerçek uygulama modeli

- Temel/terminoloji/atomic design ve actual portal visual audit; from-scratch yeni panel ve existing UI migration ayrı gerçek örnek.
- Vision/design language/tone/terminology/logo/usage/onboarding/microcopy kaynak ve browser artifact'ları.
- Functional colors/dark mode/layout/typography/iconography token pipeline ve failure/regression testleri.
- 20 core component, variant/state/role/keyboard/focus/validation ve Storybook/browser integration.
- Catalog, code style, unit/a11y/visual regression, semantic version/release/deprecation ve contribution süreçleri.
- Local editor/plugin ve design→token→code→story→artifact→consumer izlenebilirliği.
- UX journey/review/revision, tr-TR/en-US/RTL/timezone/currency, local A/B event assignment ve pilot docs.
- Adoption/build/component/service metrics ile governance/backlog/task/communication vaka çalışmaları.

Teknik konu gerçek runtime; tasarım/yönetim/communication vaka artifact+review+revision ile kapanır. A/B sentetik veri ve solo role simulation gerçek kullanıcı araştırması/ekip tecrübesi diye gösterilmez. Emlak veya mevcut araç implementation'ı yeterli doğrulanmış kanıt taşıyorsa yeniden kullanılır; eksik görev araç gününde kalır.

Day 143 sekiz explicit roadmap'in final evidence/gap raporudur. Snapshot 3 mavi link'in temsilî scope'u burada işlenir; UX roadmap'in tümünün otomatik programa alındığı iddiası yoktur. Native/Node-business-backend/paid-provider istisnaları sürer.
