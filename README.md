# Derin Öğrenme Tabanlı CNN Mimarisi ile Meyve Sınıflandırması

Bu proje kapsamında, Evrişimli Sinir Ağları (Convolutional Neural Networks - CNN) kullanılarak elma, armut ve şeftali görsellerinin otomatik olarak sınıflandırılması amaçlanmıştır. Model geliştirme sürecinde PyTorch kütüphanesi kullanılmış ve eğitim işlemleri Google Colab ortamında GPU desteği ile gerçekleştirilmiştir.

## Proje Amacı

Çalışmanın temel amacı, farklı ışık, açı ve arka plan koşullarında bulunan meyve görsellerini yüksek doğruluk oranı ile sınıflandırabilen bir derin öğrenme modeli geliştirmektir.

## Veri Seti

Projede hibrit bir veri seti kullanılmıştır. Veri seti;

* Fruits-360 veri setinden alınan hazır görseller,
* Gerçek ortamda ağaç üzerinde çekilmiş meyve görselleri

birleştirilerek oluşturulmuştur.

Toplam veri seti 3517 adet görselden oluşmaktadır. Veriler eğitim, doğrulama ve test seti olarak sırasıyla %70, %15 ve %15 oranlarında ayrılmıştır.

## Kullanılan Teknolojiler

Projede aşağıdaki teknolojiler ve kütüphaneler kullanılmıştır:

* Python
* PyTorch
* Torchvision
* NumPy
* Scikit-Learn
* Matplotlib
* Seaborn
* Google Colab (CUDA GPU)

## Model Mimarisi

Tasarlanan CNN modeli aşağıdaki temel bileşenlerden oluşmaktadır:

* 3 adet Evrişim Katmanı (Convolutional Layer)
* ReLU Aktivasyon Fonksiyonu
* MaxPooling Katmanları
* Dropout Katmanı (%50)
* Tam Bağlantılı Katmanlar (Fully Connected Layers)

Model eğitiminde kullanılan temel hiperparametreler aşağıda verilmiştir:

| Parametre     | Değer     |
| ------------- | --------- |
| Görsel Boyutu | 100x100x3 |
| Optimizer     | Adam      |
| Learning Rate | 0.001     |
| Batch Size    | 32        |
| Epoch Sayısı  | 50        |
| Dropout Oranı | 0.5       |
| Weight Decay  | 1e-4      |

## Model Performansı

Modelin test veri seti üzerindeki performans sonuçları aşağıda sunulmuştur:

| Metrik    | Sonuç  |
| --------- | ------ |
| Accuracy  | 0.8998 |
| Precision | 0.8992 |
| Recall    | 0.8998 |
| F1-Score  | 0.8981 |

Eğitim sürecinde ayrıca Accuracy/Loss eğrileri, Confusion Matrix ve ROC-AUC analizleri gerçekleştirilmiştir.

## Gelecek Çalışmalar

İlerleyen çalışmalarda veri artırma (Data Augmentation) yöntemlerinin uygulanması, veri setine yeni meyve türlerinin eklenmesi ve farklı derin öğrenme mimarilerinin kullanılması planlanmaktadır. Ayrıca meyvelerin yalnızca türlerinin değil, hastalıklı veya sağlıklı olup olmadıklarının da tespit edilmesi hedeflenmektedir.

## Geliştiriciler

* Kübra Demirtaş
* Elçin Tok
