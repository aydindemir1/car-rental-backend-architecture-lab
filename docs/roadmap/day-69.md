# Day 69 — CI platformları: GitLab CI ve CircleCI kapsam sınırı

Durum: **Planlandı**. Bu gün eğitim milestone'ıdır; tek takvim günü sınırı yoktur. Plan belgesi çalışan ürün/evidence değildir.

## Önkoşul ve kapsam

[Day 68](day-68.md) kapanır; birikimli implementation snapshot'ından `day/69` türetilir. Emlak repo/85 günlük planında değişiklik yapılmaz. [DevOps ortak kararları](../DEVOPS-ROADMAP-EXTENSION.md), [kapsam matrisi](../coverage/devops-coverage.md) ve [uygulama sözleşmesi](../coverage/mandatory-implementation-contract.md) geçerlidir.

## Öğrenme ve uygulama görevleri

Roadmap etiketleri: `CI / CD Tools`, `GitHub Actions`, `GitLab CI`, `Circle CI`, `GitLab`.

1. Mevcut araç Day 34 GitHub Actions build/test ve emlak Day 66–68 Jenkins pipeline görevleri korunur. Ortak build/test contract'ını tek script/Gradle entrypoint üzerinden tanımla.
2. İzole local GitLab Community Edition + Runner kur; local lab repository'de pipeline build/test/artifact başarı ve kasıtlı failure senaryolarını gerçekten çalıştır. Bu geçici alternatif profildir; canonical GitHub repo taşınmaz.
3. Runner executor, untrusted job isolation, publishing credential scope ve protected action sınırını tanımla. Tek release'in GitHub/Jenkins/GitLab üzerinden aynı anda publish edilmesine izin verme.
4. CircleCI CLI v1 için local execute kaldırılmıştır. Config/CLI öğrenme ve validation görevi yap; YAML veya generic Docker job çalıştırmayı gerçek CircleCI pipeline diye kaydetme.
5. CircleCI'nin günü geldiğinde doğrulanan sürekli ücretsiz/ücret riski olmayan erişimi ve gerekli kullanıcı hesabı mevcutsa bir gerçek success/failure pipeline çalıştır; workflow/artifact/log evidence'ı kaydet. Erişim yoksa CircleCI ürün uygulaması açık gap kalır. Ücretli CircleCI Server, trial veya eski unsupported CLI zorunlu değildir.
6. GitHub Actions ve Jenkins'in local/self-hosted sınırları, GitLab local işletim maliyeti ve CircleCI managed çalışma farkını karşılaştır; build-once promotion korunur.

## Planlanan dosyalar

- `infra/labs/gitlab-ci/`
- `labs/ci-platforms/`
- `docs/technology/ci-platform-comparison.md`
- `docs/evidence/day-69/` — exact komut, sürüm/edition, donanım, fixture, expected/actual sonuç ve recovery.

Bu yollar aday implementation dosyalarıdır; dosyanın varlığı Integration/Verified anlamına gelmez.

## Commit sırası

1. `docs(day-69): gereksinim sahiplik ve local kapsamı tanımla`
2. `feat(day-69): temsilî operasyon lab ve adapterlarını uygula`
3. `test(day-69): başarı hata ve toparlanmayı doğrula`
4. `docs(day-69): evidence runbook ve karşılaştırmayı kapat`

Var olan verified uygulama yeterliyse tekrar ürün veya boş feat commit oluşturulmaz; mevcut SHA/evidence ve gereken yeni testler bağlanır. Engellenen SaaS/provider için karşılaştırma commit'i literal runtime uygulaması gibi adlandırılmaz.

## Doğrulama ve kapanış

- [ ] Local GitLab Runner job'u gerçek artifact üretir; failure pipeline'ı kırar; untrusted job publish secret'a erişmez.
- [ ] CircleCI full implementation ancak gerçek pipeline evidence'ıyla doğrulanır; erişim yoksa açık gap status'u audit'te korunur.
- [ ] Required başlıklara owner/öğrenme/implementation/test evidence bağlandı; engeller explicit gap veya kapsam istisnası olarak kaldı.
- [ ] Yeni/değişen kod için uygun build/contract/integration check başarılı; ardından local runtime çalıştırıldı.
- [ ] Compatibility, sürüm, ücretsiz edition/lisans ve resource bütçesi gün başında kontrol edilip pin edildi.
- [ ] İzole namespace/VM/profile sahipliği, stop condition, cleanup ve recovery kaydedildi.
- [ ] Secret/key/token/PII Git'e girmedi; untrusted CI publishing/deploy yetkisine erişmedi.
- [ ] Matris gerçek duruma güncellendi; plan veya local emulator sonucu managed-service Verified yapılmadı.

Ücretli AWS/Azure/GCP/HCP/SaaS/trial şartı yoktur; cloud hesap/kaynakları otomatik oluşturulmaz. Yerel lab gerçek production SLA, coğrafi HA veya mesleki unvan kanıtı değildir.
