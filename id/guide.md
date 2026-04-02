# Panduan Penggunaan Bokuchi Editor

Panduan ini memperkenalkan cara-cara praktis menggunakan editor Bokuchi.

## Penggunaan Fitur Tab

### Pengeditan Multi-file
- **File Baru**: `Ctrl+N` (Windows/Linux) atau `Cmd+N` (Mac)
- **Buka File**: `Ctrl+O` (Windows/Linux) atau `Cmd+O` (Mac)
- **Beralih Tab**: `Ctrl+Tab` untuk tab berikutnya, `Ctrl+Shift+Tab` untuk tab sebelumnya

### Contoh Praktis
1. Edit dokumen utama
2. Buka materi referensi di tab terpisah
3. Kelola file template di tab terpisah
4. Salin & tempel antar beberapa tab

## Fitur Zoom

### Pengaturan Zoom
- **Perbesar**: `Ctrl++` (Windows/Linux) atau `Cmd++` (Mac)
- **Perkecil**: `Ctrl+-` (Windows/Linux) atau `Cmd+-` (Mac)
- **Atur Ulang**: `Ctrl+0` (Windows/Linux) atau `Cmd+0` (Mac)

### Kasus Penggunaan
- **Presentasi**: Teks besar untuk visibilitas yang lebih baik
- **Pengeditan Detail**: Teks kecil untuk melihat gambaran keseluruhan
- **Monitor Ganda**: Sesuaikan agar pas di satu monitor

## Fitur Tema

### Pergantian Tema
- **Mode Gelap**: Nyaman di mata, cocok untuk sesi kerja yang panjang
- **Mode Terang**: Cocok untuk pencetakan atau bekerja di lingkungan yang terang

### Kustomisasi
- Kustomisasi detail dimungkinkan dengan variabel CSS
- CSS kustom untuk pratinjau juga dapat dikonfigurasi

## Persistensi Status

### Fitur Simpan Otomatis
- Status dipulihkan saat aplikasi dimulai ulang
- Tab yang terbuka, tab aktif, dan konten yang belum disimpan dipertahankan
- Path file juga diingat, sehingga file yang diubah secara eksternal dimuat ulang secara otomatis

### Tips Penggunaan
- Saat menghentikan pekerjaan, cukup tutup aplikasi
- Saat memulai berikutnya, status pekerjaan sebelumnya akan dipulihkan
- Sangat praktis terutama saat bekerja pada beberapa proyek secara paralel

## Penerapan Fitur Variabel

### Pembuatan Template
```markdown
<!-- @var projectName: Proyek Saya -->
<!-- @var version: 1.0.0 -->
<!-- @var author: Nama Anda -->

# Dokumentasi {{projectName}}

Versi: {{version}}
Penulis: {{author}}

## Ringkasan
Dokumen ini menjelaskan proyek {{projectName}}.
```

### Penggunaan Variabel Global
- Tetapkan informasi umum seperti nama perusahaan, nama departemen, nama penulis sebagai variabel global
- Kelola informasi yang konsisten di beberapa dokumen

## Penggunaan Fitur Checkbox

### Manajemen Tugas
```markdown
## Tugas Hari Ini
- [ ] Siapkan materi rapat
- [ ] Lakukan review kode
- [ ] Perbarui dokumentasi
- [x] Periksa email pagi
```

### Manajemen Proyek
- Visualisasikan status kemajuan
- Konfirmasi tugas yang telah selesai
- Bagikan kemajuan dalam tim

## Praktik Terbaik Operasi File

### Konvensi Penamaan File
- Sertakan tanggal: `2025-01-15-catatan-rapat.md`
- Sertakan nama proyek: `proyek-alpha-spesifikasi.md`
- Kontrol versi: `api-docs-v2.md`

### Struktur Folder
```
docs/
├── meetings/
│   ├── 2025-01-15-weekly.md
│   └── 2025-01-22-weekly.md
├── specs/
│   ├── api-spec.md
│   └── ui-spec.md
└── templates/
    ├── meeting-template.md
    └── project-template.md
```

## Ringkasan

Bokuchi Editor lebih dari sekadar editor markdown, menyediakan lingkungan pembuatan dokumen yang efisien.
Editor ini unggul terutama dalam bidang berikut:

- **Dukungan Multi-tasking**: Pengeditan beberapa file secara bersamaan
- **Kemudahan Penggunaan**: Operasi intuitif dan persistensi status
- **Kemampuan Kustomisasi**: Pengaturan fleksibel dengan tema dan variabel
- **Kepraktisan**: Fitur praktis seperti checkbox dan zoom

Dengan menggabungkan fitur-fitur ini, pembuatan dokumen yang lebih efisien dan nyaman menjadi mungkin.
