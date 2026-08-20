# Analisis Komparatif Klasifikasi Citra: CNN from Scratch vs Transfer Learning (MobileNetV2)

Proyek ini bertujuan untuk mengevaluasi dan membandingkan performa dua pendekatan utama dalam klasifikasi citra menggunakan Deep Learning: membangun arsitektur *Convolutional Neural Network* (CNN) dari awal (*from scratch*) dan memanfaatkan metode *Transfer Learning* menggunakan model *pretrained* MobileNetV2.

## 📌 Ringkasan Eksperimen

Eksperimen ini dibagi menjadi dua bagian utama:

1.  **Eksperimen 1: CNN from Scratch**
    *   **Dataset:** CIFAR-10 (10 Kelas objek dunia nyata).
    *   **Resolusi:** $32 \times 32 \times 3$ (RGB).
    *   **Arsitektur:** Desain kustom menggunakan Conv2D, BatchNormalization, MaxPooling2D, Dropout, dan Dense Layer.
    *   **Tujuan:** Menguji kemampuan model kustom sederhana untuk belajar dari awal pada dataset objek multi-kelas.

2.  **Eksperimen 2: Transfer Learning**
    *   **Dataset:** Cats vs Dogs (Biner: Kucing dan Anjing).
    *   **Resolusi:** $160 \times 160 \times 3$ (RGB).
    *   **Metode:** Feature Extraction menggunakan model *pretrained* MobileNetV2 (bobot ImageNet) yang dibekukan (*frozen*), diikuti oleh *classifier head* Dense Layer baru.
    *   **Tujuan:** Memanfaatkan pengetahuan model yang sudah dilatih pada dataset masif untuk mencapai akurasi tinggi pada dataset baru dengan waktu pelatihan yang efisien.

## 📁 Struktur Repositori GitHub

Sesuai ketentuan tugas, repositori ini disusun sebagai berikut:

```text
project-cnn-vs-transfer-learning/
├── dataset/
│   └── link_dataset.txt             # Berisi tautan resmi untuk mengunduh dataset
├── notebook/
│   └── cnn_vs_transfer_learning.ipynb # Source code utama dalam format Jupyter Notebook
├── report/
│   └── laporan.pdf                  # Laporan lengkap format IEEE (Maksimal 10 Halaman)
├── README.md                        # Dokumentasi proyek (file ini)
└── requirements.txt                 # Daftar pustaka Python yang diperlukan
