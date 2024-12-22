# ImageProcessBootcampProject
- Global AI Hub Aygaz Görüntü İşleme Bootcamp Projesi -

**Proje Özeti**

Bu proje, Convolutional Neural Network (CNN) modellerinin temelini kavramayı ve çeşitli hayvan türlerini sınıflandıran bir model geliştirmeyi amaçlamaktadır. Proje dört ana aşamadan oluşmaktadır:

. Veri setinin hazırlanması

. CNN modelinin tasarımı ve eğitimi

. Modelin farklı senaryolarda test edilmesi

. Test sonuçlarının karşılaştırılması ve raporlanması



**Veri Seti**

Kullanılan veri seti: Animals with Attributes 2  ( https://www.kaggle.com/datasets/rrebirrth/animals-with-attributes-2 )

Sınıflar: Collie, Dolphin, Elephant, Fox, Moose, Rabbit, Sheep, Squirrel, Giant Panda, Polar Bear

**Veri işleme:**

Her sınıf için 650 resim seçildi.

Resimler normalize edildi ve model girişine uygun boyutlara getirildi.

Eğitim (%70) ve test (%30) olarak ikiye ayrıldı.

Eğitim verilerine veri artırma (augmentation) teknikleri uygulandı.


**Kullanılan Teknolojiler**

Python

TensorFlow/Keras

OpenCV

Scikit-learn


**Proje Aşamaları**

**1. Veri Hazırlığı**

Veri seti işlendi, sınıflar belirlendi ve dengelendi.

Resimler normalize edilerek modelin girişine uygun hale getirildi.

Eğitim ve test setleri oluşturuldu.


**2. CNN Modeli Tasarımı**

Model, aşağıdaki bileşenlerle oluşturuldu:

Convolutional Layer

Activation Function (ReLU)

Pooling Layer

Fully Connected Layer

Dropout

Categorical Crossentropy loss fonksiyonu kullanıldı.

**3. Modelin Test Edilmesi**

Model önce orijinal test setiyle, ardından manipüle edilmiş test setleriyle test edildi.

Manipülasyonlar:

Farklı ışıklandırma koşulları

Renk sabitliği algoritmaları


**4. Sonuçların Karşılaştırılması**

Üç farklı senaryoya ait başarı oranları karşılaştırıldı ve raporlandı.

Skor düşüşleri üzerine çözüm önerileri tartışıldı.

