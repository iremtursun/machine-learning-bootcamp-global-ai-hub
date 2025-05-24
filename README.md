**Global AI Hub - Akbank Makine Öğrenmesine Giriş Bootcamp Projesi**

**GİRİŞ**

Akbank ve Global AI Hub işbirliğinde hazırlanan Makine Öğrenmesine Giriş Bootcamp'ine proje konusu olarak dahil edeceğim Avustralya'da yağan yağmurların günlük verilerine ulaşabileceğimiz bir dataset üzerinden projeyi oluşturacağız. Kapsam dahilinde makine öğrenmesi algoritmalarından denetimli öğrenme çeşitlerini inceleyecek ve modellerin doğruluk, kesinlik, tahmini değerlerine göre yorumlarda bulunacağız.

Notebook ve dataset erişimi için kullanabileceğiniz Kaggle linki: https://www.kaggle.com/code/iremtursun/machine-learning-bootcamp-global-ai-hub

Veri setini almak için kullandığım kaynak: https://www.kaggle.com/datasets/jsphyg/weather-dataset-rattle-package/data

**TANIM**

Avustralya'da 01.12.2008 - 25.06.2017 seneleri arasında günlük olarak yağmur yağan bölgelerle birlikte işlenen datalar **weatherAUS.csv** dosyasında bulunmaktadır. Veri seti yağmur yağmasına etki eden sıcaklık, basınç, yağış miktarı, güneş ışığı miktarı, rüzgar hızı, nem ve ertesi günün yağmur yağmasına göre hazırlanan faktörleri içermektedir. Meteorolojik verilerin yer aldığı bu sette ana konumuz yarın yağmur yağıp yağmama olasılığını değerlendirmektir.

Ayrıca bu data .csv dosyasından ilk okunan değerlere göre 23 sütun, 145.460 satırdan oluşarak büyük bir datayı simgelemektedir.

Buradaki amacımız ana etkenlere bağlı kalarak "Avustralya'da yarın yağmur yağacak mı?" sorusunu tahminleyen modeli oluşturmaktır. Bu bir sınıflandırma problemi olduğu için Karar Ağaçları, SVM ve Lojistik Regresyon modelleri arasındaki değerlendirmeleri inceleyeceğiz.

**UYGULAMA**,

Uygulama aşamasında belirli başlıklar altında işlemlerimizi gerçekleştirdiğimiz faaliyet kısmıdır. Öncelikle notebook üzerinden keşifsel veri analizi yaptık, verilerimizi ve değişkenlerimizi tanıdık. Ardından temel betimleyici istatistikleri sunarak markdown üzerinden tanımlamalar sunduk.

Makine öğrenmesi modellerinin iyi performans gösterebilmesi için datanın ön işlemden geçmesi gerekir. Preprocessing işlemlerini yaparak kategorik ve float değerlerimiz için ayrı ayrı çalıştık. Kategorik değişkenler için LabelEncoding yaparak NaN değerleri doldurduk; benzerini float değerler için de yaparak NaN/eksik değerlerin belirlenmesi, doldurulması, aykırı değerlerin bulunması ve çözümlenmesi gibi birçok adımdan oluşturduk. Herbir işlemi grafiksel çizimlerle destekledik.

Korelasyon matrisi üzerinden özellik seçimi yaptık ve tahmin etmeye çalıştığımız **RainTomorrow** değişkeni için hangi özelliklerin ayırt edici, anlamlı olduğunu keşfettik. 

SVM, Lojistik Regresyon ve Karar Ağacı modelleri üzerinden datamızın %80'i eğittik, %20'sini test ettik. F1-score, Recall, Confusion matrisine bakarak yorumlarda bulunduk ve optimal modeli seçerek yolumuza devam ettik.

**SONUÇ**

**KAYNAKLAR**

1. https://www.kaggle.com/datasets/jsphyg/weather-dataset-rattle-package/data
2. https://bulutistan.com/blog/lojistik-regresyon-nedir/
3. https://github.com/gokerguner/example-repo/blob/main/supervised.ipynb
4. https://www.kaggle.com/code/goker67/everything-on-gpu-ml-with-cuml-polars-cupy
5. https://ravenfo.com/2021/02/11/aykiri-deger-analizi/
6. https://www.grammarly.com/blog/ai/what-is-decision-tree/
7. https://www.unite.ai/tr/what-are-support-vector-machines/
8. https://cmap-repos.github.io/cmapplot/articles/colors.html
9. https://gokerguner.medium.com/machine-learning-1-7d4581caa291
