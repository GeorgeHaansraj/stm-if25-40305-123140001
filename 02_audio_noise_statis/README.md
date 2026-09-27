# Analisis Sinyal Suara & Noise Statis (Audio Signal Fundamentals)

Repository ini berisi pengerjaan tugas Modul 01: Audio Signal Fundamentals (Sample Rate Conversion & Anti-Aliasing) untuk mata kuliah IF25-40305 Sistem Teknologi Multimedia (STM).

## 📌 Deskripsi Proyek

Proyek ini mendemonstrasikan konsep dasar pemrosesan sinyal audio digital (DSP), khususnya terkait dengan manipulasi laju sampel (_sample rate_). Eksperimen dilakukan menggunakan Python untuk menganalisis fenomena _aliasing_ dan mengimplementasikan teknik _resampling_ yang sesuai dengan standar industri.

## 🎯 Tujuan Pembelajaran

Berdasarkan modul hands-on, proyek ini bertujuan untuk:

1. Menganalisis standar penggunaan laju sampel di industri (misal: 8 kHz untuk telepon, 16 kHz untuk model AI seperti Whisper, 44.1 kHz untuk Audio CD, dan 48 kHz untuk video/YouTube).
2. Membedakan antara sekadar mengubah metadata `sr` (_sample rate_) dengan proses _resampling_ hakiki secara matematis.
3. Mengamati fenomena _spectral fold-back_ (Aliasing) ketika frekuensi tinggi menyamar menjadi frekuensi rendah palsu.
4. Menerapkan mekanisme _Downsampling_ (Desimasi \(M\)) beserta penggunaan Filter Anti-Aliasing (LPF).
5. Menerapkan tahapan _Upsampling_ (Interpolasi \(L\)) melalui proses _Zero-Stuffing_ dan _Reconstruction Low-Pass Filtering_.
6. Melakukan konversi laju sampel rasio pecahan (non-kelipatan bulat).

## 📁 Struktur Repository

- `1_audio_resampling.ipynb` : Notebook hands-on bagian 1 (Fokus pada konversi _sample rate_ dan efek _aliasing_).
- `2_audio_visual_representation.ipynb` : Notebook hands-on bagian 2 (Fokus pada representasi visual audio dan _noise_ statis).
- `audio_original.wav` : Berkas audio mentah (_raw_) yang digunakan sebagai bahan analisis utama.

## 🛠️ Teknologi & Pustaka yang Digunakan

Proyek ini dijalankan menggunakan lingkungan Google Colab dengan pustaka utama berikut:

- `numpy`: Manipulasi array numerik sinyal.
- `matplotlib.pyplot`: Visualisasi bentuk gelombang dan spektrogram.
- `scipy.signal`: Pemrosesan sinyal digital (Filter Butterworth, sintesis chirp).
- `librosa`: Analisis audio dan _resampling_ standar industri.
- `soundfile`: Pembaca dan penyimpan berkas audio (WAV/FLAC).

## 🚀 Cara Penggunaan

1. Buka file `.ipynb` menggunakan **Google Colab**.
2. Pastikan file `audio_original.wav` diunggah (_upload_) ke _session storage_ Colab Anda sebelum menjalankan _cell_ kode.
3. Jalankan sel kode secara berurutan (_Run all_).
