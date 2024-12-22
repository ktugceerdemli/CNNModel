# Hayvan Sınıflandırma Projesi

Bu proje GobalAlHub'ın Görüntü işleme Bootcamp'i için hazırlanmıştır. 

Veri seti Kaggle platformundan elde edilmiştir. [Link](https://www.kaggle.com/datasets/rrebirrth/animals-with-attributes-2)
Kaggle Notebook Linki : [Link](https://www.kaggle.com/code/tugceerdemlial/animalimageprocessingcnnmodel)
## Proje'nin Amacı

Bu projenin amacı, Convolutional Neural Network (CNN) modelini kullanarak görüntüleri 10 hayvan sınıfına sınıflandırmaktır. 

- **Collie**
- **Dolphin**
- **Elephant**
- **Fox**
- **Moose**
- **Rabbit**
- **Sheep**
- **Squirrel**
- **Giant panda**
- **Polar bear**

Proje kapsamında, hayvan görüntülerinden oluşan bir veri kümesi üzerinde veri ön işleme, veri dengeleme ve bir CNN modeli geliştirme işlemleri gerçekleştirilecektir.

---

## Veri Seti Bilgisi

- Veri seti, Python kütüphaneleri (örneğin, os ve shutil) kullanılarak okunacak ve ön işlenecektir.
- Yukarıdaki link'te bulunan verilerden 10 sınıflı bir veri setine indirgenecektir.
- Veri setini dengelemek için her sınıfında 650 resim ile sınırlama yapılacaktır. Her sınıfın ilk 650 görüntüsü alınacak, fazlası proje dışında tutulacaktır.
- Seçilen görüntüler yeni bir dizine taşınacak veya kopyalanacak.

## Veri Manipülasyonu ve Artırma

- Veri arttırma işlemi için ImageDataGenerator kullanılarak
     - Resimler normalize edilip, boyutları tekrar düzenlenecek.
     -  Döndürme (rotation), kaydırma (translation) ve yatay ayna (horizontal flip) teknikleri ile veri çeşitliliği sağlanacaktır.

---

# Model Bilgisi

Projede Tensflow kütüphanesi ile CNN modeli tasarlanarak aşağıdaki özelliklere odaklanılacaktır:

  ## Mimari
- Giriş Katmanı:

Görüntüler, standart bir boyuta (örn. 128x128 veya 224x224) yeniden boyutlandırılacak.
- Konvolüsyon Katmanları:

Artan derinlikte birden fazla konvolüsyon katmanı (örn. 32, 64, 128 filtre).
3x3 çekirdekler ve ReLU aktivasyonu kullanılacak.
- Havuzlama Katmanları:

Konvolüsyon katmanlarından sonra, mekansal boyutları azaltmak için 2x2 boyutunda maksimum havuzlama katmanları uygulanacak.
- Tam Bağlantılı Katmanlar:

Çıkışlar düzleştirilecek ve düzenli hale getirme için dropout içeren yoğun katmanlar eklenecek.
  ## Eğitim
- Kayıp Fonksiyonu:

Çok sınıflı sınıflandırma için categorical_crossentropy.
- Optimizasyon Algoritması:

Uyarlanabilir öğrenme oranı için Adam optimizatörü.
- Değerlendirme Metrikleri:

Sınıflandırma performansı için doğruluk.

# Farklı Işıklar ile Manipülasyon
- Mor, Turuncu ve Yeşil ışıklar ile manipülasyon yapılması

# Renk Sabitliği Algoritması
- Farklı ışıklarla manipüle edilmiş resimlere renk sabitliği algoritması uygulanması.

---

# Gelecek İyileştirmeleri

- CNN modelinin daha katmanlı bir hale getirilmesi
- Başka veri arttırma işlemleri; kenar algılama veya gri tonlama gibi.
- Manipülasyonların Eğitim veri setine de uygulanması






       
