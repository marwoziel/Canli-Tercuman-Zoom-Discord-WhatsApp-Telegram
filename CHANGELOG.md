# Sürüm notları

## 1.1.0 — 1 Kasım 2026

Geçersiz kayıtlı Voice ID artık açılışta çökme yerine ayar ekranını açar. Voice ID, anahtarlar diske kaydedilmeden önce doğrulanır. Yanlış alana yapıştırılan uzun değer gösterilmez; mevcut API anahtarları korunur. Yapıştırma kaynaklı tırnak ve görünmez işaretler temizlenir. Dört adımlı ilk kurulum sihirbazı, eksik sürücü kontrolü, resmî VB-Cable indirme/kurulumu açma, kullanıcı tarafından API ve ses üretimi doğrulama, yerel mikrofon/kulaklık testi, isteğe bağlı CV/kurallar ve seçilen cihazları kaydetme eklendi. Ses, seçilen çıkış cihazının doğal örnekleme hızına uyarlanır. 115 çevrimdışı test geçti.

## 1.0.0 — 1 Kasım 2026

İlk kişisel verisiz Windows dağıtımı. Python gerektirmeyen kurulum; ilk açılışta kullanıcıya ait API ve ses ayarı; boş CV/kurallar; Türkçe→İngilizce mikrofon çevirisi; İngilizce→Türkçe ekran çevirisi ve yanıt önerisi; aç/kapat düğmeli İngilizce otomatik sesli yanıt; F8 iptali; yerel düzeltme örnekleri.

Windows kullanıcı verileri program dosyalarından ayrı tutulur. Üçüncü taraf API ve ses cihazları gerektirir. Gerçek görüşme uygulamalarının her sürümünde canlı doğrulama yapılmış değildir.
