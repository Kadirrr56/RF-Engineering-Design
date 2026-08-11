# Proje 4: CST Studio Aşaması (Mikroşerit Hattın 3D Fiziksel Modeli ve Designer ile Karşılaştırma)

### Amaç
Proje 3'ün Designer aşamasında LineCalc ile sentezlenen mikroşerit hat boyutlarını (W=3.02mm, P=17.05mm) kullanarak CST Studio Suite'te gerçek bir 3D fiziksel yapı (bakır iz + FR4 substrat + toprak düzlemi) kurmak, tam dalga (full-wave) elektromanyetik simülasyon ile S-parametrelerini hesaplamak ve Designer'ın "ideal/dağıtık model" sonucuyla karşılaştırmak[cite: 5].

### CST Model Kurulumu
**Proje Şablonu ve Ayarlar**
* **Kategori:** MW & RF & Optical → Circuit & Components → Planar Filters[cite: 5]
* **Solver:** Time Domain (Transient)[cite: 5]
* **Birimler:** mm / GHz / ns[cite: 5]
* **Frekans aralığı:** 0.5 – 3.5 GHz (Designer simülasyonuyla birebir aynı, karşılaştırılabilir olması için)[cite: 5]

**Malzemeler**
| Malzeme | Tip | Parametreler |
| :--- | :--- | :--- |
| **FR4_custom** | Normal (dielektrik) | Epsilon = 4.4, Mu = 1, Tangent delta el. = 0.02 @ 2.4 GHz[cite: 5] |
| **Copper (annealed)** | Kütüphaneden yüklendi | İletken kaybı gerçekçi bakır modeli[cite: 5] |

**Geometri — 3 Katmanlı Yapı**
Model, alttan üste üç bloktan (Brick) oluşturuldu[cite: 5]. X ekseni sinyal yayılım yönü, Y ekseni genişlik, Z ekseni katman yüksekliği olarak tanımlandı[cite: 5].

| Katman | X (mm) | Y (mm) | Z (mm) | Malzeme |
| :--- | :--- | :--- | :--- | :--- |
| **Ground (toprak düzlemi)** | 0 → 17.05 | -10 → 10 | -0.035 → 0 | Copper (annealed)[cite: 5] |
| **Substrate (FR4)** | 0 → 17.05 | -10 → 10 | 0 → 1.6 | FR4_custom[cite: 5] |
| **Trace (bakır iz)** | 0 → 17.05 | -1.51 → 1.51 | 1.6 → 1.635 | Copper (annealed)[cite: 5] |

Trace genişliği (Y aralığı, 3.02mm), LineCalc'ten çıkan W değeriyle birebir örtüşüyor ve substratın tam ortasına ortalanmış durumda[cite: 5].

![Yandan görünüm (Y-Z düzlemi)](images/sekil1_yandan.png)
*Şekil 1 — Yandan görünüm (Y-Z düzlemi): substrat, altında toprak düzlemi ve üstünde bakır iz (katmanlar ince olduğu için görsel ölçekte ayırt edilmesi zor, koordinatlarla doğrulandı)[cite: 5]*

### Portlar (Waveguide Ports)
Hattın her iki ucuna, kesit alanını tamamen kaplayan Waveguide Port yerleştirildi[cite: 5]. Port1, X=0 ucunda; Port2, X=17.05mm ucunda tanımlandı[cite: 5]. Her ikisi de Y: -10→10mm, Z: -0.035→5mm aralığını kapsıyor — toprak düzleminin altından başlayıp hattın üstünde yeterli hava boşluğu (5mm) bırakacak şekilde[cite: 5].

![3D model portlar](images/sekil2_portlar.png)
*Şekil 2 — 3D model: hattın iki ucundaki portlar (kırmızı yüzeyler)[cite: 5]*

### Sınır Koşulları (Boundary Conditions)
Tüm yönler (Xmin/Xmax/Ymin/Ymax/Zmin/Zmax) için "Open (add space)" seçildi — mikroşerit gibi açık/planar yapılarda standart ve en gerçekçi seçim, dalganın yanlardan ve üstten serbestçe yayılmasına izin veriyor[cite: 5].

### Simülasyon Sonuçları

**S11 (Yansıma)**
![CST S11 grafiği](images/sekil3_cst_s11.png)
*Şekil 3 — CST S11 grafiği: 0.5 GHz'de ~-44dB, 3.5 GHz'de ~-32dB, monoton artan eğri[cite: 5]*

