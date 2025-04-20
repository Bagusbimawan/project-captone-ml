# Sistem Rekomendasi Wisata Indonesia

Proyek ini adalah sistem rekomendasi wisata di Indonesia yang menggunakan teknik pemrosesan teks dan perhitungan similarity untuk memberikan rekomendasi tempat wisata berdasarkan kemiripan deskripsi dan karakteristik tempat wisata.

## Deskripsi

Sistem ini menggunakan model machine learning untuk menganalisis deskripsi tempat wisata dan memberikan rekomendasi tempat wisata serupa. Sistem dapat merekomendasikan tempat wisata berdasarkan input nama tempat wisata yang sudah ada dalam database.

## Struktur Proyek

```
├── rekomendasi.ipynb     # Notebook utama untuk pembuatan model dan sistem rekomendasi
├── convert.ipynb         # Notebook untuk konversi model ke format JSON
├── model_wisata.h5      # Model yang disimpan dalam format H5
├── model_wisata.json    # Model yang dikonversi ke format JSON
└── wisata.csv           # Dataset tempat wisata
```

## Fitur

- Rekomendasi tempat wisata berdasarkan similarity deskripsi
- Mendukung 19 destinasi wisata populer di Indonesia
- Output berupa daftar rekomendasi dengan informasi detail setiap tempat wisata

## Cara Penggunaan

1. Load model dan data:
```python
import joblib

# Load model
model_wisata = joblib.load("model_wisata.h5")
```

2. Gunakan fungsi rekomendasi:
```python
def rekomendasi_wisata(nama_wisata: str, top_n: int = 5):
    # Fungsi akan mengembalikan list rekomendasi tempat wisata
    # berdasarkan input nama wisata yang diberikan
    pass

# Contoh penggunaan
rekomendasi = rekomendasi_wisata("Borobudur", top_n=5)
```

## Dependensi

- Python 3.12.7
- pandas
- joblib
- scikit-learn (untuk text vectorization)

## Dataset

Dataset berisi informasi tentang 19 destinasi wisata populer di Indonesia, termasuk:
- Nama tempat wisata
- Deskripsi detail
- Informasi lokasi
- Karakteristik unik

## Konversi Model

Proyek ini menyediakan kemampuan untuk mengkonversi model dari format H5 ke JSON menggunakan `convert.ipynb` untuk keperluan deployment atau penggunaan di platform berbeda.

## Catatan

- Pastikan semua dependensi terinstal sebelum menjalankan sistem
- Gunakan Python versi 3.12.7 atau yang lebih baru
- Dataset dapat diperbarui dengan menambahkan tempat wisata baru ke `wisata.csv`