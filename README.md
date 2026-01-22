# Capstone Movie Project

📱 **Capstone Movie Project** - Aplikasi Mobile untuk UAS Pemrograman Mobile

📋 **Deskripsi Proyek**
Aplikasi Android ini dikembangkan sebagai proyek Ujian Akhir Semester (UAS) untuk mata kuliah Pemrograman Mobile. Aplikasi ini bertujuan untuk menampilkan informasi film dan acara TV terbaru, populer, dan berperingkat tinggi dengan memanfaatkan API dari [The Movie Database (TMDB)](https://www.themoviedb.org/).

✨ **Fitur Utama**
✅ **Daftar Film & TV Show:** Menampilkan katalog film dan acara TV berdasarkan kategori populer, sedang tayang, dan rating tertinggi.

✅ **Fitur Favorit:** Pengguna dapat menandai film atau acara TV sebagai favorit yang disimpan secara lokal.

✅ **Akses Offline:** Data yang telah dimuat akan disimpan dalam database lokal sehingga tetap dapat dilihat tanpa koneksi internet.

✅ **Pencarian:** Memudahkan pengguna mencari judul film atau acara TV tertentu.

✅ **Keamanan Data:** Implementasi Certificate Pinning untuk koneksi jaringan dan enkripsi database menggunakan SQLCipher.

🛠 **Teknologi yang Digunakan**
*   **Bahasa Pemrograman:** Kotlin
*   **Minimum SDK:** API 21 (Android 5.0 Lollipop)
*   **Arsitektur:** MVVM dengan Clean Architecture & Modularization
*   **Library Utama:**
    *   **Retrofit** - Untuk integrasi API/Networking.
    *   **Room Database** - Untuk penyimpanan data lokal (dengan SQLCipher).
    *   **Koin** - Untuk Dependency Injection.
    *   **Coroutine Flow** - Untuk Reactive Programming.
    *   **Glide** - Untuk pemrosesan dan loading gambar.
    *   **ViewBinding** - Untuk interaksi dengan layout UI.

📁 **Struktur Proyek**
Proyek ini menggunakan pendekatan **Modularization**:
```text
.
├── app/                # Layer Presentasi (UI Utama, Activity, Fragment, ViewModel)
├── core/               # Layer Data & Domain (Repository, Database, API, Use Cases)
└── favorite/           # Dynamic Feature Module (Fitur Favorit)
```

🚀 **Cara Menjalankan Proyek**
1.  **Clone repository**
    ```bash
    git clone https://github.com/mikailalex/CapstoneMovieProject.git
    ```
2.  **Buka di Android Studio**
    *   Pastikan menggunakan versi terbaru (Rekomendasi: Arctic Fox atau lebih baru).
    *   Tunggu hingga proses Gradle sync selesai.
3.  **Konfigurasi environment**
    *   Aplikasi ini memerlukan API Key dari TMDB.
    *   Tambahkan `BASE_URL` dan konfigurasi API lainnya jika diperlukan di `gradle.properties` atau melalui `BuildConfig`.
4.  **Build dan Run**
    *   Pilih perangkat/emulator.
    *   Klik tombol **Run** atau tekan `Shift + F10`.

📸 **Screenshots & Demo**
![Demo](https://user-images.githubusercontent.com/67632360/123531199-b6c79c80-d72c-11eb-9923-bbb8949062fc.gif)

📝 **Dokumentasi Fitur**
1.  **Clean Architecture**
    Memisahkan kode menjadi layer Data, Domain, dan Presentation untuk meningkatkan *testability* dan *maintainability*.
2.  **Dynamic Feature Module**
    Modul `favorite` diimplementasikan sebagai *dynamic feature* untuk mengoptimalkan ukuran APK awal.
3.  **Database Encryption**
    Menggunakan **SQLCipher** untuk memastikan data lokal yang disimpan dalam Room Database aman terenkripsi.

🧪 **Testing**
```bash
# Menjalankan unit tests
./gradlew test

# Menjalankan instrumented tests
./gradlew connectedAndroidTest
```

📊 **Hasil Implementasi**
| Komponen | Status | Keterangan |
| :--- | :--- | :--- |
| CRUD Operations | ✅ Selesai | Menggunakan Room Database & SQLCipher |
| API Integration | ✅ Selesai | Menggunakan Retrofit & TMDB API |
| Architecture | ✅ Selesai | MVVM + Clean Architecture |
| Security | ✅ Selesai | Certificate Pinning & Obfuscation |

🤝 **Kontributor**
*   **M Mikail Alexander Firdaus - 42422045** - Developer & Student
*   **Muhammad Faran Rikhul Barqi - 42422035** - Developer & Student
*   **Arda Priambada - 42422012** - Developer & Student

📄 **Lisensi**
Copyright 2024 Capstone Movie Project
Lisensi: [MIT License](https://opensource.org/licenses/MIT)
