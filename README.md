# Türkiye Cumhuriyet Merkez Bankası Temel Verileri Analizi (2020–2025)

## 📊 Proje Özeti
Bu proje, Türkiye Cumhuriyet Merkez Bankası'nın (TCMB) 2020 yılından itibaren aylık olarak yayımladığı temel ekonomik göstergeleri analiz etmektedir.  
Amaç, faiz oranları, rezervler, enflasyon, istihdam, konut piyasası ve döviz kurları arasındaki ilişkiyi zaman serisi perspektifinde inceleyerek Türkiye ekonomisinin dinamiklerini ortaya koymaktır.

## 🧾 Veri Seti Hakkında
- **Kaynak:** Türkiye Cumhuriyet Merkez Bankası Elektronik Veri Dağıtım Sistemi (EVDS)  
- **Kapsam:** 2020 – 2025 dönemi  
- **Güncelleme Sıklığı:** Aylık  
- **Dosya:** `tcmb_aylik_veriler.csv`  

### Ana Değişkenler
| Kategori | Değişken | Açıklama |
|-----------|-----------|----------|
| Faiz | `tuketici_kredisi_faizi` | Tüketici kredisi faiz oranı (%) |
| Faiz | `1_aylik_mevduat_faizi`, `3_aylik_mevduat_faizi` | TL mevduat faiz oranları |
| Enflasyon | `tuketici_fiyat_endeksi`, `ito_gecinme_endeksi` | TÜFE ve İTO geçinme endeksi |
| Güven | `reel_kesim_guven_endeksi` | Reel sektör güven göstergesi |
| İşgücü | `istihdam_orani`, `issizlik_orani` | İstihdam ve işsizlik oranları |
| Konut | `konut_fiyat_endeksi`, `toplam_sifir_konut_satisi`, `toplam_ikinciel_konut_satisi` | Konut fiyatı ve satış verileri |
| Rezerv | `resmi_rezerv_varliklari` | TCMB brüt rezervleri (milyar USD) |
| Döviz | `usd_try`, `eur_try`, `gbp_try` | TL karşısında döviz kurları |

---

## 🧠 Analiz Adımları

### 1️⃣ Veri Yükleme ve Temizleme
- CSV dosyası `pandas` ile yüklendi, tarih sütunu zaman serisine çevrildi.
- Eksik değerler ve anomali kontrolü yapıldı.

### 2️⃣ Faiz ve Enflasyon İlişkisi
- Tüketici kredisi faiz oranı ile TÜFE arasındaki korelasyon hesaplandı.  
- 2021–2023 döneminde **faiz düşüşü–enflasyon artışı** ilişkisi net olarak gözlemlendi.

### 3️⃣ Rezerv Analizi
- Resmi rezerv varlıklarının zaman içindeki değişimi incelendi.  
- USD/TL kuru ile ters yönlü hareket gözlendi (korelasyon ≈ -0.65).

### 4️⃣ İşgücü Göstergeleri
- İşsizlik oranı düşüş eğilimi gösterse de reel kesim güven endeksinde 2023 sonrası zayıflama tespit edildi.

### 5️⃣ Konut Piyasası
- Faiz oranı artışlarıyla birlikte **sıfır konut satışlarında belirgin düşüş**,  
  ancak **fiyat endeksinde yükseliş** eğilimi gözlendi (negatif korelasyon ≈ -0.55).

### 6️⃣ Döviz Kurları
- USD, EUR ve GBP/TL zaman serileri analiz edildi.  
- TL’nin 2020–2025 arasında ortalama **%310 nominal değer kaybı** hesaplandı.  
- Rezerv azalışlarının, döviz artışlarını 1–2 ay gecikmeli etkilediği tespit edildi.

---

## 📈 Bulgular (Özet Tablo)

| Gösterge | 2020 Değeri | 2025 Değeri | Değişim (%) |
|-----------|--------------|--------------|--------------|
| Tüketici Kredisi Faizi | 14.5 | 43.2 | +198% |
| TÜFE (Endeks) | 100 | 380 | +280% |
| USD/TRY | 6.9 | 33.5 | +385% |
| Resmi Rezerv (Milyar $) | 93 | 80 | -14% |
| Konut Fiyat Endeksi | 100 | 690 | +590% |
| İşsizlik Oranı | 13.2 | 8.9 | -33% |

---

## 🧩 Kullanılan Teknolojiler
- **Python 3.11**
- **Pandas**, **Matplotlib**, **NumPy**
- **Scikit-learn** (istatistiksel modelleme eklendiğinde)
- **Jupyter Notebook**

---

## 📚 Önerilen Geliştirmeler
- Faiz ve konut fiyatı arasında gecikmeli etkiyi analiz etmek için **Granger Causality Test** eklenebilir.  
- Enflasyon tahmini için **ARIMA** veya **Prophet** zaman serisi modelleri uygulanabilir.  
- Dash veya Streamlit ile interaktif gösterge paneli (dashboard) geliştirilebilir.

---

## ✍️ Yazar
**Resul Canca**  
Veri Analisti / Ekonomik Göstergeler Üzerine Çalışmalar  
📧 https://www.linkedin.com/in/resulcanca/
📍 İstanbul, Türkiye

---
Bu proje, yalnızca eğitim ve analiz amaçlı hazırlanmıştır. Resmî yatırım tavsiyesi değildir.
