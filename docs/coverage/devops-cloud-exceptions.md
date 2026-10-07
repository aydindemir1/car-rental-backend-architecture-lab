# DevOps — Yerel ortam, provider ve ürün erişim sınırları

Karar tarihi: 2026-10-07. Bu belge önceki **ücretsiz local/self-hosted** çalışma kararını korur; ücretli cloud/HCP/SaaS/trial gerektirmez. Emlak planında değişiklik yoktur. [DevOps matrisi](devops-coverage.md) kapsamın tamamlanmadığı literal ürünleri saklamaz.

| Roadmap satırı | Program görevi | Kapanış sınırı |
|---|---|---|
| Cloud Providers / AWS / Azure / Google Cloud | Day 76 provider model/shared responsibility/IAM/network/storage tasarımı ve local karşılık deneyi | Actual provider runtime **açık kapsam istisnası**; tasarım veya local K8s provider implementation değildir |
| AWS Lambda | Day 75 Java handler + AWS SAM Docker local invoke/start-api | Local emülatör/runtime lab'ı; gerçek AWS IAM/integration/managed operasyon **uygulanmadı** |
| Cloudflare | Day 75 Wrangler/workerd local Workers fixture | Local Workers runtime; gerçek Cloudflare edge deployment/DNS/managed servis **uygulanmadı** |
| Circle CI | Day 69 config/CLI; ancak ücretsiz ve ücret riski olmayan kullanıcı erişimi varsa real managed pipeline | CLI v1 local execute kaldırıldı. Validation/generic Docker job full CircleCI execution değildir; erişim yoksa **açık gap** |
| Datadog (mor ve yeşil occurrence) | Day 73 ürün modeli; isteğe bağlı local agent; ücretsiz/ücret riski olmayan erişim varsa actual monitor/alert | Local agent metric kabulü Datadog SaaS backend/dashboard değildir; erişim yoksa **açık gap** |
| Artifactory | Day 71 güncel ücretsiz uygun OSS distribution gate, local Java publish/resolve | Erişim/licence/support uygun değilse **açık gap**; ücretli edition/trial zorunlu değil |

## Statü kuralları

- Comparison/Design Only: belge ve requirement değerlendirmesi; runtime implementation sayılmaz.
- Local Lab / Partial: resmi araç veya emülatörün açık sınırdaki local davranışı gerçekten çalıştırılmıştır; managed hizmet doğrulanmamıştır.
- Açık gap: istenen literal ürün evidence'ı yok; owner ve çözüm/erişim işi programda vardır.
- Açık kapsam istisnası: önceki local/no-cloud sınırıyla real provider runtime bu çalışma kapsamında yapılmaz. Required graph satırı envanterden silinmez.
- Verified: yalnız hangi capability'nin, hangi runtime'ın ve hangi success/failure/recovery testinin kanıtlandığı açıkça belirtilir. “Datadog agent verified” ile “Datadog SaaS monitoring verified” farklıdır.

## Günü geldiğinde yapılacaklar

Önce resmi sürüm/license/ücretsiz erişim şartlarını kontrol et. Hesap/credential veya ücretli/trial erişimi otomatik oluşturma; kullanıcı erişimi varsa ve ücret riski olmayan scope doğrulanmışsa explicit program sınırındaki testi çalıştır. Uygun ücretsiz erişim yoksa gap'i doğru raporla; eski unsupported CLI veya alternate ürünü aynı literal ürün gibi kullanma.

Cloud provider kullanımını daha sonra aktive etmek ayrı kapsam kararıdır. Bu plan bütün provider ürünlerinin ellerle uygulanmış olacağını garanti etmez. Eğitim kapsamı, runtime evidence ve istisna/gap sayıları Day 99 raporunda ayrı yazılır.

## Resmi kaynaklar

- [CircleCI CLI migration](https://circleci.com/docs/guides/toolkit/cli-migration-guide/) — local job execution v1'de kaldırılmıştır.
- [Datadog plan ve usage](https://docs.datadoghq.com/account_management/plan_and_usage/) — post-trial kullanımın ücretli olabilmesi; trial programın ücretsiz garanti yolu değildir.
- [Cloudflare local development](https://developers.cloudflare.com/workers/local-development/)
- [AWS SAM local](https://docs.aws.amazon.com/serverless-application-model/latest/developerguide/using-sam-cli-local.html)
- [Artifactory OSS](https://jfrog.com/community/download-artifactory-oss/)


## Frontend fazı sonrası audit geçişi

[Frontend kapsamı](frontend-coverage.md) yeni kullanıcı talebiyle eklenmiştir. Day 78 dört roadmap ara checkpoint olarak korunur; Day 99 beş roadmap nihai audit'idir. Önceki cloud/SaaS erişim ve ownership sınırları korunur.
