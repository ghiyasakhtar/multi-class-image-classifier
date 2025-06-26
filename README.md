# Klasifikasi Gambar

## Deskripsi Singkat
Proyek ini adalah model klasifikasi citra yang dibangun menggunakan Convolutional Neural Network (CNN) untuk mengklasifikasikan gambar ke dalam 6 kategori: `buildings`, `forest`, `glacier`, `mountain`, `sea`, dan `street`. Model ini dilatih di Google Colab dan diekspor ke format `.tflite` dan `TensorFlow.js`.

## Struktur Folder
submission
├── tfjs_model
│   ├── group1-shard1of5.bin     # File model TensorFlow.js shard (1 dari 5)
|   ├── group1-shard2of5.bin     # File model TensorFlow.js shard (2 dari 5)
|   ├── group1-shard3of5.bin     # File model TensorFlow.js shard (3 dari 5)
|   ├── group1-shard4of5.bin     # File model TensorFlow.js shard (4 dari 5)
|   ├── group1-shard5of5.bin     # File model TensorFlow.js shard (5 dari 5)
│   └── model.json               # Konfigurasi model TensorFlow.js
├── tflite
│   ├── model.tflite             # Model hasil konversi ke TFLite
│   └── label.txt                # Label kelas model TFLite
├── saved_model
│   ├── saved_model.pb           # Model TensorFlow SavedModel format
│   └── variables               # Variabel model SavedModel
├── notebook.ipynb              # Notebook Google Colab
├── README.md                   # Dokumentasi proyek
└── requirements.txt            # Daftar dependensi Python

## Teknologi & Library
- Python 3.x
- TensorFlow
- TensorFlow.js
- Scikit-learn
- NumPy
- Matplotlib
- Google Colab

## Arsitektur Model
Model CNN yang digunakan memiliki beberapa layer Conv2D, MaxPooling2D, BatchNormalization, dan Dense Layer. Model dilatih dengan teknik augmentasi data dan callback seperti EarlyStopping, ReduceLROnPlateau, dan ModelCheckpoint.

## Dataset
Dataset terdiri dari 6 kelas:
- `buildings`
- `forest`
- `glacier`
- `mountain`
- `sea`
- `street`


## Cara Menjalankan Proyek

1. **Clone atau buka Colab Notebook**
2. **Pasang dependensi** (jika tidak pakai Colab):

```bash
pip install -r requirements.txt
```

3. Latih model (atau load model yang sudah disimpan).
4. Ekspor model ke TFLite dan/atau TensorFlow.js.
5. Gunakan `label.txt` untuk menginterpretasi hasil prediksi.

## Ekspor Model
- TFLite: model.tflite
- TensorFlow.js: direktori tfjs_model/ (gunakan tensorflowjs.converters.save_keras_model(...))

## Penulis
Ghiyas Akhtar Razi Ramadhan