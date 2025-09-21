# Proje Amacı

Geçmiş hava gözlemlerinden faydalanarak bir RNN modeli ile gelecek zaman dilimindeki meteorolojik değişkenleri tahmin etmek. Proje aynı zamanda veri ön işleme (eksik değerleri doldurma, ölçekleme), özellik mühendisliği (zaman gecikmeleri, pencereleme), model eğitimi ve performans görselleştirmesi adımlarını içerir.

## Kullanılan Teknolojiler

Aşağıdaki paketler notebook'tan tespit edilmiştir (en sık kullanılanlar):

* tensorflow, statsmodels, sklearn, numpy, pandas, matplotlib, seaborn, warnings, scipy, 

## Genel olarak beklenen teknoloji yığını:

* Python (pandas, numpy)

* Veri görselleştirme: matplotlib, seaborn, plotly (varsa)

* Model: TensorFlow / Keras veya PyTorch (notebook içeriğine göre belirlenir)

* Model değerlendirme: scikit-learn (metrikler, scaler), statsmodels (opsiyonel)

## Veri Seti

* Malmö şehrinin bir yıllık hava durumu gözlemleri

* Features: datetime, temperature, humidity, wind_speed, pressure vb

## Model Mimarisi

* Model tipi: SimpleRNN

Model tipik olarak şu adımları içerir:

* Zaman serisi verisinin pencerelenmesi (sliding window)

* Özellik ölçekleme (StandardScaler veya MinMaxScaler)

RNN katmanı

* Dense çıktı katmanı (tek değerli regresyon için)

## Değerlendirme metrikleri:

* Model Derleme: Adam Optimizer ve MSE Kayıp Fonksiyonu

* Ölçeklenmiş MSE Metriklerinin Hesaplanması ve Yazdırılması

* from sklearn.metrics import mean_squared_error

* loss = "mean_squared_error"

* metrics= MSE
