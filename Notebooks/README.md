# Gözeetimli ve Gözetimsiz Öğrenme Algoritmaları Hakkında

## Akış
1. [Regresyon Modelleri](#regresyon-modelleri)
    1. [Lineer Regresyon](#lineer-regresyon) 
    1. [Polinomal Regresyon](#polinomal-regresyon)
    1. [Multinomal Regresyon](#multinomal-regresyon)
    1. [Destek Vektör Regresyon](#sv-regresyon)
    1. [Gauss Süreci Regresyon](#gauss-süreci-regresyonu)
    1. [Robust Regresyon](#robust-regresyon)
1. [Hem Regresyon Hem Sınıflandırma Modelleri](#regresyon--sınıflandırma-modelleri)
    1. [Karar Ağaçları](#karar-ağaçları)
    1. [Rassal Ormanlar](#rassal-ormanlar)
    1. [Gradient Boosting](#gradient-boosting)
    1. [Ridge Regresyon](#ridge-regresyon)
    1. [Lasso Regresyon](#lasso-regresyon)
    1. [AdaBoost](#adaboost)
    1. [XGBoost](#xgboost)
1. [Sınıflandırma MOdelleri](#sınıflandırma-modelleri)
    1. [Destek Vektör Makineleri](#svm-destek-vektör-makineleri)
    1. [En Yakın Komşu](#nearest-neighbors-en-yakın-komşu)
    1. [Lojistik Regresyon](#logistic-regresyon-ve-türevleri)
    1. [Doğrusal Diskriminant Analizi](#linear-discriminant-analysis-lineer-diskriminant-analizi)
1. [Model Değerlendirme Sonuçları](#model-değerlendirme-sonuçları)
---

## Regresyon Modelleri
### Lineer Regresyon:  
Basit bir doğrusal regresyon modelidir.  

**Avantajları:**
1. Hızlı ve kolayca yorumlanabilir.  
2. Lineer ilişkilere uygundur.  
3. Modelin karmaşıklığı düşüktür.   

**Dezavantajları:**  
1. Non-lineer ilişkileri zayıf modelleyebilir.  
2. Aykırı değerlere duyarlı olabilir.  
3. Bağımlılık varsayımlarını karşılamayan durumlarda performans sorunları olabilir.  


### Polinomal Regresyon
Polinom derecelerini kullanarak regresyon yapar.  

**Avantajları**
1. Esneklik sağlar, karmaşık ilişkileri modelleyebilir.  
2. Çoklu öznitelikleri modelleyebilir.  
3. Çoklu etkileşimleri yakalayabilir.  

**Dezavantajları:**
1. Aşırı derecede karmaşık modeller oluşturabilir.
2. Yüksek dereceli polinomlarda aşırı uyum (overfitting) riski vardır.
3. Veri seti büyüdükçe modelin hesaplama maliyeti artabilir.


### Multinomal Regresyon
Birden fazla kategorik özniteliği olan regresyon problemlerinde kullanılır.  

**Avantajları:**
1. Çoklu kategorik değişkenleri modelleyebilir.  
2. İnteraksiyonları yakalayabilir.  
3. Esnek ve genel bir modeldir.  

**Dezavantajları:**  
1. Yüksek boyutlu verilerde performans sorunları olabilir.
2. Veri setindeki çoklu kategorilerle başa çıkmak zor olabilir.
3. Aşırı uyum riski vardır.  


### SV Regresyon
Destek vektör makineleri kullanarak regresyon yapar.  

**Avantajları:**  
1. Etkili bir şekilde aykırı değerlere dayanabilir.
2. Çok boyutlu veri setleriyle başa çıkabilir.
3. Yüksek boyutlu uzayda iyi performans gösterebilir.

**Dezavantajları:**
1. Hesaplama maliyeti yüksek olabilir.
2. Kernel seçimi ve hiperparametre ayarının zorluğu vardır.
3. Büyük veri setleriyle çalışırken bellek kullanımı sorun olabilir.


### Gauss Süreci Regresyonu
Gauss süreci kullanarak regresyon yapar.  

**Avantajları:**
1. Doğrusal olmayan ilişkileri modelleyebilir.
2. Esnek bir modeldir.
3. Veri setinin boyutu arttıkça hesaplama maliyeti artabilir.

**Dezavantajları:**
1. Veri seti büyüdükçe hesaplama maliyeti artabilir.
2. Çok fazla parametreye sahip modeller oluşturabilir.
3. Overfitting riski vardır.                                 


### Robust Regresyon
Aykırı değerlere dayanıklı regresyon modelidir.  

**Avantajları:**
1. Aykırı değerlere karşı dirençlidir.
2. Lineer ilişkilere uygundur.
3. Modelin hesaplama süresi genellikle hızlıdır.                

**Dezavantajları:**
1. Doğrusal olmayan ilişkileri zayıf modelleyebilir.
2. Hassas hiperparametre ayarına ihtiyaç duyabilir.
3. Yüksek boyutlu veri setlerinde performans sorunları olabilir.

---

## Regresyon & Sınıflandırma Modelleri
### Karar Ağaçları
Karar ağaçları, sınıflandırma ve regresyon problemlerinde kullanılabilen basit ve anlaşılır bir modeldir.

**Avantajları:**

1. Basit ve anlaşılır bir modeldir.
1. Hem sınıflandırma hem de regresyon problemlerinde kullanılabilir.
1. Çoklu öznitelikleri ve etkileşimleri yakalayabilir.

**Dezavantajları:**

1. Overfitting eğilimine sahip olabilir, özellikle ağaç derinleştikçe.
1. Düzgün bir şekilde ayarlanmadığında karmaşık veri yapılarını tam olarak modelleyemeyebilir.
1. Karar ağaçları genellikle yüksek varyansa sahiptir ve aşırı uyum riski taşırlar.


### Rassal Ormanlar
Rassal ormanlar, karar ağaçlarının bir araya getirilerek oluşturulan bir ensemble yöntemidir.

**Avantajları:**

1. Daha güçlü ve karmaşık modeller oluşturabilir.
1. Overfitting riskini azaltabilir.
1. Veri setindeki özniteliklerin önemini değerlendirebilir.

**Dezavantajları:**

1. Eğitim süreci daha yavaş olabilir, çünkü birden fazla ağaç eğitilmelidir.
1. Veri setindeki gürültüye duyarlı olabilir.
1. Ağaçların birleştirilmesi ve sonuçların yorumlanması karmaşık olabilir.


### Gradient Boosting
Gradient boosting, zayıf öğrenicilerin bir araya gelerek güçlü bir model oluşturduğu bir ensemble yöntemidir.

**Avantajları:**

1. Yüksek performanslı tahminler yapabilir.
1. Aşırı uyum riskini azaltabilir.
1. Çoklu öznitelikleri ve etkileşimleri yakalayabilir.

**Dezavantajları:**

1. Daha karmaşık bir model oluşturmak için daha fazla hesaplama kaynağı gerektirebilir.
1. Hiperparametrelerin doğru ayarlanması zor olabilir.
1. Büyük veri setlerinde eğitim süresi uzun olabilir.


### Ridge Regresyon
Ridge regresyon, L2 düzenlemesi kullanarak regresyon yapabilen bir modeldir. L2 düzeltmesi, ağırlıkların karelerinin toplamını kullanarak büyük ağırlıklara ceza verir ve modelin daha istikrarlı bir şekilde çalışmasını sağlar.

**Avantajları:**

1. Çoklu korelasyonlu öznitelikleri ele alabilir.
1. Overfitting eğilimini azaltabilir.
1. İyileştirilmiş genelleştirme performansı sunabilir.

**Dezavantajları:**
1. Öznitelik seçimi yapmak için otomatik bir mekanizma sunmaz, manuel olarak ayarlama yapılması gerekebilir.
1. Ridge regresyonunda kullanılan L2 düzenlemesi, bazı durumlarda gereğinden fazla düzleştirmeye yol açarak önemli öznitelikleri zayıflatabilir.
1. Ridge regresyonu, büyük boyutlu veri setlerinde hesaplama açısından maliyetli olabilir.


### Lasso Regresyon
Lasso regresyon, L1 düzenlemesi kullanarak regresyon yapabilen bir modeldir. L1 düzeltmesi, modelin ağırlıklarını sıfıra yaklaştırarak gereksiz özelliklerin seçilmesini sağlar. Bu özellik seçimi, modelin daha az sayıda önemli özellik üzerinde odaklanmasını ve daha fazla gürültüye duyarlı olmamasını sağlar.

**Avantajları:**

1. Öznitelik seçimi yapmak için otomatik bir mekanizma sunar, gereksiz öznitelikleri sıfıra yakın katsayılarla düşürebilir.
1. Doğrusal olmayan ilişkileri de modelleyebilir.
1. Overfitting riskini azaltabilir ve modelin genelleştirme performansını artırabilir.

**Dezavantajları:**

1. Aykırı değerlere karşı hassas olabilir.
1. Birden fazla yüksek korelasyonlu özniteliğe sahip veri setlerinde seçim yapmak zor olabilir.
1. Büyük boyutlu veri setlerinde hesaplama maliyeti artabilir.


### AdaBoost
AdaBoost, zayıf öğrenicilerin bir araya gelerek güçlü bir sınıflandırma modeli oluşturduğu bir ensemble yöntemidir.

**Avantajları:**

1. Adaptif öğrenme ile model performansını sürekli olarak iyileştirebilir.
1. Hem sınıflandırma hem de regresyon problemlerinde kullanılabilir.
1. Ağırlıklı veri örnekleriyle başa çıkabilir ve veri dengesizliği durumlarında etkilidir.

**Dezavantajları:**

1. Aykırı değerlere duyarlı olabilir.
1. Ağaçların birleştirilmesi ve sonuçların yorumlanması karmaşık olabilir.
1. Veri setindeki gürültüye karşı hassas olabilir.


### XGBoost
XGBoost, Gradient Boosting'in optimize edilmiş bir implementasyonudur.

**Avantajları:**

1. Yüksek performanslı tahminler yapabilir.
1. Aşırı uyum riskini azaltabilir ve genelleştirme yeteneğini artırabilir.
1. Öznitelik önemini değerlendirebilir ve gereksiz öznitelikleri sıfıra yakın katsayılarla düşürebilir.

**Dezavantajları:**

1. Daha fazla hesaplama kaynağı gerektirebilir ve büyük veri setlerinde eğitim süresi uzun olabilir.
1. Hiperparametrelerin doğru ayarlanması zor olabilir.
1. Veri setindeki gürültüye duyarlı olabilir.

---

## Sınıflandırma Modelleri
### SVM (Destek Vektör Makineleri)
SVM, sınıflandırma ve regresyon problemlerinde kullanılan güçlü bir makine öğrenmesi modelidir.

**Avantajları:**

1. Non-lineer ilişkileri de modelleyebilir.
1. Aykırı değerlere dirençlidir.
1. Yüksek boyutlu veri setlerinde etkili olabilir.

**Dezavantajları:**

1. Büyük veri setlerinde hesaplama süresi uzun olabilir.
1. Modelin karmaşıklığı yüksek olduğunda aşırı uyum riski taşır.
1. Kernel fonksiyonunun doğru seçilmesi zor olabilir.


### Nearest Neighbors (En Yakın Komşu)
En Yakın Komşu algoritması, sınıflandırma ve regresyon problemlerinde kullanılan basit ve veriye dayalı bir modeldir.

**Avantajları:**

1. Basit ve anlaşılır bir modeldir.
1. Non-lineer ilişkileri yakalayabilir.
1. Özniteliklerin ölçeklenmesine ihtiyaç duymaz.

**Dezavantajları:**

1. Veri seti büyüdükçe hesaplama maliyeti artabilir.
1. Veri setindeki gürültüye ve aykırı değerlere duyarlı olabilir.
1. Veri setinin yoğunluğuna bağlı olarak performansı değişebilir.


### Nearest Neighbors (En Yakın Komşu)
En Yakın Komşu algoritması, sınıflandırma ve regresyon problemlerinde kullanılan basit ve veriye dayalı bir modeldir.

**Avantajları:**

1. Basit ve anlaşılır bir modeldir.
1. Non-lineer ilişkileri yakalayabilir.
1. Özniteliklerin ölçeklenmesine ihtiyaç duymaz.

**Dezavantajları:**

1. Veri seti büyüdükçe hesaplama maliyeti artabilir.
1. Veri setindeki gürültüye ve aykırı değerlere duyarlı olabilir.
1. Veri setinin yoğunluğuna bağlı olarak performansı değişebilir.


### Logistic Regresyon (ve türevleri)
Logistic Regresyon, sınıflandırma problemlerinde kullanılan bir modeldir.
 
**Avantajları:**

1. Basit ve yorumlanması kolaydır.
1. Olasılık tahminleri yapabilir.
1. Hesaplama süresi genellikle hızlıdır.

**Dezavantajları:**

1. Lineer ilişkileri modellemek için uygundur, doğrusal olmayan ilişkileri zayıf yakalayabilir.
1. Öznitelikler arasındaki çoklu korelasyona duyarlı olabilir.
1. Veri setindeki dengesizlik durumlarında performans sorunları olabilir.


### Linear Discriminant Analysis (Lineer Diskriminant Analizi)
Lineer Diskriminant Analizi, sınıflandırma problemlerinde kullanılan bir modeldir.

**Avantajları:**

1. Yüksek boyutlu veri setlerinde etkili olabilir.
1. Veri setindeki sınıf ayrımını iyileştirebilir.
1. Sınıf sınırlarını belirlemek için kullanışlı öznitelikler sağlayabilir.

**Dezavantajları:**

1. Veri setinde sınıflar arasındaki dağılım dengesiz ise model performansı etkilenebilir.
1. Öznitelikler arasındaki ilişkiler lineer değilse modelin performansı düşebilir.
1. Veri setindeki gürültüye karşı hassas olabilir.

---

## Model Değerlendirme Sonuçları
