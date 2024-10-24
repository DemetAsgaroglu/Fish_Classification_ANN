# Fish_Classification_ANN
# Balık Türü Sınıflandırma Projesi

Bu proje, derin öğrenme kullanarak balık türlerini sınıflandırmayı amaçlamaktadır. A Large Scale Fish Dataset veri seti kullanılarak, farklı balık türlerini tanımlamak için bir yapay sinir ağı (ANN) modeli geliştirilmiştir.

## Veri Seti

Veri seti, farklı balık türlerine ait 9000 adet görüntü içermektedir. Veri setindeki her bir resim, belirli bir balık türüne ait etikete sahiptir. Veri seti, aşağıdaki dizinden yüklenmiştir:


### Veri Ön İşleme

- Resimler `.png` formatında yüklenmiş ve 128x128 boyutuna yeniden boyutlandırılmıştır.
- Resimler, model eğitiminde kullanılmadan önce normalleştirilmiştir.
- Etiketler, sayısal forma çevrilerek one-hot encoding yöntemi ile kodlanmıştır.

## Model Yapısı

Model, aşağıdaki katmanlardan oluşmaktadır:

1. **Girdi Katmanı**: Görüntülerin array formatında modele verilmesi sağlanır.
2. **Ara Katmanlar**: Dört tam bağlı katman bulunmaktadır:
   - İlk Katman: 512 nöron, Leaky ReLU aktivasyonu
   - İkinci Katman: 256 nöron, Leaky ReLU aktivasyonu
   - Üçüncü Katman: 128 nöron, Leaky ReLU aktivasyonu
   - Dördüncü Katman: 64 nöron, Leaky ReLU aktivasyonu
3. **Çıkış Katmanı**: Softmax aktivasyonu ile 9 balık türünün sınıflandırılması gerçekleştirilir.

## Model Eğitimi

- **Optimizasyon**: Adam optimizasyon algoritması kullanılmıştır.
- **Kayıp Fonksiyonu**: Çok sınıflı sınıflandırma için categorical_crossentropy kullanılmıştır.
- **Epoch**: Model, 50 epoch boyunca eğitilmiştir.

## Kaggle linki: 
https://www.kaggle.com/code/demetasgaroglu/fish-classification-ann
