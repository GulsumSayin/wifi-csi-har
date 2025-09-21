# 📡 Wi-Fi Kanal Durumu Bilgisine (CSI) Dayalı İnsan Aktivitesi Tanıma Projesi

## 📖 Proje Hakkında

Bu proje, Wi-Fi Kanal Durumu Bilgisi (CSI) kullanarak insan aktivitelerini tanımayı amaçlamaktadır.
CSI, Wi-Fi sinyallerinin ortamda geçerken uğradığı değişiklikleri ölçer; bu değişiklikler insan hareketlerinden kaynaklanır.

Veri seti, farklı odalarda 7 farklı aktiviteyi içermektedir:

🚶‍♂️ Yürüme
💺 Oturma
🧍‍♂️ Ayakta durma
🛌 Yatma
↗️ Kalkma
↘️ Yere inme
🏠 Boş oda

Projede kullanılan derin öğrenme modelleri, bu zaman serisi CSI verilerini işleyerek her paket için doğru aktivite sınıfını tahmin eder. Böylece kablosuz sinyaller üzerinden insanların günlük hareketlerini doğru ve gizlilik dostu bir şekilde tanımak mümkün olur.

## 🎯 Amaç

- İnsan aktivitelerini kablosuz sinyaller üzerinden tespit etmek.

- Sensör tabanlı sistemlere göre daha az maliyetli ve gizlilik dostu bir yöntem sunmak.

- Derin öğrenme modelleri ile yüksek doğruluk sağlamak.

## 📂 Veri Seti

- HAR with Wi-Fi CSI veri seti kullanılmıştır.

- Veri seti, farklı odalarda yapılan insan aktivitelerini içerir.

- Kaynak: https://doi.org/10.6084/m9.figshare.14386892.v1

- Veri yapısı:

room1/
    1/
        data.csv
        label.csv
room2/
    ...


## ⚙️ Kurulum

- Depoyu klonlayın:
  ```bash
  git clone https://github.com/GulsumSayin/wifi-csi-har.git

- Gerekli Python paketlerini yükleyin:
  ```bash
  pip install numpy pandas scikit-learn tensorflow matplotlib

- Colab kullanıyorsanız Drive’ı bağlayın:
   ```bash
   from google.colab import drive
   drive.mount('/content/drive')

## 🛠️ Kullanım

- Veri yükleme ve ön işleme yapılır.

- CNN tabanlı bir model ile eğitim yapılır.

- Model kaydedilir ve test seti ile doğruluk ölçülür.

- Örnek kullanım:
    ```bash
    # Model eğitimi 
    history = model.fit(X_train, y_train_cat, validation_data=(X_test, y_test_cat), epochs=100)

    # Model kaydetme
    model.save("/content/drive/MyDrive/csi_har.h5")

## 🤝 Katkıda Bulunma

- Pull request ile katkıda bulunabilirsiniz.

- Lütfen mevcut kod yapısına ve standartlara uygun değişiklikler yapın.

## 📄 Lisans

Bu proje MIT Lisansı ile lisanslanmıştır.
