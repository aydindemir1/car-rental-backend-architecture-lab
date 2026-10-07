# Day 63 — Federated identity, Gatekeeper ve Valet Key

Durum: **Planlandı**. Bu gün eğitim milestone'ıdır; birden fazla takvim gününe yayılabilir. Çalışan kod veya doğrulanmış sonuç henüz yoktur.

## Önkoşul ve kapsam

[Day 62](day-62.md) kapanır; önceki günün birikimli implementation snapshot'ından `day/63` türetilir. Emlak repo/planı değiştirilmez. [System Design matrisi](../coverage/system-design-coverage.md) ve [uygulama sözleşmesi](../coverage/mandatory-implementation-contract.md) esas alınır.

## Öğrenme çıktısı

Federated identity, giriş güvenlik sınırı ve kısıtlı storage erişim anahtarı için least privilege uygulamasını doğrula.

Roadmap etiketleri: `Security`, `Federated Identity`, `Gatekeeper`, `Valet Key`.

## Görevler

1. Day 38 local OIDC/SAML identity lab'ını kullan; iki local realm/IdP arasında broker/federation akışını gerçekten çalıştır. Issuer/audience/expiry validation, role mapping ve logout/session sınırını kaydet.
2. Gatekeeper'da edge request doğrulama/rate/size sınırı ve app/data network boundary uygula; internal servis authorization'ı korusun. Edge'i bypass eden direct unauthorized request negatif testi yap.
3. Valet Key için Day 60 local file service'te tek object, tek action, expiry, size/hash scope'una sahip signed URL/token üret; browser dosyayı doğrudan file service'e taşısın. Sadece sahte dosya, kısa TTL ve ayrı signer secret kullan.
4. Expired/tampered token, yanlış object/method, fazla boyut ve replay politikasını test et; tek kullanımlı gerekiyorsa durable consumption kaydı uygula. Signed URL'yi log/evidence içinde secret gibi redakte et.
5. Day 61 security alert'ine auth denial ve token abuse fixture'ını bağla; signer rotation ve credential cleanup runbook'u yaz.

## Planlanan dosyalar

- `labs/system-design/security-patterns/`
- `docs/runbooks/federation-and-valet-key.md`
- `docs/evidence/day-63/` — exact komut, sürüm, fixture, ölçüm koşulları, expected/actual ve recovery.

Bunlar implementation sırasında oluşturulacak dosya/klasörlerdir; mevcut integration kanıtı değildir.

## Commit sırası

1. `docs(day-63): gereksinim sahiplik ve failure sözleşmesini tanımla`
2. `feat(day-63): temsilî lab ve gerekli adapterları uygula`
3. `test(day-63): başarı hata ve toparlanmayı doğrula`
4. `docs(day-63): ölçüm evidence ve runbookları kapat`

Mevcut verified implementation yeterliyse aynı sorumluluk için yeni ürün/boş feat commit oluşturulmaz; gerçek evidence ve eksik testler bağlanır. Test önce correctness/hata sözleşmesini, sonra anlamlı performance hipotezini doğrular.

## Doğrulama ve kapanış

- [ ] Federation sonunda doğru principal/scope oluşur; yanlış issuer/audience ve yetkisiz edge bypass reddedilir.
- [ ] Valet Key sadece izinli object/action için çalışır; expiry/tamper/size/replay testleri ve cleanup kanıtlıdır.
- [ ] Her roadmap etiketine öğrenme + temsilî uygulama + runtime doğrulama kanıtı bağlandı; yalnız karşılaştırma tamamlanma sayılmadı.
- [ ] Yeni/değişen Java kodu için uygun build/contract/integration check başarılı; lab local runtime üzerinde çalıştırıldı.
- [ ] Kaynak limiti, stop condition, cleanup ve geri dönüş adımı kaydedildi.
- [ ] Secret/PII/gerçek ödeme bilgisi evidence'a girmedi; sürüm/lisans/uyumluluk uygulama gününde kontrol edilip pin edildi.
- [ ] Coverage gerçek duruma göre güncellendi; Planlandı/Implemented/Verified ayrımı korundu.

Ücretli AWS/Azure/GCP veya model API gerekmiyor. Yerel fault injection/replica/edge/namespace sonuçları production scale, coğrafi HA veya SLA kanıtı değildir.
