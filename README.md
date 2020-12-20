## K-means ve Hiyerarşik Kümeleme Yöntemlerini Kullanarak Müşteri Segmentasyonu

Segmentasyonun amacı; müşterileri alım gücüne göre çeşitli gruplara ayırmak ve çıkan sonuçlara göre reklam ya da pazarlama politikasını belirlemektir. Veri seti için Kaggle platformundan alınmış veri seti kullanılmıştır. Alım gücüne göre müşteri segmentasyonu yapılacağı için gelir düzeyi (Income) ve borç-gelir oranı(DebtIncomeRatio) değişkenleri kullanılmıştır. 

## K-means Yöntemi

K değeri küme sayısını belirler. Bu nedenle, uygulamaya geçmeden önce küme sayısı belirlenmelidir. Aşağıda yöntemin adımları verilmiştir.

```
K küme sayısını seç ve K kadar ağırlık merkezini rastgele ata.
Repeat
Kayıtları en yakın ağırlık merkezinin olduğu kümeye ata.
Her kümenin ağırlık merkezini kayıtların ortalamasını alarak hesapla.
Until: Merkezler değişmeyinceye kadar yeni iterasyona başla.
```
Bu yöntemde kümelemenin doğru olması için uygun K değerinin seçilmesi, dağılımın dairesel olması ve aykırı değerlerin olmaması etkendir.

## Hiyerarşik Kümeleme Yöntemi

İlk başta her elemanın bir küme sayıldığı ve veri setinin tamamını bir kümede toplayana kadar kümeleme işleminin yapıldığı Aglomeratif, bütün kümenin tek bir kayıt kalana kadar parçaladığı Bölücü olarak iki çeşidi vardır. Aşağıda Aglomeratif yöntemin adımları verilmiştir.
```
Her bir kayıt verisi için yakınlık matrisi hesapla.
Her bir noktayı küme olarak al.
Repeat
En yakın iki kümeyi matris üzerinde bul ve birleştir. 
Yakınlık matrisini bir yöntem kullanarak güncelle.
Until: Veri setini tek bir kümede toplayıncaya kadar yeni iterasyona devam et.

```
Yakınlık matrisini güncellerken Min(en yakın komşu), Max(en uzak komşu), Grup ortalama ve Ward metodu gibi yöntemler kullanılmaktadır.

## Normalizasyon Yöntemi

Normalizasyon işlemi, değerlerin belirli aralıklara indirgenmesidir. Kümeleme yöntemlerinde iki değişkenin de eşit etkiye sahip olması ve kümelemenin doğru bir şekilde gerçekleştirilmesi için normalizasyon işlemi yapılmıştır.

## Kullanılan Teknojiler

- Veri setinin tutulması ve üzerinde işlem yapılabilmesi için Pandas kütüphanesi.

- K-Ortalamalar ve Hiyerarşik kümeleme için Scikit-learn ve SciPy kütüphanesi.

- Veri görselleştirme için Matplotlib kütüphanesi.

## Veri Seti

Veri setinde 850 kayıt vardır. Bu projede ilk 500 kayıt kullanılmıştır. Her iki kümeleme yönteminde de gelir düzeyi (Income) ve borç-gelir oranı(DebtIncomeRatio) değişkenleri kullanılmış, diğer değişkenler veri setinden çıkarılmıştır.

https://www.kaggle.com/yashgupta011/customer-segmentation-dataset

## Faydanılan Kaynaklar

Veri Bilimi ve Makine Öğrenmesi Kursu - Udemy - Mustafa Vahit Keskin