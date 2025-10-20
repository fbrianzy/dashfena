# Kebijakan Keamanan

Keamanan aplikasi Dashfena adalah prioritas utama kami. Dokumen ini menjelaskan kebijakan keamanan dan prosedur pelaporan kerentanan.

## Versi yang Didukung

Pembaruan keamanan diberikan untuk versi berikut:

| Versi | Status Keamanan |
|-------|-----------------|
| 3.0.x | ✅ Dukungan Penuh |
| 2.0.x | ⚠️ Security Only |
| 1.0.x | ❌ End of Life |

**Rekomendasi:** Gunakan versi terbaru (3.0.x) untuk keamanan maksimal.

## Pelaporan Kerentanan Keamanan

Jika Anda menemukan kerentanan keamanan pada aplikasi Dashfena, **jangan membuat public issue**. Laporkan secara private melalui:

### Kontak Keamanan

**Email:** report@dashfena.dev  
**Subject:** [SECURITY] - Deskripsi Singkat Masalah

### Informasi yang Diperlukan

Untuk mempercepat proses penanganan, sertakan informasi berikut:

1. **Deskripsi Kerentanan**
   - Penjelasan detail tentang masalah keamanan
   - Komponen atau modul yang terpengaruh
   - Tingkat keparahan (Critical, High, Medium, Low)

2. **Langkah Reproduksi**
   - Cara mereproduksi kerentanan
   - Kondisi atau konfigurasi yang diperlukan
   - Screenshot atau video (jika memungkinkan)

3. **Dampak Potensial**
   - Risiko terhadap sistem atau data
   - Pengguna yang terpengaruh
   - Skenario eksploitasi

4. **Saran Mitigasi** (opsional)
   - Solusi sementara yang dapat diterapkan
   - Rekomendasi perbaikan jangka panjang

### Timeline Respons

| Tahap | Waktu | Tindakan |
|-------|-------|----------|
| Konfirmasi | 24 jam | Penerimaan laporan |
| Analisis Awal | 72 jam | Klasifikasi severity |
| Investigasi | 5-7 hari | Analisis mendalam |
| Perbaikan | Bervariasi | Pengembangan patch |
| Rilis Patch | Sesuai severity | Update keamanan |
| Disclosure | Setelah patch | Publikasi advisory |

### Klasifikasi Severity

**Critical (CVSS 9.0-10.0)**
- Remote code execution
- Authentication bypass
- Full system compromise
- Kebocoran data sensitif massal

**High (CVSS 7.0-8.9)**
- Privilege escalation
- SQL injection
- XSS yang berdampak signifikan
- CSRF pada fungsi kritis

**Medium (CVSS 4.0-6.9)**
- Information disclosure terbatas
- Denial of service
- Session management issues
- Input validation bypass

**Low (CVSS 0.1-3.9)**
- Minor information leakage
- Low-impact configuration issues
- Edge case vulnerabilities

## Fitur Keamanan Aplikasi

Dashfena dilengkapi dengan:

- ✅ Session-based authentication
- ✅ CSRF token protection
- ✅ Input validation dan sanitization
- ✅ Rate limiting
- ✅ Comprehensive logging
- ✅ Secure file upload handling
- ✅ Environment-based configuration
- ✅ SQL injection prevention

## Praktik Keamanan Pengguna

Untuk menjaga keamanan deployment Anda:

- Gunakan HTTPS pada production
- Ganti credential default
- Update aplikasi secara berkala
- Monitor log secara rutin
- Backup data secara teratur
- Batasi akses admin
- Aktifkan firewall
- Gunakan strong passwords

## Kebijakan Disclosure

Kami menerapkan **Coordinated Vulnerability Disclosure**:

1. Kerentanan dilaporkan secara private
2. Tim melakukan investigasi dan develop patch
3. Patch dirilis untuk versi yang didukung
4. Security advisory dipublikasikan setelah patch tersedia
5. Credit diberikan kepada reporter (jika diinginkan)

## Penghargaan Keamanan

Kami menghargai peneliti keamanan yang melaporkan kerentanan secara bertanggung jawab:

- ✅ Pengakuan di security advisory
- ✅ Credit di release notes
- ✅ Hall of Fame listing
- ✅ Komunikasi langsung dengan tim

## Batasan Scope

**Dalam Scope:**
- Aplikasi web Dashfena
- Desktop control panel
- API endpoints
- Authentication mechanism
- Data processing logic

**Luar Scope:**
- Social engineering attacks
- Physical attacks
- Third-party dependencies (report ke upstream)
- GitHub platform issues
- Denial of service (kecuali ada exploit khusus)

## Kontak

**Security Team:** report@dashfena.dev  
**General Inquiries:** dashfena.dev@dashfena.bps.go.id  
**Response Time:** 24 jam untuk isu keamanan

## Pembaruan Kebijakan

Kebijakan ini ditinjau setiap 6 bulan atau setelah incident keamanan untuk memastikan relevansi dan efektivitas.

**Terakhir Diperbarui:** Oktober 2025  
**Versi Kebijakan:** 1.0

---

Terima kasih telah membantu menjaga keamanan Dashfena.
