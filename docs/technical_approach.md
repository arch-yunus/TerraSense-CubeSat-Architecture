# 🛰️ TerraSense: Teknik Yaklaşım ve Mimari Metodoloji

## 1. Dahili Veri Yolu Mimarisi (Internal Data Bus)
TerraSense, "Dual-Bus" yaklaşımını benimser:
- **Kontrol Hattı (CAN Bus):** Tüm alt sistemlerin (EPS, ADCS, OBC) düşük gecikmeli haberleşmesi için kullanılır. Hata toleransı yüksektir.
- **Veri Hattı (SpaceWire):** Sadece optik sensör ve kitle bellek (Mass Storage) arasında çalışır. Ana işlemciyi görüntü işleme sırasında yormaz.

## 2. RF Haberleşme ve Link Bütçesi
Uydunun yer istasyonu ile bağı, iki farklı RF katmanı üzerinden yönetilir:
- **UHF/VHF (9.6 kbps):** Her yöne yayın yapabilen omni antenler ile uydunun yönelimi ne olursa olsun komuta almasını sağlar.
- **S-Band (2.0 Mbps):** Yönlü patch antenler ile yer istasyonuna geçiş sırasında (overpass) verilerin hızlıca indirilmesini sağlar.

## 3. Yazılım ve Güvenilirlik
- **Watchdog Timer:** Sistem kilitlenmelerine karşı otomatik yeniden başlatma mekanizması.
- **Hata Kontrolü:** Tüm paket transferlerinde CRC-16 ve Reed-Solomon hata düzeltme kodları kullanılır.
- **Modüler Yapılım:** Yeni sensörlerin plug-and-play şeklinde eklenmesine izin veren sürücü katmanlı yazılım mimarisi.

## 4. Kullanılan Standartlar
- **ECSS-E-ST-50-12C:** SpaceWire Haberleşme Standardı.
- **CubeSat Design Specification (CDS):** Mekanik ve elektriksel arayüzler.
- **AX.25:** Telemetri paket çerçeveleme.
