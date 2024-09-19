# Crime Data Analysis Projesi

Bu proje, **Crime Data from 2020 to Present** veri setini kullanarak suç verilerini analiz etmeyi amaçlar. Proje boyunca, eksik verileri işleme, verileri ölçeklendirme ve farklı makine öğrenmesi algoritmaları kullanılarak sınıflandırma ve kümeleme işlemleri gerçekleştirilmiştir.

## Kaggle Projesi
Bu projeye **Kaggle** üzerinden de ulaşabilirsiniz: [Kaggle Proje Linki](https://www.kaggle.com/code/miraytepe/crime-data-machine-learning-model)

## İçindekiler
- [Veri Seti](#veri-seti)
- [Proje Adımları](#proje-adımları)
- [Kullanılan Kütüphaneler](#kullanılan-kütüphaneler)
- [Sonuçlar](#sonuçlar)
- [Nasıl Çalıştırılır](#nasıl-çalıştırılır)
- [İletişim](#iletişim)

## Veri Seti
Proje, Kaggle'dan alınan **Crime Data Analysis** veri setini kullanmaktadır.

**Veri setine buradan ulaşabilirsiniz**: [Kaggle: Crime Data from 2020 to Present](https://www.kaggle.com/datasets/candacegostinski/crime-data-analysis)

## Proje Adımları

### 1. Veri Ön İşleme
- **Eksik veri doldurma**: `SimpleImputer` ile eksik veriler en yaygın değer veya ortalama ile dolduruldu.
- **Tarih verisi işleme**: Tarih verisi uygun formatta işlenip, yıl, ay ve gün bilgileri elde edilmiştir.
- **Veri tipi dönüştürmeleri**: Sayısal sütunlar daha verimli veri tiplerine dönüştürüldü.
- **Kategorik verilerin işlenmesi**: Kategorik sütunlardaki nadir değerler "Other" kategorisine atanmış ve `pd.Categorical` ile verimli hale getirilmiştir.

### 2. Görselleştirme
- **Sayısal değişkenlerin dağılımı**: Verinin genel yapısını anlamak için histogramlar oluşturulmuştur.
- **Kategorik değişken dağılımları**: `seaborn` kullanılarak kategorik değişkenlerin dağılımı görselleştirilmiştir.
- **Korelasyon matrisi**: Sayısal verilerin birbiriyle olan ilişkisini göstermek için korelasyon matrisi çıkarılmıştır.

### 3. Sınıflandırma Modelleri
Aşağıdaki sınıflandırma algoritmaları uygulanmış ve sonuçları karşılaştırılmıştır:
- **Lojistik Regresyon**
- **Karar Ağaçları (Decision Tree)**
- **Naive Bayes**
- **Random Forest**
- **K-Nearest Neighbors (KNN)**
- **Gradient Boosting**

Her modelin başarı oranı (`accuracy_score`) ve sınıflandırma raporu (`classification_report`) değerlendirilmiştir.

### 4. Kümeleme Algoritmaları
Veri kümesi üzerinde unsupervised öğrenme yöntemleri kullanılarak kümeleme işlemi gerçekleştirilmiştir. Kullanılan kümeleme algoritmaları:
- **K-Means**
- **MiniBatchKMeans**
- **HDBSCAN**

Kümeleme sonuçları t-SNE ve PCA kullanılarak görselleştirilmiştir.

### 5. Boyut Azaltma
Veri setinin yüksek boyutlu yapısını daha iyi anlamak için **Principal Component Analysis (PCA)** ile boyut indirgeme işlemi yapılmıştır.

## Kullanılan Kütüphaneler
Projede aşağıdaki Python kütüphaneleri kullanılmıştır:
- `pandas`
- `numpy`
- `matplotlib`
- `seaborn`
- `scikit-learn`
- `hdbscan`
- `joblib`

## Sonuçlar
Farklı sınıflandırma ve kümeleme algoritmalarının sonuçları karşılaştırılmış ve her algoritmanın model başarımı değerlendirilmiştir. Özellikle, Random Forest ve Gradient Boosting sınıflandırma performansında öne çıkmıştır.

## Nasıl Çalıştırılır?

1. Gerekli kütüphaneleri yükleyin:
   ```bash
   pip install -r requirements.txt
2. Projeyi çalıştırmak için Python betiğini çalıştırın:
   ```bash
   python crime_data_analysis.py

### Proje Dosya Yapısı

1. **README.md**: Proje açıklamalarını ve çalıştırma talimatlarını içeren dosya.
2. **requirements.txt**: Projede kullanılan Python kütüphanelerinin bir listesi.
3. **crime_data_analysis.py**: Python analiz kodlarınızın bulunduğu ana dosya.
