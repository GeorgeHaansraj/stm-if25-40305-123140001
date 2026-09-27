# Tugas 2: Perekaman Suara, Analisis Visual, dan Eksperimen Aliasing

Folder ini merupakan hasil pengerjaan **Tugas 02** mata kuliah STM. Fokus tugas ini adalah praktik langsung untuk melihat wujud matematis dan visual dari fenomena *aliasing* pada sistem DSP.

## 🎙️ Rincian Perekaman Akuisisi
- **Sumber Suara:** Vokal bacaan artikel berita nasional.
- **Sumber Derau Statis:** Kipas angin / AC yang mengarah ke area perekaman.
- **Format File Asli:** `.wav` (PCM Uncompressed).
- **Perangkat:** Perekam suara dari *smartphone* diletakkan 0.5 meter di depan sumber derau.

## 📝 Ringkasan Kesimpulan
1. **Analisis Derau**: Derau kipas memiliki pola konstan secara waktu (garis horizontal di STFT) dan lebih mendominasi di rentang spektrum FFT frekuensi rendah.
2. **Efek Aliasing**: Terbukti bahwa memotong laju sampel secara langsung (*naive desimasi \(M\)*) memicu *spectral fold-back*, membuat desis kipas berfrekuensi tinggi memantul dan merusak area frekuensi rendah (*aliasing*). Hal ini berhasil diatasi dengan teknik resample standar (scipy/librosa) karena secara internal metode ini melibatkan Filter Anti-Aliasing sebelum membuang *sample*.