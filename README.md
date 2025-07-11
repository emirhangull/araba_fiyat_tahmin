# ArabaTahmincim

# Passat 1.6 Fiyat Tahmincisi

Bu proje, **arabam.com** sitesinden toplanan verilere dayanarak, Volkswagen Passat 1.6 model araçlar için fiyat tahmini yapan bir makine öğrenmesi uygulamasıdır.

## Projenin Amacı

2. el Passat 1.6 modelleri için fiyat tahmininde bulunmak. Böylece kullanıcılar bir aracın fiyatının piyasa ortalamasına ne kadar uygun olduğunu görebilir.

## Nasıl Çalışıyor?

1. **Veri Toplama (Web Scraping):**

   * arabam.com'dan 2100'e yakın Passat 1.6 ilanının linki Selenium ile çekildi.
   * Bu linkler tek tek ziyaret edilerek aracın yaşı, kilometresi, şanzıman türü, yakıt türü, model detayları, hasar geçmişi gibi bilgiler alındı.

2. **Veri Hazırlık ve Özellik Mühendisliği:**

   * Eksik veya bozuk veriler düzenlendi.
   * Sayısal dönüşümler ve one-hot encoding uygulandı.
   * Aracın yaşını temsil eden `arac_yasi`, tüm parçaların orijinal olup olmadığını gösteren `hepsi_orijinal`, boyalı parça sayısına dayalı `agirlikli_hasar_skoru`, ve log fiyat (`log_fiyat`) gibi özel özellikler eklendi.

3. **Modelleme:**

   * Fiyat tahmini için 4 farklı model kullanıldı:

     * Doğrusal Regresyon (Linear Regression)
     * Random Forest
     * Gradient Boosting
     * XGBoost
   * Her model Grid Search yöntemiyle optimize edildi.

4. **Fiyat Tahmini (Voting Regressor):**

   * Tüm modellerin çıktıları birleştirilerek son bir tahmin oluşturuldu.
   * Yaklaşık %90 doğruluk oranına ulaşıldı.


## Kullanılan Araçlar

* Python
* Selenium
* Pandas, NumPy
* XGBoost
* Scikit-Learn 
## Sonuç

Bu proje, belirli bir ikinci el model için fiyat tahmini yaparak hem makine öğrenmesi yöntemlerini göstermekte hem de gerçek dünya verisiyle çalışmanın uygulamasını sunmaktadır. Özelleştirilmiş özellik mühendisliği sayesinde tahmin başarımı oldukça yüksektir.

---

*Her türlü görüş ve katkıya açığım. Forklayıp geliştirebilir ya da issue açarak geri bildirimde bulunabilirsiniz!*

<img width="707" height="699" alt="image" src="https://github.com/user-attachments/assets/f1965354-cdf9-445f-85a7-db54e6395c09" />

