# Day 44 — Tool calling, MCP ve agents

Durum: **Planlandı**. Day bir milestone'dır; takvim günü sınırı yoktur.

## Önkoşul ve scope

[Day 43](day-43.md) kapanır; cumulative implementation branch'inden `day/44` türetilir. Bu gün başka datastore'ların sahipliğini devralmaz. Ortak kararlar [Project Decisions](../PROJECT-DECISIONS.md) belgesindedir.

## Görevler

1. Read-only availability/pricing tools + Spring AI MCP server/client kur; allowlist, principal propagation, deterministic tool validation ve bounded agent loop kullan.
2. Requirement, alternatif, data/resource ownership, failure mode ve version compatibility kararını ADR'ye kaydet.
3. Mevcut dosya yapısında minimal gerçek use-case'i uygula; ihtiyaç yoksa aynı responsibility için ikinci ürün ekleme.
4. Tool misuse, unauthorized read ve loop limits test; booking/payment gibi mutation explicit user confirmation ve canonical service checks gerektirir.
5. Öğrenme notunu, runbook'u, ölçüm koşullarını ve karşılaştırma sonucunu güncelle.

## Planlanan dosyalar

- `services/rental-assistant/`
- `docs/ai/tools-mcp-agents.md`
- `docs/evidence/day-44/` — secretsız komut, çıktı, sürüm ve ölçümler; bu yollar henüz implementation değildir.

## Commit sırası

1. `docs(day-44): scope ve sahiplik kararını tanımla`
2. `feat(day-44): temsilî çalışma ve adapterları uygula`
3. `test(day-44): başarı hata ve toparlanmayı doğrula`
4. `docs(day-44): actual evidence ve runbookları kapat`

Dosya ve sorumluluklar implementation sırasında incelenir; task yapılmadan boş commit oluşturulmaz.

## Kapanış ölçütleri

- [ ] Bu günün öğrenme konuları proje örneğiyle açıklanabiliyor.
- [ ] Gerekli build/CI başarılı; sonra local runtime/API/browser doğrulaması yapıldı.
- [ ] Yukarıdaki başarı/hata senaryoları gerçek runtime üzerinde gözlendi; expected/actual ve recovery kaydedildi.
- [ ] Secret/PII/anahtar ve gerçek ödeme bilgisi Git/evidence içine girmedi.
- [ ] Sürüm/lisans/uyumluluk ve RAM/CPU/disk bütçesi kaydedildi.
- [ ] İki proje coverage satırları gerçek duruma göre güncellendi; kanıt olmadan Verified işaretlenmedi.

Yerel emulator, benchmark ve toy lab sonucu production SLA/HA/scale kanıtı değildir. Ücretli cloud/model API zorunluluğu yoktur.


## Skills ve agent uygulama kanıtı

Bir rental-policy/read-only tool kullanım skill'i oluştur: giriş/çıkış şeması, allowed tools, kullanıcı kapsamı, yetki sınırı, retry ve durma koşulları version-controlled olur. Agent bu skill'i gerçek görevde kullanır. Yanlış tool argümanı, yetkisiz kullanıcı, prompt injection, sonsuz döngü ve model outage testleri uygulanır. MCP server ve client temsilî uçtan uca çağrıyla doğrulanır; yalnız dependency eklemek yeterli değildir. Dosyalar: `docs/ai/skills/rental-policy.md`, `labs/ai-agents/`. Human approval gerektiren domain mutation read-only skill'e sızmaz.
