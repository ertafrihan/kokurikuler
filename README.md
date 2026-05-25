# 🏫 SPMB & Galeri Ekskul — SMK Budi Bakti Ciwidey

Landing page premium, responsif, dan interaktif untuk **Sistem Penerimaan Murid Baru (SPMB) SMK Budi Bakti Ciwidey Tahun Ajaran 2026/2027**, dilengkapi dengan fitur **Instagram-style Stories Gallery** untuk menjelajahi kegiatan ekstrakurikuler sekolah.

Proyek ini dibangun menggunakan arsitektur frontend modern berbasis **Vanilla JS** dan **Tailwind CSS** tanpa dependensi berat (tanpa bundler/compiler), menjamin performa muat halaman yang instan, efisiensi tinggi, dan kemudahan deployment.

---

## 🚀 Fitur Unggulan Proyek

### 1. Halaman Utama (`index.html`) — Landing Page SPMB
*   **Hero Section Dinamis:** Grid 2 kolom dengan ilustrasi pemrograman modern berbasis inline SVG yang dinamis, statistik pencapaian sekolah, dan tombol CTA utama.
*   **Program Keahlian:** Grid interaktif yang menyajikan 3 jurusan unggulan:
    1.  **PPLG** (Pengembangan Perangkat Lunak & Gim)
    2.  **DKV** (Desain Komunikasi Visual)
    3.  **BRP** (Bisnis Ritel & Pemasaran)
*   **Fasilitas Unggulan Carousel:** Penjelajah sarana belajar (Lab Komputer, Studio DKV, Business Center, Collaboration Hub) dengan transisi navigasi dots & arrows yang mulus tanpa bug loncatan tata letak (*double-padding fix*).
*   **Social Proof & FAQ:** Testimoni alumni ter-integrasi, logo mitra industri terkemuka, dan *Collapsible FAQ Accordion* interaktif dengan penutupan otomatis (*auto-collapse logic*).
*   **Floating WhatsApp Helpdesk Widget:** Fitur bantuan mengambang premium di pojok kanan bawah lengkap dengan:
    -   Riak lingkaran berdenyut (*pulsing indicator halo*).
    -   Lencana notifikasi merah (*unread badge*) untuk menarik interaksi calon siswa.
    -   Jendela Popover interaktif yang memudar halus saat dibuka/tutup.
    -   Tautan WhatsApp direct chat dengan pesan pembuka otomatis (*pre-filled text*).

### 2. Halaman Galeri (`galeri.html`) — Instagram & TikTok-Style Stories
*   **Horizontal Stories Tray (Nampan Cerita):** 
    -   Desain lingkaran cerita gradasi Instagram yang familiar.
    -   Fitur **Klik-Seret (Mouse Drag-to-Scroll)** di desktop dengan inersia sentuh yang sangat luwes.
    -   Penyelarasan scroll aman (*Safe Scroll Centering CSS*) yang mencegah lingkaran cerita pertama terpotong di layar HP.
*   **Instagram Stories-Style Progress Bar:** Bilah progres atas yang dibagi menjadi beberapa segmen sesuai dengan isi cerita (berjalan dinamis dari 0% ke 100% dan mendukung ketukan navigasi kiri/kanan segmen).
*   **TikTok-Style Action Sidebar:** Panel kaca melayang di tepi kanan dalam modal cerita:
    -   **Tombol Love (Suka):** Animasi mikro memantul (*pop/bounce scale*) saat diklik dengan penyimpanan status (*state tracking*) mandiri per ekskul.
    -   **Tombol Share (Bagikan):** Secara otomatis menyalin tautan mendalam (*deep-link*) cerita tersebut ke clipboard pengguna.
*   **Toast Notification Glassmorphic:** Memunculkan notifikasi melayang indah *"Tautan cerita berhasil disalin!"* sesaat setelah tombol Share ditekan.
*   **Otomatisasi Deep-Linking:** Halaman dapat dimuat langsung menuju cerita spesifik menggunakan parameter kueri URL (contoh: `galeri.html?story=4` akan langsung otomatis membuka modal cerita Paskibra).
*   **Direct Instagram Shortcut:** Lingkaran cerita ke-6 dan spanduk spanduk promosi (CTA) di bawah halaman yang mengarah langsung ke akun Instagram resmi sekolah `@info.smkbudibakticiwidey`.

---

## 🛠️ Spesifikasi Teknologi

*   **HTML5:** Struktur semantik penuh untuk menunjang performa SEO dan pembaca layar (*accessibility*).
*   **Tailwind CSS (Play CDN):** Untuk pengembangan desain visual yang premium, fleksibel, responsif, dan konsisten.
*   **Vanilla JavaScript:** Logika fungsionalitas murni tanpa dependensi framework eksternal (seperti React/Vue) demi kecepatan optimal.
*   **Google Fonts:** Tipografi modern menggunakan font *Plus Jakarta Sans* dan *Inter*.
*   **Vector Graphic Assets:** Ilustrasi berbasis SVG kustom yang ringan, tajam di semua jenis layar (Retina/4K), dan termuat instan.

---

## 📁 Struktur Folder Proyek

```bash
kokurikuler/
├── assets/
│   ├── img/
│   │   ├── favicon.png             # Logo Emblem Sekolah (AI-generated premium)
│   │   ├── logo.png                # Logo Sekolah Resmi
│   │   ├── story_pramuka.svg       # Ilustrasi cerita Pramuka
│   │   ├── story_futsal.svg        # Ilustrasi cerita Futsal
│   │   ├── story_tech_club.svg     # Ilustrasi cerita IT Club
│   │   ├── story_art_club.svg      # Ilustrasi cerita Paduan Suara
│   │   └── story_paskibra.svg      # Ilustrasi cerita Paskibra
│   ├── desktop-uiux.jpeg           # Dokumentasi Mockup Desktop
│   └── mobile-uiux.jpeg            # Dokumentasi Mockup Mobile
├── index.html                      # Landing Page Utama SPMB
├── galeri.html                     # Halaman Galeri Cerita Ekskul
├── prd.md                          # Product Requirement Document
└── README.md                       # Dokumentasi Utama Proyek (File Ini)
```

---

## 💻 Cara Menjalankan Proyek Secara Lokal

Karena proyek ini tidak memerlukan server build atau instalasi compiler (murni frontend statis), Anda dapat menjalankannya dengan sangat mudah:

### Opsi A: Buka Langsung (Tanpa Server)
1.  Klik dua kali berkas `index.html` pada komputer Anda.
2.  Berkas akan langsung terbuka dengan sempurna di peramban web (Google Chrome, Microsoft Edge, Safari, Firefox, dll.).

### Opsi B: Menggunakan Local Development Server (Direkomendasikan)
Untuk mendapatkan pengalaman transisi yang optimal lintas browser, disarankan menjalankan server lokal sederhana:
*   **Jika menggunakan VS Code:** Instal ekstensi **Live Server**, buka folder proyek ini, kemudian klik tombol **"Go Live"** di bar status bawah VS Code.
*   **Menggunakan Python (Terminal):**
    ```bash
    python -m http.server 8000
    ```
    Buka `http://localhost:8000` di peramban Anda.
*   **Menggunakan Node.js / NPM (npx):**
    ```bash
    npx serve .
    ```
    Buka alamat yang tertera di terminal Anda.

---

## 📝 Catatan Kustomisasi

1.  **Nomor Kontak WhatsApp Helpdesk:**
    Untuk mengubah tujuan nomor admin pada floating widget, cari elemen `<a>` di dalam `index.html` pada baris ke-1086 dan perbarui nomor `628123456789` serta parameter teksnya.
2.  **Akun Instagram Resmi:**
    Tautan Instagram pada `galeri.html` terhubung ke `https://www.instagram.com/info.smkbudibakticiwidey`. Anda dapat mengubah tautan ini dengan mencari kata kunci `instagram` di dalam berkas `galeri.html` untuk disesuaikan dengan akun sosial media resmi lainnya.

---

*Dikembangkan secara profesional dan didedikasikan untuk peningkatan mutu sistem pendaftaran dan dokumentasi kreatif siswa di **SMK Budi Bakti Ciwidey**.*
