# Contoh Diagram Mermaid

Koleksi diagram Mermaid untuk memverifikasi rendering di Bokuchi.

## Diagram Alur

```mermaid
graph TD
    A[Mulai] --> B{Apakah berhasil?}
    B -- Ya --> C[Bagus!]
    B -- Tidak --> D[Debug]
    D --> B
    C --> E[Rilis]
```

## Diagram Urutan

```mermaid
sequenceDiagram
    participant Pengguna
    participant Frontend
    participant Backend
    participant DB

    Pengguna->>Frontend: Klik "Simpan"
    Frontend->>Backend: POST /api/save
    Backend->>DB: INSERT INTO documents
    DB-->>Backend: OK
    Backend-->>Frontend: 200 Berhasil
    Frontend-->>Pengguna: Tampilkan notifikasi
```

## Diagram Gantt

```mermaid
gantt
    title Jadwal Proyek
    dateFormat  YYYY-MM-DD
    section Perencanaan
    Persyaratan      :done,    req, 2025-01-01, 14d
    Desain           :done,    des, after req, 10d
    section Pengembangan
    Frontend         :active,  fe,  after des, 30d
    Backend          :         be,  after des, 25d
    section Pengujian
    Uji Integrasi    :         test, after fe, 14d
    Rilis            :milestone, rel, after test, 0d
```

## Diagram Kelas

```mermaid
classDiagram
    class Editor {
        -content: string
        -theme: string
        +onChange(content)
        +setTheme(theme)
    }
    class Preview {
        -markdown: string
        +render()
    }
    class Tab {
        -id: string
        -title: string
        -isModified: boolean
        +save()
        +close()
    }
    Editor --> Preview : merender
    Tab --> Editor : berisi
```

## Diagram Status

```mermaid
stateDiagram-v2
    [*] --> Kosong
    Kosong --> Mengedit : File Baru / Buka File
    Mengedit --> Diubah : Konten Berubah
    Diubah --> Tersimpan : Simpan (Ctrl+S)
    Tersimpan --> Diubah : Konten Berubah
    Diubah --> Ditutup : Tutup tanpa menyimpan
    Tersimpan --> Ditutup : Tutup
    Ditutup --> Kosong : Tab terakhir ditutup
    Kosong --> [*]
```

## Diagram Lingkaran

```mermaid
pie title Bahasa yang Didukung
    "Inggris" : 1
    "Jepang" : 1
    "Tionghoa (Sederhana)" : 1
    "Tionghoa (Tradisional)" : 1
    "Korea" : 1
    "Spanyol" : 1
    "Prancis" : 1
    "Jerman" : 1
    "Portugis (BR)" : 1
    "Rusia" : 1
    "Hindi" : 1
    "Arab" : 1
    "Indonesia" : 1
    "Vietnam" : 1
```

## Tes Penanganan Error

Blok berikut berisi kesalahan sintaks yang disengaja untuk memverifikasi tampilan error:

```mermaid
invalid diagram syntax !!!
this should show an error message
```
