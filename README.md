# Sekans - Film Önerme Uygulaması 🎬

Sekans, kullanıcılara izledikleri veya beğendikleri filmlere benzer içerikleri gelişmiş makine öğrenmesi algoritmalarıyla sunan tam yığın (full-stack) bir web uygulamasıdır. Proje, veri işleme hızı ile zengin görsel performansı bir arada sunmak adına hibrit bir veri mimarisi üzerine inşa edilmiştir.

---

## 🚀 Proje Hakkında ve Mimari Yaklaşım

Sekans, geleneksel sistemlerden farklı olarak veri yönetimini iki koldan yürütür:
1. **Yerel Veri ve Algoritmik Süreç:** Sistem performansını optimize etmek ve API kota sınırlarına takılmamak amacıyla; film isimleri, türler, oyuncu kadroları ve özet metinleri yerel `.csv` veri setleri üzerinden okunur. İçerik tabanlı filtreleme algoritması (TF-IDF ve Kosinüs Benzerliği) bu yerel veriler üzerinde çalışır.
2. **Dinamik Medya Entegrasyonu:** Algoritmanın ürettiği sonuçlar arayüze aktarılırken, filmlere ait yüksek kaliteli afişler, görseller ve medya dosyaları gerçek zamanlı olarak **TMDB (The Movie Database) API** üzerinden çekilir.

---

## 🛠️ Teknoloji Yığını (Tech Stack)

Projenin kararlı, modüler ve performanslı çalışabilmesi için şu teknolojiler tercih edilmiştir:

### Backend (Arka Plan)
* **Dil:** Python 3.x
* **Framework:** Flask (Mikro web framework)
* **Veri Analitiği & ML:** * `Pandas`: Veri setlerinin işlenmesi, filtrelenmesi ve yönetimi.
  * `Scikit-learn`: Metin verilerini vektörize etmek için **TF-IDF Vectorizer** ve benzerlik skorlaması için **Cosine Similarity**.

### Frontend (Arayüz)
* **Yapı:** HTML5 & CSS3 (Dinamik ve modern responsive arayüz tasarımı)
* **Programlama:** Vanilla JavaScript (ES6+)
* **Asenkron İletişim:** Flask API ve TMDB API ile haberleşme için `Fetch API` mimarisi.

### Veri Kaynakları & Araçlar
* **Veri Seti:** TMDB 5000 Film Veri Seti (`.csv` formatında local depolama)
* **Görsel API:** TMDB API (The Movie Database)
* **Geliştirme Ortamı:** PyCharm / VS Code

---

## ⚙️ Kurulum ve Yerel Ortamda Çalıştırma

Projeyi kendi yerel bilgisayarınızda ayağa kaldırmak için aşağıdaki adımları sırasıyla takip ediniz:

### 1. Gereksinimler
Bilgisayarınızda **Python 3.x** ve **Git** kurulu olduğundan emin olun.

### 2. Projenin Klonlanması
Terminal veya Git Bash kullanarak repoyu bilgisayarınıza indirin:
```bash
git clone [https://github.com/kuzeyisleyen/Sekans.git](https://github.com/kuzeyisleyen/Sekans.git)
cd Sekans
3. Sanal Ortam (Virtual Environment) Kurulumu
Proje bağımlılıklarının izole çalışması için bir sanal ortam oluşturun ve aktif edin:

Bash
# Sanal ortam oluşturma
python -m venv venv

# Sanal ortamı aktif etme (Windows)
venv\Scripts\activate

# Sanal ortamı aktif etme (macOS/Linux)
source venv/bin/activate
4. Bağımlılıkların Yüklenmesi
Gerekli tüm kütüphaneleri sanal ortam içerisine yükleyin:

Bash
pip install flask requests scikit-learn pandas flask-cors
5. API Anahtarı Yapılandırması
Görsellerin TMDB üzerinden sorunsuz çekilebilmesi için:

app.py veya yapılandırma dosyanızda yer alan API anahtarı alanına kendi geçerli TMDB API Key bilginizi tanımlayın.

6. Uygulamanın Başlatılması
Her şey hazır olduğunda Flask sunucusunu çalıştırın:

Bash
python app.py
Uygulama tarayıcınızda otomatik olarak http://127.0.0.1:5000 adresinde yayına başlayacaktır
