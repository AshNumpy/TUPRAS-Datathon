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