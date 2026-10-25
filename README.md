<div align="center">

# 🛡️ AllSafe-QRIS

### Periksa dulu, bayar kemudian.
Lapisan verifikasi risiko kode QR yang bekerja **sebelum** transaksi diselesaikan.

**Mata Kuliah:** Analisis dan Rancangan Perangkat Lunak<br>

</div>

---

## 👥 Identitas Kelompok

**Kelompok 2** | Ujian Tengah Semester

**Anggota:**

1. Suheil Heru Madhani (25343166)
2. Nasywa Althafunnisa (24343017)
3. Muhammad Zikri (24343120)
4. Elsa Anggrayni (24343086)
5. Hikmah Fauzan (24343117)

**Mata Kuliah:** Analisis dan Rancangan Perangkat Lunak<br>
**Dosen Pengampu:** Randi Proska Sandra, S.Pd., M.Sc.<br>
**Program Studi:** Informatika, Departemen Elektronika<br>
**Institusi:** Fakultas Teknik, Universitas Negeri Padang (2026)

---

## 📖 Tentang Aplikasi

**AllSafe-QRIS** bukan aplikasi pembayaran baru. Aplikasi ini adalah **lapisan pemeriksaan (safety layer)** yang berjalan saat pengguna memindai kode QR. Sebelum hasil pindai diteruskan ke e-wallet atau peramban, AllSafe-QRIS memeriksa terlebih dahulu apakah kode tersebut aman.

### 🎯 Masalah yang Diselesaikan
Penipuan QRIS marak terjadi, misalnya stiker QR palsu yang ditempel menimpa QR resmi di kasir, QR donasi atau refund palsu, dan tautan phishing. Aplikasi e-wallet saat ini tidak memeriksa keaslian QR. Keamanan sepenuhnya bergantung pada kejelian pengguna, dan korban baru menyadarinya setelah dana terkirim.

### ✨ Keunggulan (Novelty)

| Keunggulan | Penjelasan |
|---|---|
| 🔍 **Paham struktur QRIS** | Memeriksa data QRIS (Merchant ID, NMID, TID) sekaligus tautan phishing dalam satu alur |
| 🇮🇩 **Berbasis modus lokal** | Aturan deteksi disusun dari modus yang marak di Indonesia, seperti QR tempel di kasir |
| 📍 **Cocokkan konteks lokasi** | Nama merchant pada QR dibandingkan dengan tempat pengguna berada |
| 💬 **Alasan mudah dipahami** | Setiap hasil disertai penjelasan awam sehingga meningkatkan literasi keamanan digital |
| ⚡ **Pemeriksaan sebelum transaksi** | Berjalan sebagai lapisan pemindai (share-sheet atau shortcut kamera), bukan alat yang dibuka setelah kejadian |

### 🧩 Fitur Utama
- Pemindaian QR lewat kamera dan Share Sheet
- Validasi QRIS (format, NMID, TID) dan pemeriksaan domain tautan, termasuk tautan pendek dan domain yang menyerupai domain resmi
- Klasifikasi risiko **Aman / Waspada / Bahaya** beserta alasannya
- Verifikasi QRIS gerai oleh pelaku usaha
- Pelaporan QR mencurigakan oleh komunitas
- Peninjauan laporan dan pembaruan *rule set* oleh admin lewat web admin, tanpa rilis ulang aplikasi

### 🔄 Alur Singkat

```
Pindai QR → Uraikan isi → QRIS / Tautan? → Validasi → Cocokkan rule set
        → Cocokkan konteks lokasi → Status risiko + alasan → Lanjut / Batal
```

---

## 🛠️ Metode Pengembangan

Pengembangan memakai **Agile (Scrum)** karena spesifikasi layanan eksternal belum final, aturan deteksi terus diperbarui, dan setiap sprint menghasilkan fitur yang dapat diuji.

| Sprint | Cakupan |
|---|---|
| Sprint 1 | Pemindaian dan validasi QRIS/tautan (FR-001, FR-002) |
| Sprint 2 | Klasifikasi risiko dan keputusan pengguna (FR-003, FR-004) |
| Sprint 3 | Pelaporan dan peninjauan admin (FR-005, FR-006) |
| Sprint 4 | Verifikasi merchant dan penyempurnaan (FR-007) |

---

## 👤 Pengguna Sasaran

| Persona | Gambaran |
|---|---|
| **Rina Amelia** (Konsumen) | Mahasiswi informatika, 21 tahun, memakai QRIS setiap hari, jarang membaca nama penerima, dan langsung memasukkan PIN saat terburu-buru |
| **Justin Bieber** (Merchant) | Pemilik warung makan, 45 tahun, QRIS statis di meja kasir terbuka, rawan tertimpa stiker QR palsu |
| **Admin / Moderator** | Meninjau laporan komunitas dan memperbarui *rule set* |

---

## 🗂️ Struktur Repositori

```
AllSafe-Qris/
├── Diagram/
│   ├── BPMN As-is dan To-be
│   ├── User Persona
│   └── UML: Use Case, Activity, Class Diagram
├── Dokumen/
│   ├── SRS
│   ├── Use Case Specification
│   └── RTM (Requirement Traceability Matrix)
└── README.md
```

| Folder | Isi |
|---|---|
| [📁 Diagram](./Diagram) | Pemodelan proses bisnis, persona, dan diagram UML |
| [📁 Dokumen](./Dokumen) | Spesifikasi kebutuhan perangkat lunak dan ketertelusuran kebutuhan |

---

<div align="center">

**Kelompok 2 · Informatika · Universitas Negeri Padang · 2026**

</div>
