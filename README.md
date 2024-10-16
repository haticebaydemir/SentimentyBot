# SentimentyBot
# Tweetlerde Duygu Analizi

Bu proje, tweetlerde duygu analizi yapmak için lojistik regresyon ve TF-IDF vektörizasyonu kullanmayı amaçlamaktadır. Ana hedef, tweetleri üç duygu kategorisine (pozitif, negatif ve nötr) sınıflandırmaktır.
Miuul NLP kursu bitirme projesidir.

## İçindekiler
- Giriş
- Veri Seti
- Özellikler
- Başlarken
- Kullanım
- Sonuçlar

## Giriş
Duygu analizi, sosyal medya platformları aracılığıyla kamuoyunun farklı konular hakkındaki görüşlerini anlamak için güçlü bir araçtır. Bu proje, etiketlenmiş veriler temelinde tweetleri analiz etmek ve duygu durumlarını sınıflandırmak için makine öğrenimi tekniklerinden faydalanmaktadır.

## Veri Seti
Proje iki CSV dosyası içermektedir:
- `tweets_labeled.csv`: Duygu etiketleri (1 pozitif, -1 negatif, 0 nötr) ile birlikte tweetleri içerir.
- `tweets_21.csv`: Duygu tahminleri yapılacak yeni tweetleri içerir (2021 yılından).

## Özellikler
- **Veri Temizleme**: Eksik değerlerin ve tarih formatlarının işlenmesini sağlar.
- **Özellik Mühendisliği**: Tweet tarihinden mevsimler ve zaman aralıkları gibi ek özellikler üretir.
- **Metin İşleme**: Metinleri küçük harfe çevirir ve TF-IDF uygulayarak özellik çıkarımı yapar.
- **Lojistik Regresyon Modeli**: Duygu sınıflandırması için bir lojistik regresyon modeli eğitir.
- **Tahmin**: Eğitilen model kullanılarak yeni tweetlerin duygu durumlarını tahmin eder.

## Başlarken

### Gereksinimler
- Python 3.x
- Gerekli kütüphaneler:
  ```bash
  pip install numpy pandas scikit-learn seaborn matplotlib
```
## Kodu Çalıştırma
1. Depoyu klonlayın:
  ```bash
  git clone https://github.com/kullaniciadi/depo-adi.git
cd depo-adi
```
2. Google Drive'ı bağlayın (Google Colab kullanıyorsanız):
  ```bash
from google.colab import drive
drive.mount('/content/drive')
```
3. Ana scripti çalıştırın: İşlemleri başlatmak için scripti çalıştırın.
  ```bash
python main.py
```
### Not
Scriptte veri seti dosyalarınızın yollarını güncellemeyi unutmayın.

## Kullanım
- Scripti çalıştırdıktan sonra, `tweets_21.csv `dosyasındaki tweetlerin duygu tahminleri label adlı yeni bir sütunda kaydedilecektir.

## Sonuçlar
Lojistik regresyon modelinin doğruluğu çapraz doğrulama ile değerlendirilmiştir. Script tarafından üretilen grafiklerle etiketlenmiş veri setindeki duygu dağılımını görselleştirebilirsiniz.
