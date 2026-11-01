# Güvenlik incelemesi — 1 Kasım 2026

**Durum: İnceleme açık. İndirmeler askıda. Bu belge güvenlik sertifikası değildir.**

## Bildirilen dosya

CanliTercuman-Setup-1.1.0.exe  
SHA256: `fa035d5794ae0277c130a1ca77324e01f402d7d2a5ecd6be9183eaed0acd665a`

Kullanıcının VirusTotal ekran görüntüsünde Microsoft `Trojan:Win32/Wacatac.C!ml` dahil birden fazla tespit var. Ekrandaki dosya hash'i yayımlanan dosyayla eşleşiyor. Yeni bir VirusTotal taraması henüz alınmadı; mevcut tespitler yanlış alarm olarak doğrulanmadı.

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

- Orijinal 1.1.0 kurucu ile iç uygulamanın ayrı, güncel çok motorlu taramaları.
- Microsoft ve tespit veren üreticilerin dosya/ilgili davranış incelemesi.
- Yeni sürüm yayımlanmadan önce sonuçların dosya hash'i ve tarama tarihiyle belgelenmesi.

Orijinal dosyaları içeren üretici inceleme paketi ve İngilizce açıklama yerelde hazırlandı. Henüz bir üreticiye gönderildiği veya onay alındığı iddia edilmiyor. Antivirüs kapatma, istisna ekleme veya uyarıları aşma önerilmiyor.
