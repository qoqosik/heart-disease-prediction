# Makine Öğrenmesi ile Kalp Hastalığı Tahmini

Bu proje, **Veri Analizi** dersi kapsamında geliştirilmiştir.  
Projenin amacı, hasta tıbbi verilerini kullanarak kalp hastalığının varlığını tahmin etmek için veri analizi ve makine öğrenmesi tekniklerini uygulamaktır.

---

## 📊 Veri Seti

- **Kaynak:** Kaggle – Heart Disease Dataset  
- **Gözlem Sayısı:** 1025  
- **Özellik Sayısı:** 13 girdi değişkeni + 1 hedef değişken  
- **Hedef Değişken:** İkili sınıflandırma  
  - `1` — Kalp hastalığı var  
  - `0` — Kalp hastalığı yok  
- **Eksik Veri:** Yok  
- **Sınıf Dağılımı:** Neredeyse dengeli  

---

## 🎯 Problem Tanımı

Bu çalışma, klinik ve demografik özelliklere dayanarak bir hastada kalp hastalığının bulunup bulunmadığını tahmin etmeyi amaçlayan bir **ikili sınıflandırma problemi** olarak ele alınmıştır.

Bu problem, sağlık alanında yanlış negatiflerin ciddi sonuçlara yol açabilmesi nedeniyle önemlidir.

---

## 🧪 Keşifsel Veri Analizi (EDA)

EDA aşamasında veri seti aşağıdaki yöntemler kullanılarak analiz edilmiştir:
- Tanımlayıcı istatistikler
- Hedef değişken dağılımı
- Korelasyon analizi
- Veri görselleştirmeleri (ısı haritaları ve grafikler)

Elde edilen temel bulgular:
- `cp`, `thalach` ve `slope` değişkenlerinin kalp hastalığı ile pozitif korelasyona sahip olduğu gözlemlenmiştir.
- `exang`, `oldpeak`, `ca` ve `thal` değişkenlerinin ise hedef değişken ile negatif korelasyon gösterdiği tespit edilmiştir.

---

## ⚙️ Veri Ön İşleme

- Girdi değişkenleri ve hedef değişken ayrıştırılmıştır.
- Eğitim ve test veri setleri oluşturulmuştur.
- Gerekli durumlarda özellik ölçeklendirmesi uygulanmıştır.
- Veri seti önceden temiz ve tamamen sayısal olduğu için eksik veri doldurma veya kodlama işlemlerine ihtiyaç duyulmamıştır.

---

## 🤖 Makine Öğrenmesi Modelleri

Aşağıdaki makine öğrenmesi modelleri uygulanmış ve değerlendirilmiştir:

### 1. Lojistik Regresyon
- Temel (baseline) model olarak kullanılmıştır.
- Yapısal ve tıbbi veriler için yorumlanabilir ve etkili bir yöntemdir.

### 2. Random Forest
- Topluluk (ensemble) öğrenme yöntemidir.
- Doğrusal olmayan ilişkileri yakalayabilme yeteneğine sahiptir.

---

## 📈 Model Değerlendirme

Modeller aşağıdaki metrikler kullanılarak değerlendirilmiştir:
- Accuracy
- Precision
- Recall
- F1-score
- Confusion Matrix

Özellikle **1 sınıfı (kalp hastalığı var)** için recall metriğine odaklanılmıştır, çünkü sağlık uygulamalarında hastaların doğru şekilde tespit edilmesi yanlış pozitiflerden daha kritiktir.

---

## 🏆 Sonuçlar ve Model Karşılaştırması

- **Lojistik Regresyon** modeli, genel doğruluk oranı açısından daha yüksek bir performans sergilemiş ve kalp hastalığı vakaları için belirgin şekilde daha iyi recall değerine ulaşmıştır.
- **Random Forest** modeli ise daha yüksek precision değerine sahip olmasına rağmen daha düşük recall göstermiştir.

Bu sonuçlara dayanarak, bu problem için **en uygun model olarak Lojistik Regresyon seçilmiştir**.

---

## 🧾 Proje Yapısı
