# Car Rental Backend Architecture Lab

Araç kiralama domain'inde **öğrenme ve uygulama amaçlı Full Stack + backend/architecture + DevOps laboratuvarı**. Ana eksen Java, Spring Boot, Spring Cloud, Docker ve Kubernetes'tir.

Bu repo [Real Estate Backend Architecture Lab](https://github.com/aydindemir1/real-estate-backend-architecture-lab/tree/docs/backend-roadmap-design) 85 günlük programının devamı değil, tamamlayıcı ikinci projedir. Emlak projesi büyütülmez. İki projede roadmap.sh/backend'in belirlenmiş snapshot kapsamını kanıtla karşılamak amaçlanır.

**Mevcut durum: Planlandı / documentation foundation.** Çalışan kiralama sitesi, datastore integration veya runtime evidence henüz yoktur. Dosya/commit planları gerçek uygulama ile güncellenmeden tamamlandı sayılmaz.

- [Ana program](ROADMAP.md) ve [48 milestone ayrıntısı](docs/roadmap/README.md)
- [Proje kararları](docs/PROJECT-DECISIONS.md)
- [Domain ve veri sahipliği](docs/architecture/domain-and-data.md)
- [İki proje coverage matrisi](docs/coverage/two-project-coverage.md)
- [Sarı/mor/mavi başlıklar](docs/coverage/required-topics.md)
- [Seçilmiş alternatifler](docs/technology/alternatives.md)
- [Kaynaklar ve sürüm politikası](docs/REFERENCES.md)

## Planlanan use-case'ler

Araç/şube arama; fiyat teklifi; çakışmasız rezervasyon; teslim/iade; telemetri; utilization/gelir raporu; durum panosu; policy/FAQ AI asistanı. Gerçek ödeme, kimlik belgeleri ve dış araç telematiği başlangıç scope'unda değildir.

## Temel sınırlar

Ücretli AWS/Azure/GCP, model API veya domain satın alma zorunluluğu yok. Firebase yalnız local emulator'dür. Java backend dili; React/TypeScript frontend dili. Datastore'lar kendi requirement'ını karşılar, bir rezervasyon state'i birden fazla store'un canonical verisi olmaz. Senior/staff/principal öğrenme hedefi gerçek saha tecrübesi veya unvanın yerine geçmez.
