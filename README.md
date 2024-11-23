# Road_Accident_Casualties Veri Seti İncelemesi ve Sınıflama Modeli
"Safety first!"

Proje Linki: https://www.kaggle.com/code/keremozakca/accident-casualties-prediction
Veri Seti: https://www.kaggle.com/datasets/nezukokamaado/road-accident-casualties-dataset

## Kazalar Analizi ve Tahmin Modeli

Bu projede, yol kazası verilerini kullanarak **yaralı sayısını tahmin etmeye** yönelik bir model geliştirilmesi amaçlanmaktadır. Veriler, farklı kazalarla ilgili çeşitli özellikleri içermektedir. Özellikle, kazaların **şiddeti**, **ışık koşulları**, **yol yüzey koşulları**, **yol tipi**, **şehir içi/şehir dışı alanlar**, **hava koşulları** ve **araç tipi** gibi kategorik değişkenlerin yanı sıra, kazaya karışan araç sayısı ve coğrafi konum bilgisi gibi sayısal veriler de yer almaktadır.

Veri setine aşağıdaki bağlantıdan ulaşabilirsiniz:
[Accidents Dataset](https://www.kaggle.com/datasets/nezukokamaado/road-accident-casualties-dataset)

## Özellikler

Veri setinde kullanılan temel kategorik ve sayısal özellikler şunlardır:

### Kategorik Özellikler:
- **Accident_Severity**: Kazanın şiddeti (Slight, Serious, Fatal)
- **Light_Conditions**: Işık koşulları (Day, Dark (lit), Dark (none), vb.)
- **Road_Surface_Conditions**: Yol yüzey koşulları (Dry, Wet, Icy, vb.)
- **Road_Type**: Yol tipi (Single Rd, Dual Rd, Roundabout, vb.)
- **Urban_or_Rural_Area**: Şehir içi/şehir dışı alan (Urban, Rural, Unallocated)
- **Weather_Conditions**: Hava koşulları (Fine, Rain, Snow, vb.)
- **Vehicle_Type**: Araç tipi (Car, Van, Bus, vb.)

### Sayısal Özellikler:
- **Latitude**: Enlem
- **Longitude**: Boylam
- **Number_of_Casualties**: Yaralı sayısı
- **Number_of_Vehicles**: Kazaya karışan araç sayısı

## Keşifsel Veri Analizi

Veri seti üzerinde yapılan keşifsel analizde şu bulgulara ulaşılmıştır:

### Işık Koşulları (Light Conditions)
- Çoğu kaza **gündüz** (Day) gerçekleşmektedir.
- Işık koşullarına göre kazaların şiddeti genellikle **slight** (hafif) olarak rapor edilmiştir.
- **Kötü ışık koşulları** (karanlık, ışıklandırılmamış) kazalarda daha fazla yaralıya yol açmamaktadır.
  
### Yol Yüzey Koşulları (Road Surface Conditions)
- En yaygın yol yüzey koşulu **kuru** (Dry) olup, bu koşulda kazaların şiddeti genellikle **slight**’tir.
- **Ilımlı** (Wet) ve **buzlu** (Icy) yol koşulları kazalarda daha fazla yaralıya neden olmaktadır.

### Yol Tipi (Road Type)
- **Tek yol** (Single Rd) en yaygın yol tipi olup, kazaların çoğu bu yolda meydana gelmiştir.
- **Çift yol** (Dual Rd) gibi yollar kazalarda daha fazla yaralıya yol açmaktadır.

### Şehir İçi/Şehir Dışı Alanlar (Urban/Rural Area)
- **Şehir içi** kazalarda, **şehir dışı** alanlara göre daha az yaralı bulunmaktadır.
- **Kırsal alanlarda** daha fazla yaralı sayısı gözlemlenmiştir.

### Hava Koşulları (Weather Conditions)
- Kazalar en çok **güzel hava koşullarında** (Fine) gerçekleşmektedir.
- Hava koşullarının kazaların şiddeti üzerinde belirgin bir etkisi yoktur, ancak **fırtına** (Stormy) ve **buzlu** (Blizzard) koşullarında daha fazla yaralıya rastlanmaktadır.

### Araç Tipi (Vehicle Type)
- En yaygın araç tipi **araba** (Car) olup, kazalarda genellikle hafif yaralanmalar görülmektedir.
- **Bisiklet** gibi daha küçük araçlar kazalarda biraz daha fazla yaralıya yol açmaktadır.

## Sayısal Analizler

- **Enlem** ve **Boylam** verileri, kazaların çoğunun Birleşik Krallık'ta (UK) yoğunlaştığını göstermektedir.
- Kazaya karışan araç sayısı genellikle 1 ila 5 arasında değişmektedir.

## Model Geliştirme

Bu keşifsel veri analizi sonucunda, **yaralı sayısını tahmin etmek** için çeşitli sınıflandırma modelleri geliştirilecektir. Modellerde kullanılan özellikler arasında **ışık koşulları**, **yol yüzey koşulları**, **hava koşulları** ve **şehir içi/şehir dışı alanlar** gibi faktörler yer alacaktır.

### Kullanılan Teknolojiler ve Yöntemler
- **Python**: Veri işleme ve modelleme için temel programlama dili.
- **Pandas**: Veri analizi ve temizleme işlemleri için kullanıldı.
- **Scikit-learn**: Modelleme ve sınıflandırma işlemleri için kullanıldı.
- **Matplotlib** ve **Seaborn**: Veri görselleştirme işlemleri için kullanıldı.

## Grafikler

- Işık koşulları, yol yüzey koşulları, yol tipi, hava koşulları ve araç tipi gibi kategorik değişkenlerin her biri için bar grafikler ve sayısal özetler görüntülenmiştir.

## Sonuçlar ve Çıkarımlar

Veriler üzerinde yapılan analizler, kazaların çoğunun gündüz, kuru yol yüzey koşullarında ve iyi hava koşullarında meydana geldiğini göstermektedir. Ancak, **kötü yol koşulları** ve **düşük ışık seviyeleri** kazalarda daha fazla yaralıya neden olabilmektedir. Bu bulgular, gelecekteki model geliştirmeleri için rehber olacaktır. (%70 Doğruluk Oranı)

## Öneriler
Bu proje, yol kazası verilerini kullanarak yaralı sayısını tahmin etmeyi amaçlayan bir model geliştirmiştir ve %70 doğruluk oranı elde edilmiştir. Ancak doğruluk oranını artırmak için şu adımlar önerilmektedir:

**Özellik Seçimi ve Veri Temizliği:** Gereksiz özelliklerin çıkarılması ve yeni özelliklerin eklenmesi modelin doğruluğunu artırabilir.
**Farklı Modellerin Denenmesi:** Random Forest, XGBoost gibi modellerle sonuçlar iyileştirilebilir.
**Hiperparametre Optimizasyonu:** Grid Search ile modelin parametreleri optimize edilebilir.
**Daha Fazla Veri Kullanımı:** Verinin genişletilmesi modelin başarısını artırabilir.

## Kullanım Alanları

**Trafik Güvenliği:** Bu model, kaza analizi ve önlemler geliştirmede kullanılabilir.
**Sigorta Şirketleri:** Sigorta primlerini daha doğru hesaplamak için tahminler yapılabilir.
**Şehir Planlama:** Yolların güvenliği konusunda veri odaklı kararlar alınabilir.

**Gelecekteki İyileştirmeler:**
Derin öğrenme algoritmaları (LSTM, CNN) ve zaman serisi tahmin modelleri ile daha gelişmiş sonuçlar elde edilebilir.

### Katkılar
Proje geliştirilirken sağlanan katkılar:
- [Kerem Özakça] - Proje geliştiricisi
