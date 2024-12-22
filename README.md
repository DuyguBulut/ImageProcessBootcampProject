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

1. İlk Test Verileri Sonuçları
Doğruluk: 67.56%
Kayıp: 5.5746
İlk test verileri ile modelin doğruluğu %67.56 olarak belirlenmiş ve kayıp 5.5746. Bu sonuç, modelin eğitim sırasında genel olarak doğru tahminler yapabildiğini, ancak mükemmel bir sonuç elde edilmediğini gösteriyor. Modelin genel başarısı, belirli bir problem üzerinde yapılacak iyileştirmelerle artırılabilir.

2. Manipüle Edilmiş Test Verileri Sonuçları
Doğruluk: 18.62%
Kayıp: 54.2937
Manipüle edilmiş test verileri ile elde edilen doğruluk oranı %18.62, kayıp ise 54.2937. Bu düşük doğruluk oranı, manipülasyonların modelin doğru sonuçlar üretmesini zorlaştırdığını gösteriyor. Manipülasyonlar, verilerin çok farklı bir biçime dönüşmesine neden olabilir ve modelin bu değişimlere uyum sağlaması zor olabilir.

3. Renk Sabitliği Uygulanan Test Verileri Sonuçları
Doğruluk: 65.30%
Kayıp: 5.2612
Renk sabitliği uygulanmış test verilerinde ise doğruluk %65.30, kayıp ise 5.2612. Bu sonuç, renk sabitliği algoritmasının manipülasyonların etkilerini kısmen azalttığını ve modelin manipüle edilmiş verilerde daha iyi performans göstermesini sağladığını gösteriyor. Manipülasyonlara rağmen modelin doğru tahmin yapabilmesi, renk sabitlemenin önemli bir iyileştirme sağladığını gösteriyor.

Sonuçların Yetersiz Olma Sebepleri ve Çözüm Önerileri
1. Manipülasyonların Model Performansını Düşürmesi
   
Manipülasyonlar genellikle verinin doğal yapısını değiştirir ve modelin doğru tahminler yapmasını zorlaştırabilir. Bu durumun sebepleri şunlar olabilir:

Veri Çeşitliliği: 
Modelin eğitildiği veriler manipüle edilmiş verilere uyum sağlamakta zorlanmış olabilir. Manipülasyonlar, özellikle renk değişimlerini içeriyorsa, modelin renklerin veya ışık koşullarının etkisini öğrenmesini zorlaştırabilir.

Modelin Genel Başarısızlığı: 
Modelin manipülasyonlar karşısında başarısız olmasının diğer bir sebebi, modelin eğitim sırasında yeterince çeşitli veri ile eğitilmemiş olması olabilir. Özellikle yapay ışık koşullarını içeren veriler modelin başarısını düşürebilir.

2. Renk Sabitliği Algoritmasının Yetersizliği

Renk sabitliği algoritması bazı durumlarda etkili olsa da, daha karmaşık ışık koşullarında ya da çok fazla manipülasyon yapılan verilerde beklenen iyileştirmeyi sağlamakta zorlanabilir. Renk sabitleme işlemi, modelin manipülasyonları dengelemesine yardımcı olmuş ancak tam anlamıyla etki etmemiştir.

Çözüm Önerileri
Daha Fazla Veri ile Eğitim:

Modelin manipülasyona karşı dayanıklılığını artırmak için daha fazla manipülasyonlu veri ile eğitim yapabiliriz. Bu sayede model manipülasyonlara karşı daha iyi genelleme yapabilir.
Veri Augmentasyonu kullanıldı ancak yeterli olmadı, eğitim setine daha fazla çeşitlilik eklemek ve farklı parametrelerle yeniden eğitim yapmak (dönme, yakınlaştırma, renk değişimlerini içeren augmentasyonlar) modelin daha iyi genelleme yapmasına yardımcı olabilir.
Renk Sabitliği Algoritmasını Geliştirme:

Şu anda kullanılan renk sabitliği algoritması başarılı olmasına rağmen, farklı ışık koşulları ve daha karmaşık manipülasyonlar için daha gelişmiş algoritmalar kullanabilirsiniz. Örneğin, Huang ve Wang'ın 2019'da önerdiği algoritmalar gibi daha sofistike renk sabitleme teknikleri araştırılabilir.

Modeli Geliştirme ve Parametre Ayarları:

Model mimarisini gözden geçirebiliriz. Özellikle daha derin ağlar (daha fazla katman, farklı mimariler gibi) veya transfer öğrenme yöntemleri (örneğin, ResNet, VGG) modelin performansını artırabilir.
Öğrenme oranı ve ağırlık güncelleme tekniklerini inceleyerek, eğitimde daha iyi sonuçlar elde edebiliriz.
Modelin eğitimi sırasında daha fazla epoch kullanmak ve erken durdurma (early stopping) yöntemini gözden geçirmek, modelin daha iyi öğrenmesini sağlayabilir.

Manipülasyon Tiplerinin Çeşitlendirilmesi:

Renk manipülasyonu dışında başka tür manipülasyonlar (örneğin, parlaklık, kontrast değişimlerini içeren augmentasyonlar) eklemek, modelin farklı ışık ve renk koşullarına dayanıklılığını artırabilir.
Modelin Performansını Takip Etme:

Validation set üzerinde modelin doğruluğunu takip etmek, aşırı öğrenme (overfitting) veya yetersiz öğrenme (underfitting) durumlarının önüne geçebilir.

**Sonuç**

Manipülasyonlar ve renk sabitleme algoritması modelin performansını iyileştirmede bir miktar etkili olmuş olsa da, genel doğruluk oranı hala tatmin edici seviyelere ulaşmamış durumda. Yukarıda önerilen iyileştirme yöntemleri adım adım test edilerek, modelin manipülasyonlarla başa çıkabilme yeteneği artırılabilir.
