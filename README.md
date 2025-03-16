## ULN2803 ile 8 Kanal Röle Kartı
Bu proje, ULN2803A Darlington Transistör Dizisi kullanarak 8 röleyi kontrol edebilen bir röle sürücü kartı tasarlamaktadır. Üç ana bölümden oluşan bu devre kartı gömülü sistem projelerinde, endüstriyel otomasyon ve IoT uygulamalarında röle tabanlı cihazları kontrol etmek için kullanılabilir.
## İçindekiler
- [Özellikler](#özellikler)
- [Kullanılan Bileşenler](#kullanılan-bileşenler)
- [Çalışma Prensibi](#çalışma-prensibi)
- [Proje Görselleri](#proje-görselleri)
## Özellikler
- 8 Kanal röle kontrolü
- ULN2803A ile yüksek akım sürme kapasitesi
- 5V harici güç kaynağı ile çalışabilir.
- Arduino, STM32 ve diğer mikrodenetleyicilerle uyumludur.
- Her röle kanalı için bir LED gösterge eklenerek durum takibi sağlanmıştır.
- Kompakt, düşük parazitli ve kolay üretilebilir PCB tasarımı ile prototipleme ve seri üretime uygundur.
##  Kullanılan Bileşenler
1. **Entegre Devreler**
<<<<<<< HEAD
- ULN2803A: 8 kanallı Darlington transistör dizisi. Röleleri düşük akım seviyelerinde sürmek için kullanılır.
2. **Röleler ve Sürücü Elemanları**
- Röleler (SRD-05VDC-SL-C): Yüksek akım/gerilim anahtarlamak için kullanılır.
- Diyotlar(1N4007): Röle bobinlerinin oluşturduğu ters EMF'yi (geri gerilim darbelerini)  engellemek için kullanılır. (flyback diyotları)
=======
- ULN2803A: 8 kanallı Darlington transistör dizisi röleleri düşük akım seviyelerinde sürmek için kullanıldı.
2. **Röleler ve Sürücü Elemanları**
- Röleler (SRD-05VDC-SL-C): Yüksek akım/gerilim anahtarlamak için kullanılır.
- Diyotlar(M7-DC 1A 1000V): Röle bobinlerinin oluşturduğu ters EMF'yi (geri gerilim darbelerini)  engellemek için kullanılır. (flyback diyotları)
>>>>>>> 54cf637373071c6b525579860f33b1d83039397b
3. **Pasif Bileşenler**
- 10kΩ pull-down dirençler (R2-R9): Bu dirençler, giriş pinlerinin belirsiz bir durumda kalmasını engellemek için GND'ye bağlanmış. Pull-down dirençleri sayesinde girişler, kaynaktan bağımsız olarak her zaman belirli bir lojik seviyede kalır.
- 10kΩ seri giriş dirençleri (R10-R17): Seri dirençler, giriş pinleri üzerindeki ani gerilim değişikliklerini (darbe gürültülerini) yumuşatarak ULN2803A’nın daha stabil çalışmasını sağlar. Sinyal geçişlerini daha düzgün hale getirerek istenmeyen osilasyonları önler. Aynı zamanda akımı sınırlayarak mikrodenetleyici pinlerini korur.
- 680Ω röle LED göstergeleri için dirençler (R18-R25): LED'lerin aşırı akım çekmesini engellemek için kullanılır.
- 100nF (C2-C3): ULN2803A’nın güç hattında gürültüyü filtrelemek için kullanılır.
4. **Göstergeler & Bağlantılar**
- LED'ler (D1-D16): Rölelerin aktif olup olmadığını göstermek için kullanılır.
- Bağlantı Terminalleri (J2, J5-J10): Mikrodenetleyici ve harici yükler için giriş/çıkış bağlantı noktaları.
5. **Güç ve Kontrol**
- 5V Güç Kaynağı: Devrenin çalışma voltajına bağlı olarak harici güç kaynağı
- Switch (SW1): Devreye güç vermek veya kesmek için kullanılır.
## Çalışma Prensibi
- 5V  besleme bağlanır
- Mikrodenetleyici çıkışı ULN2803A girişine bağlanır.
- ULN2803A çıkışı röleyi tetikler.
- Röle, bağlı olan yüksek güçlü cihazları açıp kapatır.
- LED'ler röle durumunu gösterir.
## Proje Görselleri
<p align="center">
<img src="https://github.com/yavuzselimpek/8-Channel-Relay-Driver/blob/master/Pictures/schema.png">
<p align="center">
<img src="https://github.com/yavuzselimpek/8-Channel-Relay-Driver/blob/master/Pictures/PCB01.png">
<p align="center">
<img src="https://github.com/yavuzselimpek/8-Channel-Relay-Driver/blob/master/Pictures/PCB02.png">
<p align="center">
<img src="https://github.com/yavuzselimpek/8-Channel-Relay-Driver/blob/master/Pictures/PCB03.png">
<p align="center">
<img src="https://github.com/yavuzselimpek/8-Channel-Relay-Driver/blob/master/Pictures/PCB04.png">
<p align="center">
<img src="https://github.com/yavuzselimpek/8-Channel-Relay-Driver/blob/master/Pictures/PCB05.png">
<p align="center">
<img src="https://github.com/yavuzselimpek/8-Channel-Relay-Driver/blob/master/Pictures/PCB06.png">