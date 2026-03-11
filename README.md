# Klasifikasi Gambar Fruits 100
**Dibuat oleh:** Humaira Zeanova  

---

## Deskripsi Proyek

Proyek ini membangun model klasifikasi gambar buah menggunakan subset **10.400 gambar, 26 kategori** dari dataset [Fruits-100 (Kaggle)](https://www.kaggle.com/datasets/marquis03/fruits-100).

## Arsitektur Model

| Komponen | Detail |
|---|---|
| Backbone | EfficientNetB0 (pretrained ImageNet) |
| Input size | 224 × 224 × 3 |
| Jumlah kelas | 26 |
| Training | 2-phase (head training + fine-tuning 100 layer terakhir) |
| Loss | CategoricalCrossentropy (label smoothing 0.1) |
| Optimizer | Adam |

## Performa Model
| Kategori | Accuracy |
|---|---|
| Training | 99.74% |
| Testing | 92.88% |
| Validation | 93.27% |
| Test Loss | 0.9071 |

## Training History Plot
<Figure size 1400x500 with 2 Axes><img width="1389" height="495" alt="image" src="https://github.com/user-attachments/assets/f1101572-be04-4cd3-acb6-15b04ab56fe5" />

## Inference
<Figure size 1300x1300 with 9 Axes><img width="1289" height="1318" alt="image" src="https://github.com/user-attachments/assets/54c9cfc0-6848-4620-9f25-22aa042c67a0" />

## Struktur Folder

```
submission/
├── tfjs_model/          # TensorFlow.js model (model.json + shard)
├── tflite/              # TFLite model + label.txt
├── saved_model/         # TF SavedModel format
├── notebook.ipynb       # Notebook lengkap
├── README.md            # File ini
└── requirements.txt     # Daftar dependensi
```

## Cara Menjalankan

1. Buka `notebook.ipynb` di Google Colab  
2. Aktifkan runtime GPU: *Runtime → Change runtime type → T4 GPU*  
3. Jalankan semua sel secara berurutan (*Runtime → Run all*)  

## Dependensi Utama

Lihat `requirements.txt` untuk versi lengkap.  
Install dengan: `pip install -r requirements.txt`
