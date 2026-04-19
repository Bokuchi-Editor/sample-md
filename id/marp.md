---
marp: true
theme: default
paginate: true
header: 'Bokuchi Editor'
footer: 'Editor Markdown offline yang gratis'
---

<!-- _class: lead -->
<!-- _paginate: false -->
<!-- _header: '' -->
<!-- _footer: '' -->

![w:160](../images/bokuchi-icon.png)

# Bokuchi Editor

### Editor Markdown offline yang gratis
### untuk Windows, macOS, dan Linux

---

## Apa itu Bokuchi?

- Sebuah **editor Markdown** yang berjalan sepenuhnya di komputer Anda
- **Tanpa cloud**, tanpa akun, tanpa pelacakan — file Anda tetap di lokal
- **Pratinjau real-time** saat Anda mengetik
- **Lintas platform**: Windows · macOS · Linux
- **Open source** dan gratis digunakan

> Slide deck ini ditulis dalam Markdown dan dirender oleh fitur Marp Bokuchi.

---

## Mengapa Bokuchi?

| | |
|---|---|
| **Offline-first** | Berfungsi tanpa koneksi internet |
| **Pratinjau real-time** | Lihat hasil render saat mengetik |
| **Pengeditan multi-tab** | Buka banyak file, sesi dipulihkan otomatis |
| **Fitur lengkap** | Variabel, KaTeX, Mermaid, Marp, dan lainnya |
| **14 bahasa UI** | English, 日本語, 中文, Español, हिन्दी, … |

---

## Editor & Pratinjau Berdampingan

![bg right:55% fit](../images/editor-split-view-01.png)

- **Tampilan terbagi** — edit di kiri, pratinjau di kanan
- Mode **hanya editor** / **hanya pratinjau** juga tersedia
- Scroll tetap **tersinkronisasi**
- Ganti mode kapan saja dengan `Ctrl+Shift+1/2/3`

---

## Sekilas Antarmuka

![bg right:55% fit](../images/ui-overview-annotated-01.png)

- **Bilah tab** untuk file yang dibuka
- **Pohon folder** untuk navigasi
- Panel **outline** untuk daftar heading
- **Bilah status** dengan zoom & statistik
- Panel **pratinjau** di sebelah kanan

---

## Pengeditan Multi-Tab

![bg right:55% fit](../images/tabs-horizontal-01.png)

- Buka **banyak file** sekaligus
- **Drag & drop** untuk mengatur urutan
- **Pemulihan sesi** — lanjutkan dari tempat terakhir
- `Ctrl+Tab` / `Ctrl+Shift+Tab` untuk berpindah
- Tab **horizontal atau vertikal**

---

## Pohon Folder

![bg right:55% fit](../images/folder-tree-panel-01.png)

- Jelajahi folder mana saja sebagai **ruang kerja**
- Buat, ubah nama, hapus file langsung di tempat
- Cocok untuk **repositori dokumen** dan sistem catatan
- Selalu tersinkron dengan editor

---

## Panel Outline

![bg right:55% fit](../images/outline-panel-01.png)

- Menampilkan semua **heading** di dokumen
- Klik untuk **melompat** ke bagian tertentu
- Penting untuk **dokumen panjang**, spesifikasi, dan notulen
- Diperbarui secara langsung saat Anda mengedit

---

## Toolbar Markdown

![bg right:55% fit](../images/toolbar-overview-01.png)

- Satu klik untuk **tebal**, *miring*, heading, daftar
- **Tabel**, **blok kode**, **tautan**, **gambar**
- **Konversi tabel** dari TSV / CSV
- Tak perlu mengingat setiap simbol Markdown

---

## Variabel — Placeholder yang Dapat Digunakan Ulang

![bg right:50% fit](../images/variables-preview-01.png)

```markdown
<!-- @var projectName: Bokuchi -->
<!-- @var version: 1.0.0 -->

# Dokumentasi {{projectName}}

Versi: {{version}}
```

- Variabel **lokal**: dideklarasikan di dalam dokumen
- Variabel **global**: dibagikan ke semua dokumen
- Lokal lebih diutamakan daripada global

---

## KaTeX — Matematika yang Elegan

![bg right:50% fit](../images/katex-preview-01.png)

Inline: $E = mc^2$

Blok:

$$
\int_{-\infty}^{\infty} e^{-x^2}\,dx = \sqrt{\pi}
$$

- Dukungan penuh persamaan **LaTeX**
- Dirender **seketika** di pratinjau

---

## Mermaid — Diagram dari Teks

![bg right:50% fit](../images/mermaid-preview-01.png)

````markdown
```mermaid
graph TD
  A[Mulai] --> B{OK?}
  B -- Ya --> C[Rilis]
  B -- Tidak --> D[Debug]
  D --> B
```
````

- **Flowchart**, **sequence**, **class**, **gantt**, dan lainnya
- Diagram tetap berada di **version control** sebagai teks biasa

---

## Marp — Slide dari Markdown

Anda sedang melihat salah satunya sekarang.

```markdown
---
marp: true
---

# Slide 1

Halo!

---

# Slide 2

- Poin A
- Poin B
```

- Aktifkan di **Pengaturan → Lanjutan → Rendering Extensions**
- Gunakan **tombol panah** di mode Pratinjau saja
- Fullscreen & thumbnail grid sudah tersedia

---

## Tema

![bg left:50% fit](../images/themes-default-01.png)
![bg fit](../images/themes-dark-01.png)

- **5 tema bawaan** — Default, Dark, Darcula, Pastel, Vivid
- Tema terpisah untuk **editor** dan **pratinjau**
- Mendukung **CSS** kustom

---

## Pencarian & Penggantian

![bg right:55% fit](../images/search-panel-01.png)

- Mencari dalam file saat ini
- **Pencarian lintas tab** di semua file yang dibuka
- Opsi **regex** dan sensitif huruf besar/kecil
- Ganti satu per satu, atau ganti semua

---

## Pintasan Keyboard (beberapa yang penting)

| Aksi | Windows / Linux | macOS |
|--------|-----------------|-------|
| File baru | `Ctrl+N` | `Cmd+N` |
| Buka file | `Ctrl+O` | `Cmd+O` |
| Simpan | `Ctrl+S` | `Cmd+S` |
| Tab berikutnya | `Ctrl+Tab` | `Ctrl+Tab` |
| Perbesar / Perkecil | `Ctrl++` / `Ctrl+-` | `Cmd++` / `Cmd+-` |
| Pengaturan | `Ctrl+,` | `Cmd+,` |

---

## Dapatkan Bokuchi

- **Situs web**: https://bokuchi.com/
- **Unduh**: https://github.com/Bokuchi-Editor/bokuchi/releases
- **Dokumentasi**: https://doc.bokuchi.com
- **Kode sumber**: https://github.com/Bokuchi-Editor/bokuchi

Gratis dan open source.
Tanpa akun. Tanpa cloud. Tanpa pelacakan.

---

<!-- _class: lead -->
<!-- _paginate: false -->
<!-- _header: '' -->
<!-- _footer: '' -->

# Terima kasih!

### Selamat menulis dengan Bokuchi ✍️

![w:120](../images/bokuchi-icon.png)
