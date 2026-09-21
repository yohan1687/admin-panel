# PERANCANGAN.MD - MILESTONE 1
## Sistem Informasi Koperasi Simpan Pinjam (KSP "Maju Makmur")

---

### 1. Informasi Proyek
- **Topik Proyek**: Sistem Informasi Koperasi Simpan Pinjam
- **Target Platform**: Responsive Web / Mobile-First Application
- **Role Pengguna**: 
  1. **Pengurus / Petugas Admin**: Mengelola data anggota, persetujuan pinjaman, pencatatan simpanan, dan laporan keuangan.
  2. **Anggota Koperasi**: Melihat saldo simpanan (Pokok, Wajib, Sukarela), simulasi & pengajuan pinjaman, riwayat angsuran, serta estimasi SHU.

---

### 2. Hirarki Menu & Arsitektur Informasi (Sitemap)

```
Sistem Informasi Koperasi Simpan Pinjam
├── 0. Autentikasi & Akun
│   ├── Login (Nomor Anggota / NIK & Password)
│   ├── Registrasi Anggota Baru
│   └── Profil Anggota & Pengaturan
│
├── 1. Dashboard Utama
│   ├── Ringkasan Saldo (Simpanan Wajib, Pokok, Sukarela)
│   ├── Kartu Status Pinjaman Berjalan & Jatuh Tempo
│   ├── Quick Action: Setor Simpanan, Ajukan Pinjaman, Bayar Cicilan
│   └── Grafik Arus Kas & Statistik Koperasi
│
├── 2. Data Master (Tabel & Manajemen Data)
│   ├── Master Anggota (Daftar, Status Keaktifan, Filter, CRUD)
│   ├── Master Jenis Simpanan & Produk Pinjaman (Bunga, Tenor)
│   └── Master Petugas / Administrator
│
├── 3. Transaksi Simpan Pinjam (Form Interaktif)
│   ├── Form Pengajuan Pinjaman (Simulasi Angsuran, Plafon, Tenor, Validasi)
│   ├── Form Setor / Tarik Simpanan
│   └── Form Konfirmasi Pembayaran Angsuran
│
└── 4. Laporan & Detail Transaksi
    ├── Rincian Pinjaman & Kartu Angsuran (Jadwal Pembayaran & Status Pelunasan)
    ├── Laporan Buku Tabungan Simpanan
    ├── Laporan Laba Rugi / Alokasi SHU
    └── Cetak Bukti Transaksi Digital (PDF / Print Struk)
```

---

### 3. Konsep ER-D (Entity Relationship Diagram) - Mermaid.js

```mermaid
erDiagram
    ANGGOTA ||--o{ SIMPANAN : "memiliki"
    ANGGOTA ||--o{ PINJAMAN : "mengajukan"
    PINJAMAN ||--o{ ANGSURAN : "memiliki jadwal"
    PENGURUS ||--o{ PINJAMAN : "menyetujui / menolak"
    PENGURUS ||--o{ TRANSAKSI_KAS : "mencatat"

    ANGGOTA {
        string no_anggota PK "Nomor Induk Anggota (misal KSP-2025-001)"
        string nik UK "Nomor Induk Kependudukan"
        string nama_lengkap
        string alamat
        string no_telepon
        string email
        string status_anggota "Aktif / Non-Aktif"
        date tanggal_bergabung
        string password_hash
    }

    SIMPANAN {
        int id_simpanan PK
        string no_anggota FK
        string jenis_simpanan "Pokok / Wajib / Sukarela"
        decimal nominal
        datetime tgl_transaksi
        string bukti_transfer
        string status_verifikasi "Verified / Pending"
    }

    PINJAMAN {
        string no_pinjaman PK "Kode Pinjaman (misal PJ-202505-012)"
        string no_anggota FK
        decimal plafon_pinjaman
        int tenor_bulan "3, 6, 12, 24 bulan"
        float suku_bunga_persen "1.2% per bulan"
        string jenis_bunga "Flat / Menurun"
        decimal cicilan_per_bulan
        string status_pengajuan "Diajukan / Diverifikasi / Disetujui / Ditolak / Lunas"
        date tgl_pengajuan
        date tgl_pencairan
        string id_pengurus FK
    }

    ANGSURAN {
        int id_angsuran PK
        string no_pinjaman FK
        int angsuran_ke
        decimal jumlah_angsuran
        decimal denda
        date tgl_jatuh_tempo
        date tgl_bayar
        string status_bayar "Lunas / Belum / Terlambat"
        string bukti_bayar
    }

    PENGURUS {
        string id_pengurus PK
        string nama_pengurus
        string role "Admin, Bendahara, Ketua"
        string username
        string password_hash
    }

    TRANSAKSI_KAS {
        int id_transaksi PK
        string kode_referensi
        string jenis_arus "Masuk / Keluar"
        decimal jumlah
        string keterangan
        datetime created_at
        string id_pengurus FK
    }
```

---

### 4. User Flow Antarmuka (Flowchart Mermaid.js)

```mermaid
flowchart TD
    Start([Mulai]) --> Login[Halaman Login]
    Login --> AuthCheck{Role?}
    
    AuthCheck -->|Anggota| UserDash[Dashboard Anggota]
    AuthCheck -->|Admin/Pengurus| AdminDash[Dashboard Admin]
    
    UserDash --> MenuPilihan{Pilih Aksi}
    MenuPilihan -->|Cek Saldo & Pinjaman| DetailInfo[Layar Detail Simpanan & Pinjaman]
    MenuPilihan -->|Ajukan Pinjam| FormPinjam[Formulir Pengajuan & Simulasi Cicilan]
    MenuPilihan -->|Bayar Tagihan| BayarCicilan[Upload Bukti Angsuran]
    
    FormPinjam --> SubmitPinjam[Submit Pengajuan]
    SubmitPinjam --> AdminReview[Verifikasi oleh Petugas Admin]
    
    AdminDash --> DataMaster[Halaman Data Master Anggota & Pinjaman]
    DataMaster --> ActionAdmin{Aksi Admin}
    ActionAdmin -->|Tambah / Edit Anggota| FormAnggota[Form Input Master Anggota]
    ActionAdmin -->|Review Pinjaman| ApproveReject[Setujui / Tolak Pinjaman]
    ActionAdmin -->|Lihat Buku Kas| LaporanView[Laporan Rekap & Cetak Struk]
```

---

### 5. Rencana Desain UI & Wireframing (Milestone 1)
1. **Design Tokens & Palette**:
   - **Primary**: Deep Forest Green (`#14532D` / `#16A34A`) mencerminkan stabilitas koperasi & finansial terpercaya.
   - **Secondary / Accent**: Warm Amber / Gold (`#F59E0B`) melambangkan kesejahteraan anggota.
   - **Neutral**: Slate Gray (`#0F172A`, `#334155`, `#F8FAFC`) untuk tipografi jelas & kontras tinggi.
2. **Komponen Reusable**:
   - Status Badges: `Disetujui` (Hijau), `Pending` (Kuning), `Jatuh Tempo` (Merah).
   - Metric Summary Cards (Saldo Pokok, Wajib, Sukarela, dan Sisa Plafon).
   - Form Slider Tenor & Real-time Loan Calculator Preview.
   - Quick Bottom Navigation Bar untuk mobile usability.
