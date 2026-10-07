# Repository ve branch çalışma düzeni

[Repository](https://github.com/aydindemir1/car-rental-backend-architecture-lab) kullanıcı tarafından 2026-10-07 tarihinde public olarak oluşturuldu. Başlangıç içeriği eğitim programı ve kapsam belgeleridir; uygulama kodu henüz yoktur.

## Branch sahipliği

- `main`: başlangıç dokümantasyon baseline'ı; tamamlanan uygulamalar ancak ayrı kararla buraya alınır.
- `docs/car-rental-roadmap-design`: canonical plan/program ve kapanan günlerin birikimli belgeleri.
- `day/NN`: önceki kapanmış implementation gününün birikimli snapshot'ından türetilen çalışma branch'i. Day 01 başlangıç baseline'ından başlar.

Her gün yalnız ilgili çalışma branch'i ve canonical dokümantasyon branch'i güncellenir. Eski gün branch'lerine sonraki günlerin kodu taşınmaz. Küçük ve anlamlı commit'ler kullanılır; unrelated sorumluluklar tek commit'e alınmaz.

## Doğrulama sırası

Önce ilgili build/CI başarılı olur, sonra yerel runtime/API/browser testleri yapılır. Ardından secretsız evidence, ADR, runbook, servis belgeleri ve Knowledge Base etki incelemesi gerçek uygulamaya göre kapatılır. Planlandı durumundaki yetenekler bu başlangıç yayınıyla Implemented veya Verified olmaz.

Mevcut içerik önce okunup karşılaştırılmadan değiştirilmez; force push kullanılmaz. Emlak projesinin 85 günlük programı bu repo çalışması kapsamında değiştirilmez.
