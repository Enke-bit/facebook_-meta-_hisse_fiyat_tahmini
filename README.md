# Facebook Hisse Senedi Tahmini LSTM ile
Bu proje, Facebook (Meta) hisse senedi fiyatlarını bir yıl ileriye dönük tahmin etmek için Long Short-Term Memory (LSTM) sinir ağı modelini kullanmaktadır. Bu analizde kullanılan veri seti Kaggle'dan alınmıştır ve Facebook'un tarihsel hisse senedi verilerini içermektedir.

## Veri Seti
Bu projede kullanılan veri seti, Facebook'un (Meta) tarihsel hisse senedi fiyatlarını içermektedir. Veri seti aşağıdaki sütunları içermektedir:

- Date: Tarih
- Open: Açılış fiyatı
- High: Gün içindeki en yüksek fiyat
- Low: Gün içindeki en düşük fiyat
- Close: Kapanış fiyatı
- Volume: İşlem hacmi
- Veri seti, Facebook'un tarihsel hisse senedi performansını değerlendirmek ve gelecekteki fiyatları tahmin etmek için kullanılmıştır.

  ## model yapısı

  Model: "sequential_8"
_________________________________________________________________
 Layer (type)                Output Shape              Param #   
=================================================================
 lstm_16 (LSTM)              (None, 60, 50)            10400     
                                                                 
 dropout_16 (Dropout)        (None, 60, 50)            0         
                                                                 
 lstm_17 (LSTM)              (None, 50)                20200     
                                                                 
 dropout_17 (Dropout)        (None, 50)                0         
                                                                 
 dense_16 (Dense)            (None, 25)                1275      
                                                                 
 dense_17 (Dense)            (None, 1)                 26        
                                                                 
=================================================================
Total params: 31901 (124.61 KB)
Trainable params: 31901 (124.61 KB)
Non-trainable params: 0 (0.00 Byte)
_________________________________________________________________

## Kullanılan Kütüphaneler
Bu projede aşağıdaki kütüphaneler ve modüller kullanılmıştır:

- pandas: Veri işleme ve analiz için
- numpy: Sayısal hesaplamalar için
- matplotlib: Veri görselleştirme için
- sklearn.preprocessing.MinMaxScaler: Özellik ölçekleme için
- tensorflow.keras.models ve tensorflow.keras.layers: LSTM modelini oluşturma ve eğitme için
- datetime.timedelta: Tarih işlemleri için

 ##  Değerlendirme
Modelin performansı Mean Squared Error (MSE) ile değerlendirilmiştir. Bu model için MSE yaklaşık 106.31 olup, tahminlerin gerçek fiyatlara ortalama kare farkını göstermektedir.

## Katkıda Bulunma
Projeye katkıda bulunmaktan çekinmeyin; sorun bildirebilir veya pull request gönderebilirsiniz. Geri bildirim ve önerileriniz memnuniyetle karşılanacaktır.

## Lisans
Bu proje MIT Lisansı altında lisanslanmıştır. Detaylar için LICENSE dosyasına bakabilirsiniz.

## İletişim
Herhangi bir soru veya bilgi için ibrahimpuskullu44@gmail.com ile iletişime geçebilirsiniz.
