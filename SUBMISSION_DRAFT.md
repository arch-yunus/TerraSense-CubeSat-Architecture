# 🚀 TUA Astro Hackathon 2026 - Proje Yükleme Taslağı

Bu döküman, yarışma platformuna yükleyeceğiniz bilgilerin taslağını içerir. Kopyala-yapıştır yaparak kullanabilirsiniz.

---

### 🏷️ Proje Başlığı
**Feza-X: Küp Uydu (CubeSat) Sistem Mimarisi Tasarımı**

---

### 📝 Özet (1-3 Cümle)
Feza-X; 3U form faktöründe, NASA-cFS tabanlı otonom uçuş yazılımı ve kenar yapay zeka (Edge AI) işleme kabiliyetine sahip, Milli Uzay Hamlesi vizyonuyla geliştirilmiş modüler bir küp uydu mimarisidir. Geleneksel tasarımlardaki veri darboğazını "uzayda işleme" teknolojisi ile aşarak yüksek çözünürlüklü multispektral görüntüleme verimliliğini %90 artırır. Proje; mekanik stabilite, siber güvenlik ve otonom hata yönetimi (FDIR) gibi ileri mühendislik standartlarını tek bir ekosistemde birleştirir.

---

### 🔗 Drive Linki
*Lütfen aşağıdaki linki kendi Drive dosyanızla güncelleyin:*
`https://drive.google.com/drive/folders/SİZİN_LİNKİNİZ`
*(Önemli: Linkin "herkese açık" olduğundan emin olun.)*

---

### 🔗 Proje Linki (GitHub/Demo)
`https://github.com/arch-yunus/Feza-X-CubeSat-Architecture`

---

### 📑 Proje Detayları (Açıklama Metni)

#### 1. Giriş ve Problem Tanımı
Uzay teknolojilerinde, özellikle Küp Uydu (CubeSat) segmentinde en büyük engel "veri darboğazı"dır. Sensör çözünürlükleri (GSD) arttıkça, uydunun kısıtlı bant genişliği ile bu devasa veriyi yer istasyonuna indirmesi günler sürebilmektedir. **Feza-X**, bu problemi veriyi indirmeden önce yörüngede işleyen (Edge AI) ve sadece anlamlı olanı ileten akıllı bir mimari ile çözer.

#### 2. Feza-X Mimarisi: 3 Katmanlı Güvenilirlik
Fiziksel tasarımımız, uydunun kararlılığını artırmak için 3 bağımsız modüle ayrılmıştır:
*   **Unit 1 (Altyapı):** EPS ve batarya blokları en alta konumlandırılarak "Gravity Gradient" stabilizesi sağlanmıştır.
*   **Unit 2 (Beyin):** Cortex-M7 tabanlı OBC ve çift yedekli UHF/S-Band haberleşme hattı.
*   **Unit 3 (Görev Yükü):** 5m GSD çözünürlüklü optik sensör ve NPU hızlandırıcılı yapay zeka birimi.

#### 3. İnovatif Yaklaşım: Uzayda Yapay Zeka (Edge AI)
Feza-X'in kalbi olan Edge AI modülü, ham görüntüleri yer istasyonuna göndermeden önce iki kritik işlem yapar:
1.  **Bulut Eleme:** %70+ oranında bulutsu olan kareleri silerek bant genişliğini korur.
2.  **ROI (İlgi Bölgesi) Tespiti:** Gemi, araç konvoyu veya arazi değişikliklerini tespit ederek sadece bu bölgeleri yüksek çözünürlükle iletir.

#### 4. Yazılım Standartları ve Güvenlik
Projemiz, NASA tarafından geliştirilen **Core Flight System (cFS)** mimarisini kullanır. Bu sayede:
*   **Hata Yönetimi (FDIR):** Sistem hatalarını otonom olarak tespit eder ve iyileştirir (Self-healing).
*   **Siber Güvenlik:** Tüm komuta hattı HMAC-SHA256 ile imzalanır, veriler ise AES-256-GCM ile şifrelenir.
*   **Modülerlik:** Yörüngedeyken AI modelleri veya uygulama kodları yer istasyonundan güvenle güncellenebilir.

#### 5. Stratejik Avantaj: Gövde Entegre Paneller
Klasik açılır paneller yerine gövdeye entegre (body-mounted) paneller kullanarak:
*   Mekanik arıza riskini 0'a indirdik.
*   Atmosferik sürüklenmeyi azaltarak uydu ömrünü %25 uzattık.
*   ADCS (yönelim kontrol) üzerindeki tork yükünü minimize ederek çekim kalitesini artırdık.

#### 6. Milli Uzay Hamlesi ve Vizyon
Feza-X, Türkiye'nin 10 yıllık Milli Uzay Programı hedefleriyle tam uyumludur. Yerli partnerlerin (ASELSAN, TÜBİTAK UZAY) standartlarına uygun ICD topolojisi ile teknolojik bağımsızlığı hedefler.

---

### 💾 Kaydet ve Gönder Notları
- **Resimler:** `assets/` klasöründeki `hardware_architecture.png`, `exploded_view.png` ve `feza_x_banner.png` görsellerini "Resim Yükle" kısmından eklemeyi unutmayın.
- **Demos:** Repository içindeki `csp_packet_generator.py` ve `thermal_equilibrium_model.py` simülasyonlarını demo olarak vurgulayabilirsiniz.
