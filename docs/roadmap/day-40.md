# Day 40 — AI destekli geliştirme

Durum: **Planlandı**. Day bir milestone'dır; takvim günü sınırı yoktur.

## Önkoşul ve scope

[Day 39](day-39.md) kapanır; cumulative implementation branch'inden `day/40` türetilir. Bu gün başka datastore'ların sahipliğini devralmaz. Ortak kararlar [Project Decisions](../PROJECT-DECISIONS.md) belgesindedir.

## Görevler

1. Claude Code CLI'yi resmi dağıtımından kur; Ollama local endpoint + tool calling destekli yerel model ile bağla; code review/refactoring/docs generation görevlerini tests/diff review ile değerlendir.
2. Requirement, alternatif, data/resource ownership, failure mode ve version compatibility kararını ADR'ye kaydet.
3. Mevcut dosya yapısında minimal gerçek use-case'i uygula; ihtiyaç yoksa aynı responsibility için ikinci ürün ekleme.
4. Human baseline vs assisted output, injected bad suggestion ve recovery testlerini Claude Code üzerinde gerçekten çalıştır; ücretli account/model API veya cloud fallback kullanma.
5. Öğrenme notunu, runbook'u, ölçüm koşullarını ve karşılaştırma sonucunu güncelle.

## Planlanan dosyalar

- `docs/ai/assisted-development.md`
- `labs/ai-coding/`
- `docs/evidence/day-40/` — secretsız komut, çıktı, sürüm ve ölçümler; bu yollar henüz implementation değildir.

## Commit sırası

1. `docs(day-40): scope ve sahiplik kararını tanımla`
2. `feat(day-40): temsilî çalışma ve adapterları uygula`
3. `test(day-40): başarı hata ve toparlanmayı doğrula`
4. `docs(day-40): actual evidence ve runbookları kapat`

Dosya ve sorumluluklar implementation sırasında incelenir; task yapılmadan boş commit oluşturulmaz.

## Kapanış ölçütleri

- [ ] Bu günün öğrenme konuları proje örneğiyle açıklanabiliyor.
- [ ] Gerekli build/CI başarılı; sonra local runtime/API/browser doğrulaması yapıldı.
- [ ] Yukarıdaki başarı/hata senaryoları gerçek runtime üzerinde gözlendi; expected/actual ve recovery kaydedildi.
- [ ] Secret/PII/anahtar ve gerçek ödeme bilgisi Git/evidence içine girmedi.
- [ ] Sürüm/lisans/uyumluluk ve RAM/CPU/disk bütçesi kaydedildi.
- [ ] İki proje coverage satırları gerçek duruma göre güncellendi; kanıt olmadan Verified işaretlenmedi.

Yerel emulator, benchmark ve toy lab sonucu production SLA/HA/scale kanıtı değildir. Ücretli cloud/model API zorunluluğu yoktur.


## Zorunlu Claude Code uygulaması

- [Ollama resmî Claude Code entegrasyonu](https://docs.ollama.com/integrations/claude-code) esas alınır. Yerel model, context ve RAM bütçesi pin edilir; CLI için açık kaynak lisansı varsayılmaz.
- Day 40'ta önce local Ollama/model bootstrap tamamlanır; Day 41 aynı foundation'ı Spring AI uygulamasına bağlar. Sonraki güne ait çalışan servis önkoşulu yaratılmaz.
- Backend ve model isteklerinin yalnız yerel endpoint'e gittiği doğrulanır; cloud model suffix'i ve hosted web-search bu zorunlu local deneyde kullanılmaz.
- Aynı küçük değişiklik için manuel baseline ve Claude Code review/refactor/documentation çıktıları karşılaştırılır; diff, test sonucu, süre ve yanlış öneri kaydedilir.
- Agent shell/file izinleri sınırlandırılır; permission bypass varsayılan değildir. Destructive veya domain mutation önerisi otomatik yürütülmez.
- Exact version/resource/support nedeniyle çalıştırılamazsa “açık uygulama gap” bırakılır; başka agent veya comparison belgesi Claude Code satırını kapatmaz.

Ek dosyalar: `docs/ai/claude-code-local.md`, `labs/ai-coding/claude-code/`. Ek commit: `test(ai-coding): Claude Code yerel model görevlerini ve network sınırını doğrula`.
