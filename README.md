# 🚗 Araç Kiralama Sistemi (Car Rental System)

Bu proje, **C Programlama Dili** kullanılarak geliştirilmiş, terminal tabanlı bir araç kiralama otomasyonudur. Veri kalıcılığı sağlamak için dosya işlemlerini (File I/O) kullanır; böylece program kapatılsa bile kayıtlar (araçlar, müşteriler ve kiralama geçmişi) saklanır.

## 📋 Özellikler

Bu otomasyon sistemi üç ana modülden oluşur:

### 1. 🚙 Araç Yönetimi
* **Araç Ekleme:** Marka, model ve yıl bilgileriyle yeni araç kaydı. (Otomatik ID atama)
* **Araç Silme:** ID numarasına göre araç silme işlemi.
* **Araç Listeleme:** Kayıtlı tüm araçların durumunu (Müsait/Kirada) listeleme.
* **Araç Arama:** ID ile spesifik araç detaylarını görüntüleme.

### 2. busts_in_silhouette: Müşteri Yönetimi
* **Müşteri Ekleme:** TC Kimlik No (11 hane kontrolü), İsim ve Telefon bilgileriyle kayıt.
* **Müşteri Listeleme:** Kayıtlı tüm müşterileri görüntüleme.
* **Müşteri Arama:** TC Kimlik No ile müşteri sorgulama.

### 3. 🔑 Kiralama ve Teslim İşlemleri
* **Araç Kiralama:** Müsait bir aracı, kayıtlı bir müşteriye kiralama. (Araç durumu otomatik güncellenir).
* **Araç Teslim Alma:** Kiradaki aracı teslim alma ve kiralama geçmişine teslim tarihini işleme.
* **Kiralama Geçmişi:** Tüm eski ve aktif kiralama işlemlerini log dosyasından okuyarak listeleme.

## 🛠 Kullanılan Teknolojiler ve Yöntemler

* **Dil:** C
* **Veri Yapıları:** `struct` (Yapılar) kullanılarak ilişkisel veri modellemesi.
* **Dosya İşlemleri:** `fopen`, `fprintf`, `fscanf`, `remove`, `rename` fonksiyonları ile `.txt` dosyaları üzerinde CRUD (Oluşturma, Okuma, Güncelleme, Silme) işlemleri.
* **Algoritma:** Doğrusal arama (Linear Search) ve durum kontrol algoritmaları.

## 📂 Dosya Yapısı

Program çalıştığında aşağıdaki dosyalar otomatik olarak oluşturulur veya kullanılır:

* `arac.txt`: Araçların veritabanı.
* `musteriler.txt`: Müşteri bilgilerinin tutulduğu dosya.
* `kiralamalar.txt`: Aktif ve geçmiş kiralama kayıtları.
* `arac_id.txt`: Benzersiz araç ID'si üretmek için sayaç dosyası.

## 🚀 Kurulum ve Çalıştırma

Bilgisayarınızda bir C derleyicisi (GCC gibi) yüklü olmalıdır.

1. **Projeyi indirin:**
   ```bash
   git clone [https://github.com/kullaniciadin/arac-kiralama-sistemi.git](https://github.com/kullaniciadin/arac-kiralama-sistemi.git)
   cd arac-kiralama-sistemi

2. **Derleyin:**
   gcc main.c -o arac_kiralama

3. **Çalıştırın:**
   Windows için: arac_kiralama.exe
   Linux/Mac için: ./arac_kiralama
   
