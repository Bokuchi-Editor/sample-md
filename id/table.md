# Sampel Tata Letak Tabel

Berkas ini menunjukkan bagaimana pengaturan **Tata Letak Tabel (Pratinjau)** di Bokuchi memengaruhi cara tabel ditampilkan.

> Lokasi pengaturan: **Pengaturan → Lanjutan → Tata Letak Tabel (Pratinjau)**

Berpindah-pindah antara tiga mode sambil melihat pratinjau berkas ini akan memperlihatkan perbedaannya secara langsung.

## Perbedaan tiap mode

| Mode | Lebar kolom | Konten panjang |
|------|-------------|----------------|
| Lebar kolom sama | Semuanya sama | Dilipat di dalam sel |
| Sesuaikan dengan konten (lipat di sel) — bawaan | Mengikuti konten | Dilipat di dalam sel |
| Sesuaikan dengan konten (gulir horizontal) | Mengikuti konten | Tabel menggulir horizontal |

---

## Contoh 1: Hanya satu kolom yang berisi deskripsi panjang

Di sinilah perbedaan **Lebar sama** dan **Sesuaikan dengan konten** paling terlihat.
Pada mode **Lebar sama**, kolom singkat seperti "ID", "Tanggal", dan "Status" mendapat lebar yang sama dengan kolom deskripsi yang panjang, sehingga kolom deskripsi menjadi kolom sempit dan tinggi yang sulit dibaca.
Pada mode **Sesuaikan dengan konten**, kolom deskripsi mendapat ruang yang dibutuhkannya dan kolom singkat tetap ringkas.

| ID | Tanggal | Deskripsi | Status |
|----|---------|-----------|--------|
| 001 | 2026-05-01 | Menambahkan alur registrasi pengguna baru. Mendukung login OAuth2 (Google / GitHub / Microsoft) dan email/sandi, serta meminta pengguna mengisi profil saat login pertama. | Selesai |
| 002 | 2026-05-03 | Mengganti lapisan cache ke Redis, menurunkan rata-rata waktu respons API dari 280ms menjadi 95ms. | Selesai |
| 003 | 2026-05-05 | Memperbarui paginasi pada API pencarian. Pengambilan total kini dilakukan secara malas, mempercepat respons pertama. | Tinjauan |
| 004 | 2026-05-08 | Memperbarui UI pengaturan notifikasi: dukungan tema gelap/terang dan peningkatan aksesibilitas. | Berjalan |

---

## Contoh 2: Banyak kolom yang tidak muat di layar

Di sinilah keunggulan mode **gulir horizontal**.
Pada mode **Lebar sama** dan **Sesuaikan dengan konten (lipat di sel)** setiap sel dipersempit agar seluruh tabel pas dengan panel. Pada mode **gulir horizontal** setiap kolom mempertahankan lebar alaminya dan tabelnya yang menggulir ke samping.

| ID Pesanan | Pelanggan | Waktu Pesan | SKU | Produk | Qty | Harga (Rp) | Subtotal (Rp) | Alamat Pengiriman | Pengiriman | Penanggung Jawab |
|------------|-----------|-------------|-----|--------|-----|------------|---------------|-------------------|------------|------------------|
| ORD-20260501-001 | Adi Pratama | 2026-05-01 09:14 | SKU-A1023 | Laptop Performa Tinggi Pro 15 | 1 | 28.500.000 | 28.500.000 | Jl. Sudirman Kav. 52-53, Jakarta Selatan, DKI Jakarta 12190 | Terkirim | Sato |
| ORD-20260502-007 | Bunga Lestari | 2026-05-02 13:22 | SKU-B2240 | Keyboard Mekanik Nirkabel | 2 | 2.150.000 | 4.300.000 | Jl. Asia Afrika No. 8, Bandung, Jawa Barat 40111 | Dalam Perjalanan | Suzuki |
| ORD-20260503-014 | Cahyo Nugroho | 2026-05-03 18:47 | SKU-C0098 | Monitor 4K 32 inci HDR | 1 | 10.300.000 | 10.300.000 | Jl. Diponegoro No. 100, Surabaya, Jawa Timur 60241 | Disiapkan | Tanaka |

---

## Contoh 3: Tabel perbandingan sederhana

Jika semua sel pendek, ketiga mode hampir tidak menunjukkan perbedaan yang terlihat. Tabel perbandingan sehari-hari tetap nyaman dibaca pada mode mana pun.

| Item | Paket A | Paket B | Paket C |
|------|---------|---------|---------|
| Bulanan | Rp 130rb | Rp 280rb | Rp 580rb |
| Penyimpanan | 10 GB | 100 GB | 1 TB |
| Dukungan | Email | Email / Chat | Telepon 24 jam |

---

## Cara mencobanya

1. Buka berkas ini di Bokuchi dan tampilkan pratinjau
2. Buka **Pengaturan → Lanjutan → Tata Letak Tabel (Pratinjau)**
3. Pilih **Lebar kolom sama** dan perhatikan kolom deskripsi pada Contoh 1 menjadi sempit dan tinggi
4. Kembalikan ke **Sesuaikan dengan konten (lipat di sel)** (bawaan) dan perhatikan kolom mengikuti panjang konten
5. Pindah ke **Sesuaikan dengan konten (gulir horizontal)** dan pastikan tabel pada Contoh 2 menggulir secara horizontal

> HTML yang dihasilkan tombol **Download** (di kanan atas pratinjau) juga mengikuti pengaturan ini.
