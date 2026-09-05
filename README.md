# 230441100055_230441100135_Tugas2CNN__PraktikumB_DeepLearningA

Tugas 2 CNN - Praktikum B Deep Learning

Repository ini berisi implementasi dan perbandingan dua model Convolutional Neural Network (CNN) pada dataset CIFAR-10 untuk memenuhi tugas mata kuliah Deep Learning.

Anggota Kelompok
1. Abd. Based - 230441100055
2. Aditya - 230441100138

---

Ringkasan Eksperimen & Perbandingan Model

Pada eksperimen ini, digunakan 25 Epoch,Batch Size 64, Optimizer Adam, dan teknik Data Augmentation (RandomCrop & RandomHorizontalFlip) untuk membandingkan dua arsitektur model:

| Metrik Evaluasi | Model A (Custom CNN) | Model B (Mini-ResNet) |
| :--- | :--- | :--- |
| **Total Parameter** | 620.810 | **150.474** (Lebih efisien) |
| **Waktu Training (25 Epoch)** | ~18,1 Menit | ~22,2 Menit |
| **Akurasi Akhir (Test Set)** | 82% | **84%** |

---

Kesimpulan
1. Pencapaian Target: Kedua model berhasil melampaui target akurasi di atas 80% (Model A mencapai 82% dan Model B mencapai 84%) berkat penerapan Data Augmentation dan peningkatan jumlah epoch menjadi 25.
2. Efisiensi Arsitektur:Model B (Mini-ResNet) menunjukkan performa yang lebih unggul secara efisiensi. Meskipun memiliki jumlah parameter yang jauh lebih sedikit dibanding Model A (~4x lipat lebih sedikit), Model B mampu memberikan akurasi yang lebih tinggi. Hal ini membuktikan efektivitas dari residual connection dalam melatih model yang lebih dalam tanpa pembengkakan parameter yang berlebihan.
3. Analisis Kelas: Berdasarkan Confusion Matrix dan Classification Report, kedua model sama-sama sangat handal dalam mengenali objek benda mati (seperti mobil, truk, dan kapal), namun masih memiliki tingkat kebingungan yang wajar pada kelas hewan yang mirip secara visual (seperti kucing dan anjing).
