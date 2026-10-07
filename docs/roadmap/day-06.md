# Day 06 — JavaScript ve React temeli

Durum: **Planlandı**. Day bir milestone'dır; takvim günü sınırı yoktur.

## Önkoşul ve scope

[Day 5](day-05.md) kapanır; cumulative implementation branch'inden `day/06` türetilir. Bu gün başka datastore'ların sahipliğini devralmaz. Ortak kararlar [Project Decisions](../PROJECT-DECISIONS.md) belgesindedir.

## Görevler

1. JavaScript async/fetch/event/storage konularını küçük uygulamayla öğren; sonra React + TypeScript kullan; Java backend dili kalır.
2. Requirement, alternatif, data/resource ownership, failure mode ve version compatibility kararını ADR'ye kaydet.
3. Mevcut dosya yapısında minimal gerçek use-case'i uygula; ihtiyaç yoksa aynı responsibility için ikinci ürün ekleme.
4. Loading/error/empty state ve başarısız API yanıtı testlerini uygula.
5. Öğrenme notunu, runbook'u, ölçüm koşullarını ve karşılaştırma sonucunu güncelle.

## Planlanan dosyalar

- `web/`
- `docs/frontend/javascript-react.md`
- `docs/evidence/day-06/` — secretsız komut, çıktı, sürüm ve ölçümler; bu yollar henüz implementation değildir.

## Commit sırası

1. `docs(day-06): scope ve sahiplik kararını tanımla`
2. `feat(day-06): temsilî çalışma ve adapterları uygula`
3. `test(day-06): başarı hata ve toparlanmayı doğrula`
4. `docs(day-06): actual evidence ve runbookları kapat`

Dosya ve sorumluluklar implementation sırasında incelenir; task yapılmadan boş commit oluşturulmaz.

## Kapanış ölçütleri

- [ ] Bu günün öğrenme konuları proje örneğiyle açıklanabiliyor.
- [ ] Gerekli build/CI başarılı; sonra local runtime/API/browser doğrulaması yapıldı.
- [ ] Yukarıdaki başarı/hata senaryoları gerçek runtime üzerinde gözlendi; expected/actual ve recovery kaydedildi.
- [ ] Secret/PII/anahtar ve gerçek ödeme bilgisi Git/evidence içine girmedi.
- [ ] Sürüm/lisans/uyumluluk ve RAM/CPU/disk bütçesi kaydedildi.
- [ ] İki proje coverage satırları gerçek duruma göre güncellendi; kanıt olmadan Verified işaretlenmedi.

Yerel emulator, benchmark ve toy lab sonucu production SLA/HA/scale kanıtı değildir. Ücretli cloud/model API zorunluluğu yoktur.


## Full Stack ek görevi — npm ve frontend uygulama checkpoint'i

1. npm/package manifest, dependencies/devDependencies, semantic version ranges, lockfile, scripts ve package lifecycle kavramlarını öğren; client/server package farkını açıkla.
2. Seçilmiş bir external frontend package'ı gerçek form/route/use-case içinde kullan; lisans ve güvenlik/supply-chain kontrolünü kaydet. Paket sayısını artırmak amaç değildir.
3. `npm ci`, build/test/lint script'leri ve clean checkout yeniden üretimini doğrula; lockfile mismatch/missing dependency testini yap. Lockfile tek başına byte-identical artifact garantisi değildir.
4. React component/props/state, controlled form, route navigation, async cancellation, loading/error/empty state görevlerini açıkla ve uygula. Browser'da JS gerçek interactivity fixture'ı da göster.
5. Dev dependency ve frontend build tooling için gereken Node executable yalnız local araçtır. Node.js backend, Express/Nest veya ayrı server-side JS servis scope'u yoktur; deploy edilen statik portal Nginx'ten sunulur.

Aday çıktılar: `web/package.json`, `web/package-lock.json`, `docs/frontend/npm-package-management.md`. Commit: `build(frontend): npm lockfile ve tekrar üretilebilir frontend görevlerini kur`.
