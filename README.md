<div align="center">

![TerraSense Banner](assets/banner.png)

# 🛰️ TerraSense: Küp Uydu (CubeSat) Sistem Mimarisi Tasarımı

[![TUA - Astro Hackathon](https://img.shields.io/badge/TUA-Astro_Hackathon-1E3A8A?style=for-the-badge&logo=spaceX)](https://uzay.gov.tr/)
[![Category - Engineering](https://img.shields.io/badge/Kategori-Mühendislik_ve_Yazılım-F97316?style=for-the-badge)](https://github.com/topics/aerospace)
[![Level - Advanced](https://img.shields.io/badge/Zorluk-İleri_Seviye-DC2626?style=for-the-badge)](https://github.com/topics/cubesat)

</div>

---

## 1. 📋 Gerekli Girdiler (Required Inputs)
Projenin hayata geçirilmesi için temel alınan teknik kısıtlar ve operasyonel girdiler:
- **Form Faktörü:** 3U CubeSat (10x10x34 cm).
- **Kütle Limiti:** Maksimum 4.0 kg.
- **Güç Bütçesi:** Ortalama 15W üretim (GaAs solar hücreler).
- **Yörünge Parametreleri:** 500 km LEO (Düşük Yer Yörüngesi), Sun-Synchronous.
- **Görev Amacı:** Yüksek çözünürlüklü multispektral yeryüzü gözlemi.

---

## 2. 🌟 Yüksek Düzey Özet (High-Level Summary)
**TerraSense**, modüller arası ısıl izolasyon ve hibrit veri yolu mimarisi ile CubeSat sistemlerindeki performans darboğazlarını çözen yenilikçi bir 3U tasarımıdır. "Milli Uzay Hamlesi" vizyonunu temel alan proje; düşük maliyetli, yüksek güvenilirlikli ve hızlı prototiplenebilir bir uzay platformu sunarak Türkiye'nin uzay ekosistemine katkıda bulunmayı hedefler.

---

## 3. 🛠️ Detaylı Çözüm (Detailed Solution)
Uydunun donanım iç yerleşimi (Hardware Layout), kütle merkezi ve ısıl dengeye göre 3 ana katmanda kurgulanmıştır:

- **Unit 1 - Güç ve Stabilite:** Batarya blokları ve ADCS modülü (Reaksiyon tekerlekleri). En ağır bileşenler olduğu için stabilite için uydunun altına yerleştirilmiştir.
- **Unit 2 - Komuta ve Veri İşleme:** OBC (Ana Bilgisayar) ve Transceiver kartları. Isıl açıdan en korunaklı bölge olan merkezde konumlandırılmıştır.
- **Unit 3 - Görev Yükü (Payload):** CMOS sensör ve lens sistemi. Nadir yüzeye (yere bakan) bakacak şekilde en üstte yerleştirilmiştir.

*Daha fazla detay için:* [`/hardware-layout`](hardware-layout)

---

## 4. 🛰️ Teknik Yaklaşım (Technical Approach)
Haberleşme mimarisi; sistem sürekliliği ve yüksek hızlı veri aktarımı için iki katmanlı olarak tasarlanmıştır:

- **Dahili Haberleşme:** Kritik sistem telemetrisi için **CAN Bus**, yüksek boyutlu görüntü verileri için ise **SpaceWire/LVDS** protokolleri kullanılarak veri çakışmaları engellenmiştir.
- **Harici Haberleşme:** TT&C (Telemetri ve Komuta) için güvenilir **UHF/VHF** bandı, bilimsel veri indirme (downlink) için ise yüksek hızlı **S-Band** linki tercih edilmiştir.

*Teknik rapor ve hesaplamalar için:* [`/communication-arch`](communication-arch)

---

## 🔗 Bağlantılar & Demos
*   📽️ **Demo Videosu:** [Drive Linki]
*   📊 **Proje Sunumu:** [Drive Linki]
*   📂 **GitHub Kaynak Kod:** [Bu Repo Linki]

---
<div align="center">
  Developed for <b>TUA Astro Hackathon 2026</b>
</div>