S11, tüm bant boyunca -32dB'nin altında kaldı — hattın gerçek 3D fiziksel yapıda da çok düşük yansıma gösterdiğini kanıtlıyor[cite: 5]. Mesh Pass 1 ve Mesh Pass 2 eğrilerinin neredeyse üst üste çakışması, çözümün mesh çözünürlüğünden bağımsız, güvenilir bir sonuç olduğunu gösteriyor (yakınsama sağlanmış)[cite: 5].

**S21 (Geçiş)**
![CST S21 grafiği](images/sekil4_cst_s21.png)
*Şekil 4 — CST S21 grafiği: 0.5 GHz'de ~-0.01dB, 3.5 GHz'de ~-0.26dB, kademeli azalan eğri[cite: 5]*

S21, 0.5GHz'de neredeyse kayıpsız (~-0.01dB) iken, 3.5GHz'e çıkıldıkça kayıp kademeli olarak artıyor (~-0.26dB'ye kadar)[cite: 5]. Bu artış, dielektrik kaybının (TanD) ve bakırın iletken kaybının frekansla birlikte artmasından kaynaklanıyor — fiziksel olarak beklenen bir davranış[cite: 5].

### Designer ile Karşılaştırma
| Özellik | Designer (ideal/dağıtık model) | CST (3D fiziksel model) |
| :--- | :--- | :--- |
| **S11 aralığı (0.5–3.5 GHz)** | ~ -42 ile -32 dB arası[cite: 5] | ~ -44 ile -32 dB arası[cite: 5] |
| **S11 eğri şekli** | Hafif tümsek: önce iyileşip sonra kötüleşiyor[cite: 5] | Monoton: frekansla sürekli kötüleşiyor[cite: 5] |
| **S21** | ~0 dB'ye çok yakın, düz görünümlü[cite: 5] | 0 dB'den -0.26 dB'ye kademeli azalış[cite: 5] |
| **Yakınsama / güvenilirlik göstergesi** | —[cite: 5] | Mesh Pass 1-2 çakışıyor, sonuç güvenilir[cite: 5] |

**Yorum**
İki model de büyüklük (magnitude) açısından aynı mertebede ve birbirine çok yakın sonuçlar veriyor — bu, LineCalc ile yapılan elle/analitik hesabın ve Designer'daki dağıtık devre modelinin, gerçek 3D fiziksel dünyada da doğrulandığı anlamına geliyor[cite: 5]. Şekil olarak gözlenen küçük fark (Designer'da S11'in önce iyileşip sonra kötüleşmesi, CST'de ise sürekli kötüleşmesi) CST'nin gerçek 3D radyasyon kaybını, kenar etkilerini (fringing fields) ve tam dalga etkileşimlerini hesaba katmasından kaynaklanıyor[cite: 5]. Designer'ın basitleştirilmiş dağıtık model formülleri bu etkileri tam olarak yakalayamıyor[cite: 5]. Bu fark, ideal/analitik modellerin gerçek fiziksel dünyada nerede ayrıştığını gösteren, bu projenin asıl öğretmek istediği kavram[cite: 5].

### Öğrenilen Kavramlar
* CST Studio'da proje şablonu seçimi, birim/frekans ayarları ve malzeme tanımlama (Normal tip, Epsilon, Tangent delta el.)[cite: 5]
* Brick komutuyla katmanlı 3D geometri kurma ve koordinatların (Xmin/Xmax, Ymin/Ymax, Zmin/Zmax) tutarlılığının önemi[cite: 5]
* Waveguide Port tanımlama mantığı: port boyutunun kesit alanını kapsaması, portların birbirine "bakması"[cite: 5]
* Boundary conditions (Open/add space) seçiminin planar yapılarda standart kullanımı[cite: 5]
* Mesh Pass karşılaştırmasıyla simülasyon sonucunun yakınsadığının (mesh'e bağlı hata içermediğinin) doğrulanması[cite: 5]
* İdeal/dağıtık devre modeli (Designer) ile tam dalga 3D fiziksel model (CST) arasındaki farkın kaynağı: radyasyon kaybı, kenar etkileri, tam dalga etkileşimleri[cite: 5]
* Designer → CST iş akışının tamamlanması: analitik/devre seviyesi tasarımdan fiziksel doğrulamaya geçiş[cite: 5]

> *Not: Bu belge, Proje 3'ün CST Studio aşamasını raporlamak için ayrı olarak hazırlanmıştır[cite: 5]. Designer aşaması, ana özet dokümanında (RF_Proje_Ozet.docx) yer almaktadır[cite: 5].*
