## Problem Hakkında

Yarışma boyunca TÜPRAŞ’ta bir Veri Bilimci rolü üstlenilecektir. TÜPRAŞ Veri Analitiği ekibinin bir üyesi olarak İngiltere’de bulunan Tüpraş Trading Ltd. iştirakinde kritik öneme sahip olacak bir proje tamamlanması istenmektedir.  

Traderlar tarafından bir hafta sonra benzin ürününde oluşacak talebi tahminleyen bir model üretilmesi beklenmektedir. Modellemeyi yaparken kullanılabilecek veriler ticaret uzmanlarının alan bilgisi dahilinde filtrelenerek paylaşılmıştır `../Datasets/`.  

Oluşturulacak olan model talebin eksiksiz sağlanması, ticari karlılık, yerinde/zamanında lojistik, stok yönetimi ve sürdürülebilirlik gibi birçok konuda kritik değer yaratacaktır.  

## Veri Seti Hk.

|Değişken|Açıklama|
|:-------|-------:|
|period |Tarih|
|gasoline_imports |Benzin ürünü ithalat miktarı|
|gasoline_exports |Benzin ürünü ihracat miktarı|
|crude_imports |Ham petrol ithalat miktarı|
|crude_exports |Ham petrol ihracat miktarı|
|gasoline_stocks |Depolarda bulunan benzin miktarı|
|crude_stocks |Depolarda bulunan ham petrol miktarı|
|distillate_fuel_stocks |Depolarda bulunan dizel türü yakıt miktarı|
|jet_stocks |Depolarda bulunan jet yakıtı miktarı|
|propane_stocks |Depolarda bulunan propan miktarı|
|gasoline_net_input |Benzin üretimi için kullanılan girdi miktarı|
|gasoline_output |Rafineriler tarafından üretilen benzin miktarı|
|distillate_fuel_output |Rafineriler tarafından üretilen dizel miktarı|
|jet_output |Rafineriler tarafından üretilen jet yakıtı miktarı|
|propane_output |Rafineriler tarafından üretilen propan miktarı|
|residual_fuel_output |Rafineriler tarafından üretilen diğer yakıt miktarı|
|conventional_gasoline_spot_price |Benzin piyasa değeri/fiyatı|
|crude_brent_spot_price |Ham petrol piyasa değeri/fiyatı|
|gasoline_future_price1 |Vadeli işlemlerde 1 ay ötelemeli benzin fiyatı|
|gasoline_future_price2 |Vadeli işlemlerde 2 ay ötelemeli benzin fiyatı|
|gasoline_future_price3 |Vadeli işlemlerde 3 ay ötelemeli benzin fiyatı|
|gasoline_future_price4 |Vadeli işlemlerde 4 ay ötelemeli benzin fiyatı|
|gasoline_demand |Benzin talep miktarı|
|target |Hedef değişken, bir hafta sonraki benzin talebi|

## Veri Setinin Hazırlanması
Veri işleme sürecinde gerekli ön işlemeler yapıldı (**bkz:**`./Notebooks/1-Exploring.ipynb` & `./Notebooks/File-Manipulation.ipynb`)

Verilerin incelenme sürecinde 2020 yılı Mart ayında keskin bir düşüş yaşandığı görüldü ve buna istinaden pandeminin başlamasını veri setine bir şekilde eklenilmeli şeklinde düşünüldü ve vaka sayısı ile ölüm sayısı değerleri dış veri olarak veri setine eklendi.

Özellik çıkarımı ile tarih sütunu kullanılarak yeni özellikler oluşturuldu (**bkz:**`./Notebooks/1-Exploring.ipynb`). 

## Makine Öğrenmesi & Derin Öğrenme
Makine öğrenmesi sürecinde çeşitli analizler ve modeller uygulandı (**bkz:**`./Notebooks/5-ML-Study.ipynb`)

Çeşitli modeller çeşitli sebeplerden ötürü denendi/denenmedi. Sonuç olarak aşağıdaki tablo elde edildi:

<div align="center">

|Model                      |RMSE  |MAE   |MAPE |
|:--------------------------|:----:|:----:|:---:|
|Random Forest Regressor|621.09| 448.77|0.047|
|Gradient Boosting Regressor|649.97|492.16|0.052|
|XGBoost Regressor|674.70|472.43|0.050|
|Ridge Regressor|887.15|643.06|0.070|

</div>

<hr width=410>

**Not:**  
Tahmin edilmesi istenilen hedef değişkenin ortalaması: 9635.77

Derin öğrenme sürecinde sadece zamana bağlı değişimi olan hedef değişkeni kullanılarak LSTM modelleri kuruldu ancak en iyi performansı sergileyen LSTM modeli yine de makine öğrenmesi modellerinin önüne geçemedi.

Ancak LSTM modeli değişkendeki dalgalamayı çok iyi yakaladığı için LSTM modelinin tahmin değerleri yeni bir özellik şeklinde veri setine dahil edilip tekrardan makine öğrenmesi modellerine girdi şeklinde verildi:
