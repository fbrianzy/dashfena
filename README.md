# Dashfena - Dashboard Fenomena BPS Sidoarjo

## Tentang Aplikasi

Dashfena adalah aplikasi web resmi Badan Pusat Statistik (BPS) Kabupaten Sidoarjo untuk memvisualisasikan dan mengelola data fenomena ekonomi, sosial, dan pembangunan. Aplikasi ini menyajikan data secara interaktif dan mudah dipahami untuk mendukung pengambilan keputusan berbasis data.

## Fitur Utama

### Dashboard Interaktif
- Visualisasi data fenomena dalam bentuk grafik dan tabel
- Analisis tren bulanan dengan perhitungan pertumbuhan
- Segmentasi data berdasarkan kategori lapangan usaha dan pengeluaran
- Indikator sentiment untuk memahami arah perkembangan

### Integrasi GitHub Real-Time
- Sinkronisasi otomatis dengan repositori data [database-fenomena](https://github.com/fbrianzy/database-fenomena)
- Sistem caching cerdas untuk performa optimal
- Timestamp sinkronisasi data terkini

### Panel Administrasi
- Manajemen data lengkap dengan operasi CRUD
- Upload dan validasi file CSV
- Editor data dengan preview real-time
- Monitoring cache dan diagnostik sistem

### Desktop Control Panel
- Aplikasi desktop berbasis Tkinter untuk manajemen server
- Monitoring log real-time dengan kategorisasi
- Kontrol server (start, stop, restart)
- Interface modern dengan dark mode support

### Keamanan Terintegrasi
- Autentikasi berbasis session
- Proteksi CSRF token
- Rate limiting pada endpoint sensitif
- Logging aktivitas komprehensif
- Validasi input menyeluruh

## Teknologi

**Backend:** Flask (Python 3.8+)  
**Frontend:** Tailwind CSS 3, Font Awesome 6, Vanilla JavaScript  
**Data Source:** GitHub Repository (CSV)  
**Control Panel:** Tkinter Desktop Application

## Sumber Data

Aplikasi ini menggunakan data dari repositori publik:

**Repositori Data:** [github.com/fbrianzy/database-fenomena](https://github.com/fbrianzy/database-fenomena)

Data mencakup fenomena ekonomi dan sosial Kabupaten Sidoarjo yang dikurasi dari sumber berita terverifikasi dan diperbarui secara berkala.

## Dokumentasi

Untuk dokumentasi teknis lengkap, instalasi, dan konfigurasi, silakan merujuk pada file-file berikut:

- **CONTRIBUTING.md** - Panduan kontribusi pengembangan
- **SECURITY.md** - Kebijakan keamanan dan pelaporan kerentanan
- **CHANGELOG.md** - Riwayat versi dan perubahan

## Deployment

Aplikasi ini dirancang untuk deployment pada production environment dengan konfigurasi yang aman. Pastikan untuk:

- Menggunakan HTTPS pada production
- Mengatur environment variables dengan benar
- Mengaktifkan firewall dan security measures
- Melakukan backup log secara berkala
- Memantau performa dan resource usage

## Status Proyek

**Versi Terkini:** 3.0.0  
**Status:** Production Ready  
**Update Terakhir:** Oktober 2025

## Kontak

**Developer:** Bagus Febriansyah Pratama  
**Email:** dashfena.dev@dashfena.bps.go.id  
**Repository:** [github.com/fbrianzy/dashfena](https://github.com/fbrianzy/dashfena)

## Lisensi

Proyek ini dilisensikan di bawah MIT License. Lihat file LICENSE untuk detail lengkap.

---

**Dashfena** | Visualisasi Data Fenomena BPS Kabupaten Sidoarjo
