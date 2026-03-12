# Wtech Big Data Bootcamp
## Final Proje Dokümanı

---

### Uçtan Uca Big Data Pipeline Projesi

Olist Brazilian E-Commerce veri seti üzerinde uçtan uca bir veri mühendisliği pipeline'ı kurmanızı, veriyi analiz etmenizi ve iş sorularına cevap veren anlamlı çıktılar üretmenizi bekliyoruz.

[Olist Brazilian E-Commerce](https://www.kaggle.com/datasets/olistbr/brazilian-ecommerce)

Projenizi aşağıdaki gereksinimlere uygun olarak geliştirmeniz gerekiyor.

---

### Veri Seti

Bu projede kullanılacak veri seti Kaggle üzerindeki **Brazilian E-Commerce Public Dataset by Olist** veri setidir.

- **Kaynak:** https://www.kaggle.com/datasets/olistbr/brazilian-ecommerce
- **Boyut:** ~100K sipariş, 9 ayrı CSV dosyası
- **Tablolar:** orders, order_items, customers, sellers, products, payments, reviews, geolocation
- **Dönem:** 2016 – 2018

Bu veri seti gerçek bir Brezilya e-ticaret platformuna ait anonimleştirilmiş verilerden oluşmaktadır. Birden fazla tablonun ilişkisel olarak birbirine bağlı olması, hem SQL hem de Spark becerilerinizi uygulamanız için ideal bir ortam sunmaktadır.

---

### 1) Veri Keşfi ve Temizleme (EDA)

Pandas, Matplotlib ve Seaborn kullanarak veri setini keşfedin ve temizleyin.

Beklentiler:
- Her tablonun yapısı, satır/sütun sayısı, veri tipleri hakkında genel bakış
- Eksik ve tutarsız verilerin tespiti ve ele alınması
- Temel istatistiksel özetler (ortalama, medyan, standart sapma vb.)
- En az **5 anlamlı görselleştirme** (dağılım, trend, korelasyon, kategori bazlı karşılaştırma vb.)
- Portekizce kategori isimlerinin İngilizce'ye çevrilmesi (translation tablosu ile)
- EDA bulgularının markdown hücrelerinde açıkça yorumlanması
- Analize ve raporlamaya uygun tek bir csv dosyasını hazırlayın

---

### 2) SQL Katmanı

Veriyi SQLite veritabanına yükleyin ve iş sorularına SQL ile cevap verin.

Beklentiler:
- En az 2 tabloyu SQLite veritabanına yükleme
- Tablolar arası **JOIN** kullanmayı gerektiren en az **5 SQL sorgusu** yazma
- Sorguların her birinin hangi iş sorusuna cevap verdiğinin açıklanması

Örnek iş soruları (bunlarla sınırlı değilsiniz):
- Aylık toplam gelir trendi nasıl değişiyor?
- En çok gelir getiren ilk 10 ürün kategorisi hangileri?
- Ortalama teslimat süresi şehirlere göre nasıl farklılaşıyor?
- Müşteri memnuniyet skoru ile teslimat süresi arasında bir ilişki var mı?
- Hangi ödeme yöntemleri en yüksek ortalama sipariş değerine sahip?

---

### 3) PySpark ile Veri Dönüştürme

Aynı veri seti üzerinde PySpark kullanarak dönüştürme işlemleri gerçekleştirin.

Beklentiler:
- CSV dosyalarını PySpark DataFrame olarak okuma
- En az **3 farklı transformation** işlemi (gruplama, filtreleme, yeni kolon türetme, window function vb.)
- Spark işlemlerinin Pandas'taki karşılıklarıyla kısa bir karşılaştırma/yorum
- İşlenmiş verinin dosyaya (CSV veya Parquet) yazılması

---

### 4) Basit ETL Pipeline

Veriyi okuyup, dönüştürüp, hedef bir formatta yazan basit bir ETL akışı oluşturun.

Beklentiler:
- **Extract:** Ham CSV dosyalarını okuma
- **Transform:** Temizleme, birleştirme, yeni metrikler türetme (örn: sipariş başına ortalama gelir, teslimat performans skoru vb.)
- **Load:** Sonuçları temiz bir formatta kaydetme (SQLite tablosu, Parquet dosyası veya temiz CSV)
- Bu akışın tek bir Python scripti (`etl_pipeline.py`) olarak çalıştırılabilir olması

---

### 5) Sonuçların Sunumu

Analiz bulgularınızı anlaşılır bir şekilde sunun.

Beklentiler:
- Jupyter Notebook içinde bulgularınızı özetleyen bir **sonuç/özet bölümü**
- En az **3 iş önerisi** (veriye dayalı, "bu veriye göre şunu öneriyorum" formatında)
- Görselleştirmelerle desteklenmiş açıklamalar

---

### Repo Yapısı ve README

Projenizi bir **GitHub reposu** olarak teslim etmeniz gerekmektedir.

Örnek repo yapısı:
```
olist-data-pipeline/
├── README.md
├── requirements.txt / uv / poetry
├── data/                  # Ham ve işlenmiş veri dosyaları (.gitignore ile hariç tutulabilir)
├── notebooks/
│   ├── 01_eda.ipynb
│   ├── 02_sql_analysis.ipynb
│   └── 03_spark_transformations.ipynb
├── src/
│   └── etl_pipeline.py
└── outputs/               # Nihai çıktılar (görseller, temiz veri, raporlar)
```

README.md içeriği:
- Proje başlığı
- Projenin ne kapsamda yapıldığı ve amacı
- Veri seti hakkında kısa bilgi
- Kullanılan teknolojiler
- Proje yapısı
- Kurulum ve çalıştırma adımları
- Bulgular ve iş önerileri özeti
- İletişim

---

### Olsa Güzel Olur

Zorunlu olmayan fakat yapıldığında projeyi bir adım öne taşıyan özellikler.

- **Git Geçmişi:** Projenin adım adım gelişimini gösteren düzenli commit'ler 
- **Dockerize:** Projeyi bir Dockerfile ile paketleme, `docker build` ve `docker run` ile çalıştırılabilir hale getirme
- **Airflow DAG:** ETL pipeline'ını basit bir Airflow DAG'ı olarak kurgulama
- **Veritabanına Yükleme:** SQLite yerine BigQuery/PostgreSQL veya başka bir veritabanına yükleme
- **Dashboard:** PowerBI, Streamlit veya benzeri bir araçla interaktif dashboard oluşturma
- **Medium Yazısı:** Projenin teknik kısımlarını adım adım anlatan bir blog yazısı

---

Kolay gelsin :)