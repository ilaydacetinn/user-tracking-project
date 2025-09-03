# User Tracker Projesi

Bu proje, Django REST Framework ve Vue.js kullanılarak geliştirilmiş, kullanıcıları, gönderilerini, albümlerini ve yapılacak işlerini takip etmek için tasarlanmış bir web uygulamasıdır.

## Özellikler

- **Kullanıcı Yönetimi:** Kullanıcıları listeleme ve detaylarını görüntüleme.
- **Gönderiler:** Kullanıcıya özel gönderileri ve gönderilere ait yorumları görüntüleme.
- **Albümler ve Fotoğraflar:** Kullanıcıya özel albümleri ve albümlerin içindeki fotoğrafları görüntüleme.
- **Yapılacaklar Listesi:** Kullanıcıya özel yapılacaklar listesini görüntüleme ve durumlarını değiştirme.
- **Modern Arayüz:** TailwindCSS kullanılarak oluşturulmuş, temiz ve modern bir kullanıcı arayüzü.

## Teknolojiler

### Backend
-   **Django 5.1.6**
-   **Django REST Framework 3.16.0**
-   **psycopg2-binary 2.9.10** (PostgreSQL veritabanı için)
-   **Faker** (dummy data oluşturmak için)

### Frontend
-   **Vue.js 3.5.13**
-   **Vue Router 4.5.0**
-   **Pinia 3.0.2** (State Management)
-   **TailwindCSS 3.4.1**
-   **Axios 1.8.4** (API istekleri için)
-   **Vite 6.2.0** (Development ve Build aracı)

## Kurulum

### 1. Backend Kurulumu

1.  `backend` dizinine gidin.
2.  Gerekli Python kütüphanelerini yüklemek için bir sanal ortam oluşturun ve etkinleştirin:
    ```bash
    python -m venv venv
    source venv/bin/activate  # macOS/Linux
    venv\Scripts\activate.bat  # Windows
    ```
3.  `req.txt` dosyasındaki bağımlılıkları yükleyin:
    ```bash
    pip install -r req.txt
    ```
4.  Veritabanı ayarlarınızı `usertracker/settings.py` içinde düzenleyin.
5.  Migrasyonları çalıştırın ve veritabanı şemasını oluşturun:
    ```bash
    python manage.py makemigrations core
    python manage.py migrate
    ```
6.  İsteğe bağlı olarak, dummy verileri oluşturmak için `fill_data.py` scriptini çalıştırın:
    ```bash
    python manage.py shell
    exec(open('scripts/fill_data.py').read())
    ```
7.  Backend sunucusunu başlatın:
    ```bash
    python manage.py runserver
    ```

### 2. Frontend Kurulumu

1.  `frontend` dizinine gidin.
2.  Node.js bağımlılıklarını yükleyin:
    ```bash
    npm install
    ```
3.  Frontend uygulamasını başlatın:
    ```bash
    npm run dev
    ```

Artık uygulamaya `http://127.0.0.1:5173` adresinden erişebilirsiniz.
