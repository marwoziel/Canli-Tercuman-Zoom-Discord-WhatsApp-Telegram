# Güvenlik incelemesi — 1 Kasım 2026

**Durum: İnceleme açık. İndirmeler askıda. Bu belge güvenlik sertifikası değildir.**

## Bildirilen dosya

CanliTercuman-Setup-1.1.0.exe  
SHA256: `fa035d5794ae0277c130a1ca77324e01f402d7d2a5ecd6be9183eaed0acd665a`

Kullanıcının VirusTotal ekran görüntüsünde Microsoft `Trojan:Win32/Wacatac.C!ml` dahil birden fazla tespit var. Ekrandaki dosya hash'i yayımlanan dosyayla eşleşiyor. Kullanıcı dört dosyanın VirusTotal sonuç ekranlarını paylaştı; aşağıdaki tablo bu ekranlardan kaydedildi. Mevcut tespitler yanlış alarm olarak doğrulanmadı.

## 2 Kasım 2026 güncellemesi: dört dosyanın sonucu

| Dosya | Tespit / değerlendirilen motor | Rapor |
|---|---|---|
| 1.1.0 Kurulum | 7/57 | [SHA256 raporu](https://www.virustotal.com/gui/file/fa035d5794ae0277c130a1ca77324e01f402d7d2a5ecd6be9183eaed0acd665a) |
| 1.1.0 İç uygulama | 3/71 | [SHA256 raporu](https://www.virustotal.com/gui/file/c7a0a79907a2732595e2242147ce9d0dd18a06119a4ecc1f72231576f5813b25) |
| 1.1.1 Kurulum | 6/70 | [SHA256 raporu](https://www.virustotal.com/gui/file/0659564463610fa29bda1ed6dba4e5f06b61f645b021093232032221baa7fa7f) |
| 1.1.1 İç uygulama | 3/71 | [SHA256 raporu](https://www.virustotal.com/gui/file/96470a451be90a032b7abdb6a6fd5fd859c91a09d87492c1581920157b7d5a1a) |

İki iç uygulamada da Arctic Wolf (`Unsafe`), SecureAge (`Malicious`) ve Skyhigh (`BehavesLike.Win64.Backdoor.vc`) tespiti görünüyor. Dolayısıyla uyarı sadece kurucuyla sınırlı değil. Bunlar kullanıcı ekranlarından alınan sonuçlardır; API üzerinden tüm davranış raporu okunmadı. Motor sayıları ve analiz zamanları farklıdır; 7'den 6'ya düşüş bir güvenlik düzeltmesinin doğrulandığı anlamına gelmez.

**Yayın kararı:** Tüm EXE sürümleri taslakta kalır. Tespit veren üreticilerin değerlendirmesi ve aynı dosya hash'iyle doğrulama olmadan güvenli sürüm duyurusu yapılmaz.

## Tamamlanan kontroller

| Kontrol | Sonuç ve kapsam |
|---|---|
| Güncellenmiş yerel Defender | 1.1.0 kurucu ve tam içeriği, 1.1.1 kurucu ve tam içeriği, uygulama kaynakları: tehdit bulunmadı; özel tarama dönüş kodu 0. Bu sonuç diğer motorların tespitlerini geçersiz kılmaz. |
| Resmî bağımlılık eşleşmesi | 25 dağıtım, güncelleme sonrası 5847 dosya: PyPI wheel içerikleriyle eşleşti. Wheel SHA256 değerleri PyPI metadata ile doğrulandı. |
| Kurucu içeriği | Her iki sürümün kurucusundaki 453'er dosya, karşılık gelen tutulan uygulama klasörüyle birebir eşleşti. |
| Derlenmiş kendi modüllerimiz | İki sürümde 14'er modülde sabit ağ adresleri incelendi: Deepgram, Groq, ElevenLabs, VB-Audio adresleri. Bu statik kontrol tüm olası davranışların analizi değildir. |
| İmza kontrolü | Python çalışma zamanı: Python Software Foundation; C# derleyicisi: Microsoft; indirilen VB-Cable kurucusu: BUREL VINCENT. İmzalar geçerli. Kendi uygulama/kurucu EXE'lerimiz imzasız. |
| Bilinen bağımlılık açıkları | OSV sorgusunda uygulama bağımlılıkları için kayıt dönmedi. Eski derleme araçları pip/setuptools için kayıtlar çıktı; bunlar dağıtılan uygulamanın içinde bulunmuyor. Araçlar güncellendi ve yeni sürümlerde OSV kayıt döndürmedi. Bu tarama tüm yerel/native kütüphane açıklarını kapsamaz. |
| İşlev ve güvenlik regresyonları | 120 test geçti. Testlerin geçmesi zararlı yazılım bulunmadığı garantisi değildir. |

## Yapılan güvenlik iyileştirmeleri

Derleme ortamında pip 26.2.2 ve setuptools 84.2.1 kullanılıyor. Kaynak sürümde resmî VB-Cable ZIP paketi için sabit SHA256 kontrolü ve UAC öncesi 64 bit kurucu dosyasının yeniden hash kontrolü eklendi. Değiştirilmiş arşiv kurulum öncesinde, değiştirilmiş EXE çalıştırılmadan reddedilir. İncelenen resmî sürücü paketi kontrolü geçti. Bu değişiklikler henüz yeni bir genel dağıtım olarak yayımlanmadı.

## Uyarının nedeni

Kesin neden henüz belirlenmedi. İmzasız, ZIP yükü taşıyan özel .NET kurucu ve içindeki PyInstaller uygulaması sezgisel/makine öğrenmesi tespitleri açısından incelenmesi gereken bileşenler. PyInstaller, bu tür tespitlerde antivirüs üreticisine dosya incelemesi gönderilmesini öneriyor: [resmî açıklama](https://github.com/pyinstaller/pyinstaller/issues/6062). Bu genel açıklama, bu dosyanın yanlış alarm olduğunu kanıtlamaz.

## Açık kalan işlemler

- Tespit veren motorların tam davranış bulguları ve üretici inceleme kararları. Dört EXE için kullanıcı tarafından paylaşılan tespit sonuçları yukarıdadır.
- Microsoft ve tespit veren üreticilerin dosya/ilgili davranış incelemesi.
- Yeni sürüm yayımlanmadan önce sonuçların dosya hash'i ve tarama tarihiyle belgelenmesi.

Orijinal dosyaları içeren üretici inceleme paketi ve İngilizce açıklama yerelde hazırlandı. Henüz bir üreticiye gönderildiği veya onay alındığı iddia edilmiyor. Antivirüs kapatma, istisna ekleme veya uyarıları aşma önerilmiyor.

## 1.1.2 sonucu — güvenlik onayı verilmedi

2 Kasım 2026 tarihinde kullanıcı tarafından paylaşılan ekranlarda kurucu **6/69**, iç uygulama **6/71** tespit aldı. Önceki yerel Defender sonucuna rağmen bu aday da güvenli sürüm olarak kabul edilmedi; dağıtıma açılmadı.

- 05_Kurulum_1.1.2_TEST.exe: [6/69 raporu](https://www.virustotal.com/gui/file/fd53d506bd4990862e7b91da347e13ed7cf79439e3140d120615fd6d1c4cbd0e). SHA256: `fd53d506bd4990862e7b91da347e13ed7cf79439e3140d120615fd6d1c4cbd0e`.
- 06_Uygulama_1.1.2_TEST.exe: [6/71 raporu](https://www.virustotal.com/gui/file/b30c21bc991d30bba61dd193a9fc743a2c4ee28be52a9928e78bbeee50f53d62). SHA256: `b30c21bc991d30bba61dd193a9fc743a2c4ee28be52a9928e78bbeee50f53d62`.

1.1.1 ile 1.1.2 arşivlerinin karşılaştırılması, modül sayısının 548'den 755'e çıktığını gösterdi. Derleme araçlarının güncellenmesiyle setuptools/distutils ve bağlı modüller 1.1.2 çalışma paketine de dahil edilmiş. Önceki “derleme araçları dağıtılan EXE içinde yok” bulgusu yalnızca incelenmiş 1.1.0/1.1.1 için geçerlidir; 1.1.2 için geçerli değildir. Bu değişikliğin antivirüs tespitlerine neden olduğu kanıtlanmış değildir.

Sürücü hash kontrolü bütünlük iyileştirmesidir; mevcut antivirüs tespitlerini çözmüş sayılmaz. Yeni dosyalar üretip tespit sayısını değiştirmeye çalışmak yerine, orijinal dosya hash'leri ve üreticilerin değerlendirmeleri üzerinden inceleme sürdürülmelidir. Hiçbir üreticiye gönderim veya onay henüz doğrulanmadı.
