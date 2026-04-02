<!-- @var title: Tes Variabel Lokal -->
<!-- @var author: Pengguna Uji Coba -->
<!-- @var date: 2026-03-07 -->
<!-- @var version: 1.0.0 -->

# {{title}}

Dokumen ini adalah tes fitur variabel lokal.

## Informasi Dasar

- **Penulis**: {{author}}
- **Tanggal**: {{date}}
- **Versi**: {{version}}

## Perbandingan dengan Variabel Global

Dengan membuka [Pengaturan] > Variabel Global > Tambah Variabel Baru
dan mengatur "Nama Variabel" = globalVar, "Nilai" = Global,
tampilan berikut akan berubah di pratinjau dengan variabel yang diterapkan.

Nilai yang ditetapkan oleh variabel global: **{{globalVar}}**

## Prioritas Variabel Lokal

Variabel lokal memiliki prioritas lebih tinggi daripada variabel global.
Coba daftarkan variabel global dan lihat apakah tampilan berikut berubah.
Juga, coba hapus deklarasi variabel di awal dan lihat apakah tampilannya berubah.

Nilai variabel lokal `title`: {{title}}
Nilai variabel lokal `author`: {{author}}
