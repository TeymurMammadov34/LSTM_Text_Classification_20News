# 🧠 LSTM ile 20 Newsgroups Metin Sınıflandırma
Bu proje, **20 Newsgroups** metin veri setini kullanarak derin öğrenme (LSTM) ile metin sınıflandırması yapmaktadır. Amaç, haber metinlerini doğru kategorilere ayıran bir model geliştirmektir.


# 🔍 Proje Özeti

- Veri Seti: 20 Newsgroups — 20 farklı haber grubundan binlerce metin içerir.

- Model: LSTM (Long Short-Term Memory) ağı kullanılarak derin öğrenme temelli çok sınıflı sınıflandırma modeli inşa edilmiştir.

- Hedef: Verilen bir metnin ait olduğu kategori(yi) tahmin etmek.



# 📦 Kullanılan Kütüphaneler


| Kütüphane          | Amaç                                           |
| ------------------ | ---------------------------------------------- |
| `numpy`, `pandas`  | Veri işleme ve analiz                          |
| `matplotlib`       | Grafik ve eğitim süreci görselleştirme         |
| `scikit-learn`     | Veri seti, etiket kodlama, eğitim/test ayırımı |
| `tensorflow.keras` | Metin önişleme, model katmanları, eğitim       |
| `warnings`         | Uyarı mesajlarını gizlemek için                |



# ⚙️ Model Mimarisine Genel Bakış

Model sırasıyla şu katmanlardan oluşur:

1. **Embedding Layer:** Kelimeleri 32 boyutlu vektörlere dönüştürür.

2. **LSTM Layer:** Metinlerdeki ardışık bağıntıları öğrenir.

3. **Dropout Layer:** Overfitting’i önler (%60 oranında nöronları siler).

4. **Dense Output Layer:** Softmax aktivasyonu ile 20 sınıf tahmini yapılır.


# 🧪 Eğitim Detayları

- Eğitim Epoch sayısı: **20**

- Erken durdurma: **val_loss** 7 epoch boyunca düşmezse eğitim durur.

- Eğitim/Doğrulama bölünmesi: **X_train,y_train** + **x_test,y_test**

- En iyi ağırlıklar, erken durdurma ile geri yüklenir.


# 📊 Performans
Model test verisi üzerinde yaklaşık olarak şu sonuçları vermektedir:

**Test loss:** *~1.85*

**Test accuracy:** *~46%*

**Not:** Sonuçlar kullanılan token sayısı, **LSTM** hücre sayısı, dropout oranı gibi hiperparametrelere göre değişebilir.



## 👨‍💻 Geliştirici

**Teymur Mammadov** 
