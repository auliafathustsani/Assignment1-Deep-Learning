# Assignment 1 — Single Layer Perceptron

Implementasi Single Layer Perceptron (SLP) untuk klasifikasi biner data Iris Setosa dan Iris Versicolor menggunakan Google Sheet dan Python.

## Identitas

* Nama: Aulia Fathus Tsani
* NIM: 24/534388/PA/22661
* Mata Kuliah: Deep Learning
* Tugas: Assignment 1 — Single Layer Perceptron

## Deskripsi

Model digunakan untuk mengklasifikasikan dua kelas:

* Iris Setosa sebagai kelas `0`
* Iris Versicolor sebagai kelas `1`

Dataset terdiri atas 100 data dengan empat fitur:

* Sepal length
* Sepal width
* Petal length
* Petal width

Data dibagi menjadi:

* 80 data training
* 20 data validation

Masing-masing kelompok data memiliki jumlah kelas yang seimbang.

## Parameter Model

* Learning rate: `0.1`
* Jumlah epoch: `5`
* Bias awal: `0.5`
* Bobot awal: `[0.5, 0.5, 0.5, 0.5]`
* Fungsi aktivasi: Sigmoid
* Batas klasifikasi: `0.5`
* Loss function: Mean Squared Error (MSE)

## Tahapan Perhitungan

1. Memasukkan data Iris Setosa dan Iris Versicolor.
2. Mengubah label kelas menjadi nilai numerik `0` dan `1`.
3. Membagi data menjadi data training dan validation.
4. Menghitung nilai masukan model menggunakan bobot dan bias.
5. Mengubah nilai tersebut menggunakan fungsi sigmoid.
6. Menentukan kelas prediksi menggunakan batas `0.5`.
7. Menghitung error dan squared error.
8. Memperbarui bobot dan bias pada setiap data training.
9. Menghitung accuracy dan MSE pada setiap epoch.
10. Membandingkan hasil Google Sheet dengan hasil Python.

## Hasil

| Epoch | Training Accuracy | Validation Accuracy | Training MSE | Validation MSE |
| ----: | ----------------: | ------------------: | -----------: | -------------: |
|     1 |            52.50% |              50.00% |     0.449889 |       0.328951 |
|     2 |            95.00% |              50.00% |     0.037452 |       0.247289 |
|     3 |            97.50% |              50.00% |     0.024372 |       0.175892 |
|     4 |            97.50% |              85.00% |     0.017357 |       0.119381 |
|     5 |            98.75% |             100.00% |     0.012740 |       0.081581 |

Hasil perhitungan Python sama dengan hasil perhitungan pada Google Sheet. Accuracy training meningkat dari 52.50% menjadi 98.75%, sedangkan accuracy validation meningkat dari 50.00% menjadi 100.00%. Nilai MSE training dan validation juga terus menurun selama proses training.

## Struktur Repository

```text
Assignment1-Deep-Learning/
├── README.md
└── assignment1_slp_aulia(534388).py
```

## Library yang Digunakan

* NumPy
* Pandas
* Matplotlib
* IPython

## Cara Menjalankan

Kode dapat dijalankan menggunakan Google Colab.

1. Buka Google Colab.
2. Unggah file `assignment1_slp_aulia(534388).py`.
3. Jalankan seluruh kode.
4. Program akan menampilkan tabel hasil training dan validation.
5. Grafik akan disimpan dengan nama:

   * `01_accuracy_training_validation.png`
   * `02_loss_training_validation.png`

Data Iris sudah dimasukkan langsung ke dalam kode sehingga tidak memerlukan file CSV tambahan.

## Project Links

* [Google Sheet](https://docs.google.com/spreadsheets/d/1UbDc6-Mrmwye_CvHZPoBBJhFuBKGMMvd/edit)
* [Google Colab](https://colab.research.google.com/drive/1tZj1VYsVCOONwD1P4OJUZn1_mSo6nQKp)
* [GitHub Repository](https://github.com/auliafathustsani/Assignment1-Deep-Learning)

## Referensi

* Fisher, R. A. (1936). The use of multiple measurements in taxonomic problems. *Annals of Eugenics, 7*(2), 179–188.
* Goodfellow, I., Bengio, Y., & Courville, A. (2016). *Deep Learning*. MIT Press.
* [NumPy Documentation](https://numpy.org/doc/)
* [Matplotlib Documentation](https://matplotlib.org/)
