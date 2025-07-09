bir ml projesi yaptım
proje şu
arabam.com'dan passat 1.6 bir modele özel fiyat tahmincisi geliştiriyorum
2100 e yakın ilanın linkini web scrapping ile (selenium) çekiyorum
ardından bu linkleri tek tek ziyaret edip ilandaki ilgili verileri dataframe'ime çekiyorum
dataframe'i preprocess, data cleaning, feature engineering işlemleri uygulayarak modellemeye hazır hale getiriyorum
ardından modelimi geliştiriyorum
lineer regresyon, random forest, gradient boosting, xgboost olmak üzere 4 adet modelin parametrelerini optimize ettikten sonra ortak bir final fiyat tahmini yapmaları için voting classifier kullanarak son ortak fiyat tahminini yapıyorum
ve %90 doğruluk ile fiyat tahminimiz yapılmış oluyor