# Mini_Project_Tugas_7
# Mini Project: Verifikasi Ijazah Menggunakan OCR dan Image Processing

## 1. Deskripsi Proyek

Proyek ini merupakan prototipe pengolahan citra digital untuk membaca nomor ijazah menggunakan Optical Character Recognition (OCR) dan mendeteksi indikasi keberadaan tanda tangan pada area dokumen yang ditentukan.

Tahapan pemrosesan meliputi grayscale, image enhancement, OCR, thresholding, dan morphological operations. Kinerja OCR dievaluasi menggunakan Character Error Rate (CER).

## 2. Teknologi yang Digunakan

- Python
- Google Colab
- OpenCV
- Tesseract OCR
- Pytesseract
- Matplotlib
- NumPy
- Pandas
- Jiwer

## 3. Metode yang Digunakan

Metode image enhancement yang dibandingkan:

- Grayscale
- CLAHE (Contrast Limited Adaptive Histogram Equalization)
- Histogram Equalization
- Unsharp Masking

Deteksi indikasi tanda tangan dilakukan menggunakan thresholding, morphological opening, morphological closing, dan analisis komponen terhubung.

## 4. Cara Menjalankan Program

1. Buka notebook `MiniProject_Verifikasi_Ijazah.ipynb` melalui Google Colab.
2. Jalankan sel instalasi dependensi untuk memasang library yang diperlukan dan Tesseract OCR.
3. Unggah gambar input berformat `.jpg` atau `.png` ketika diminta.
4. Jalankan seluruh sel kode secara berurutan, mulai dari preprocessing dan image enhancement hingga OCR, evaluasi CER, dan deteksi tanda tangan.
5. Periksa hasil OCR, perbandingan nilai CER, dan keluaran deteksi tanda tangan.

## 5. Hasil Evaluasi

Pada pengujian awal, hasil OCR menunjukkan:

| Metode | CER |
|---|---:|
| Grayscale | 0% |
| CLAHE | 0% |
| Unsharp Masking | 0% |
| Histogram Equalization | 100% |

Grayscale, CLAHE, dan Unsharp Masking menghasilkan pembacaan yang sama dengan ground truth pada gambar uji. Histogram Equalization menghasilkan keluaran OCR kosong pada pengujian tersebut.

Hasil ini hanya berlaku untuk gambar yang diuji dan belum menunjukkan bahwa satu metode selalu lebih unggul pada seluruh jenis dokumen.

## 6. Keterbatasan

- Hasil OCR dipengaruhi oleh kualitas gambar dan ketepatan cropping.
- Koordinat area nomor dan tanda tangan perlu disesuaikan untuk gambar yang berbeda.
- Deteksi tanda tangan merupakan estimasi berdasarkan ciri visual, bukan verifikasi keaslian tanda tangan atau identitas penandatangan.

## 7. Privasi Data

Gunakan gambar yang diizinkan untuk pengujian. Jangan mengunggah ijazah asli yang berisi informasi pribadi ke repository publik. Gunakan gambar sintetis atau gambar yang telah dianonimkan untuk demonstrasi.
