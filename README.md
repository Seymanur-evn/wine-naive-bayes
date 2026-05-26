# wine-naive-bayes
Veri Madenciliği projesi - UCI Wine veri seti üzerinde Gaussian Naïve Bayes yöntemiyle yapılmış bir sınıflandırma.

BLM0463 — Veri Madenciliğine Giriş — Dönem Projesi
Hazırlayan: Şeymanur Evin


Proje Hakkında
Bu projede, üç farklı İtalyan üzüm çeşidinden (Barolo, Grignolino, Barbera) üretilen şarapların 13 kimyasal ölçümüne bakarak, bir şarabın hangi çeşide ait olduğunu tahmin eden bir model geliştirilmiştir. Yöntem olarak, olasılık temelli bir sınıflandırıcı olan Gaussian Naïve Bayes kullanılmıştır.
Veri Seti

Kaynak: UCI Machine Learning Repository - Wine
Örnek sayısı: 178
Özellik sayısı: 13 (tümü sürekli sayısal kimyasal ölçümler)
Sınıf sayısı: 3 — Barolo (59), Grignolino (71), Barbera (48)
Eksik veri: Yok

Kullanılan Yöntemler ve Kütüphaneler

Python (Google Colab)
scikit-learn (model ve değerlendirme)
pandas, numpy (veri işleme)
matplotlib, seaborn (görselleştirme)

Çalışmanın Adımları

Veri setinin yüklenmesi ve incelenmesi
Keşifsel veri analizi ve görselleştirme (sınıf dağılımı, kutu grafikleri)
Verinin %70 eğitim / %30 test olarak ayrılması (stratified)
Gaussian Naïve Bayes modelinin eğitilmesi
Değerlendirme: accuracy, precision, recall (sensitivity), specificity, F1-skoru ve confusion matrix
5 katlı çapraz doğrulama ile sonucun doğrulanması
Bir akademik çalışmayla karşılaştırma

Sonuçlar
DeğerlendirmeDoğrulukTek bölünme (random_state=42)%100,005 Katlı Çapraz Doğrulama (ortalama)%96,63 (± %2,11)
İlk test bölünmesinde elde edilen %100'lük sonuç, tek bir şanslı bölünmeden kaynaklandığı için çapraz doğrulama ile sınanmış ve modelin gerçek genelleme başarısının yaklaşık %96–97 olduğu görülmüştür.
Akademik Karşılaştırma
Sonuçlar, aynı veri setini kullanan Arafat ve arkadaşlarının (2025) çalışmasıyla karşılaştırılmıştır:
YöntemDoğrulukGaussian Naïve Bayes (Bu Çalışma)%96,63 (± %2,11)Logistic Regression (Arafat ve ark., 2025)%98,15L1 Düzenlileştirmeli LR (Arafat ve ark., 2025)%93,52
Naive Bayes, basit bir yöntem olmasına rağmen optimize edilmiş yöntemlerle yarışabilecek bir başarı göstermiştir.
Karşılaştırılan çalışma: arXiv:2510.14449
Nasıl Çalıştırılır?

Wine_Naive_Bayes.ipynb dosyasını Google Colab ile açın.
Hücreleri sırayla çalıştırın (Runtime → Run all).
Gerekli kütüphaneler Colab'da hazır olduğu için ek kurulum gerekmez.

Referanslar

Aeberhard, S., & Forina, M. (1991). Wine [Veri seti]. UCI Machine Learning Repository.
Arafat, J., Tasmin, F., & Poudel, S. (2025). Feature Selection and Regularization in Multi-Class Classification. arXiv:2510.14449.
Pedregosa, F. ve ark. (2011). Scikit-learn: Machine Learning in Python. JMLR, 12, 2825–2830.
