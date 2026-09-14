# Assignment 1 — Single Layer Perceptron

Implementasi **Single Layer Perceptron (SLP)** untuk klasifikasi biner spesies Iris Setosa dan Iris Versicolor menggunakan Google Sheets dan Python.

## Identitas

* Nama: Aulia Fathus Tsani
* NIM: 24/534388/PA/22661
* Mata Kuliah: Deep Learning
* Tugas: Assignment 1 — Single Layer Perceptron

## Deskripsi

Model Single Layer Perceptron digunakan untuk mengklasifikasikan dua spesies dalam dataset Iris:

* Iris Setosa sebagai kelas `0`
* Iris Versicolor sebagai kelas `1`

Dataset diambil menggunakan fungsi `load_iris()` dari library Scikit-learn. Sebanyak 100 data dari dua kelas digunakan, dengan empat fitur:

* Sepal length
* Sepal width
* Petal length
* Petal width

Data dibagi menjadi:

* 80 data training, terdiri atas 40 Iris Setosa dan 40 Iris Versicolor
* 20 data validation, terdiri atas 10 Iris Setosa dan 10 Iris Versicolor

## Parameter Model

* Learning rate: `0.1`
* Jumlah epoch: `5`
* Bias awal: `0.5`
* Bobot awal: `[0.5, 0.5, 0.5, 0.5]`
* Fungsi aktivasi: Sigmoid
* Batas klasifikasi: `0.5`
* Loss function: Mean Squared Error (MSE)
* Metode pembaruan: Online gradient descent

## Tahapan Perhitungan

1. Mengambil dataset Iris menggunakan `load_iris()`.
2. Memilih data Iris Setosa dan Iris Versicolor.
3. Menggunakan target `0` untuk Iris Setosa dan `1` untuk Iris Versicolor.
4. Membagi data menjadi data training dan validation.
5. Menghitung nilai masukan berdasarkan fitur, bobot, dan bias.
6. Menghitung output menggunakan fungsi aktivasi sigmoid.
7. Menentukan kelas prediksi menggunakan batas `0.5`.
8. Menghitung error dan squared error.
9. Memperbarui bobot dan bias pada setiap data training.
10. Menghitung accuracy dan MSE pada setiap epoch.
11. Melakukan validation menggunakan bobot hasil training tanpa memperbarui bobot.
12. Membandingkan hasil training dan validation melalui tabel dan grafik.

Rumus error, squared error, MSE, accuracy, output, dan pembaruan bobot dikelompokkan ke dalam fungsi. Perulangan digunakan untuk memproses setiap data training, data validation, dan setiap epoch.

## Hasil

| Epoch | Training Accuracy | Validation Accuracy | Training MSE | Validation MSE |
| ----: | ----------------: | ------------------: | -----------: | -------------: |
|     1 |            52.50% |              50.00% |     0.450046 |       0.328014 |
|     2 |            95.00% |              50.00% |     0.037215 |       0.246373 |
|     3 |            97.50% |              50.00% |     0.024224 |       0.175153 |
|     4 |            97.50% |              85.00% |     0.017254 |       0.118946 |
|     5 |            98.75% |             100.00% |     0.012664 |       0.081341 |

Accuracy training meningkat dari 52.50% menjadi 98.75%, sedangkan accuracy validation meningkat dari 50.00% menjadi 100.00%. Nilai MSE training dan validation juga menurun pada setiap epoch. Hasil tersebut menunjukkan bahwa model semakin baik dalam membedakan Iris Setosa dan Iris Versicolor.

## Struktur Repository

```text
Assignment1-Deep-Learning/
├── README.md
├── assignment1_slp_aulia(534388).py
└── hasil/
    ├── hasil_slp.xlsx
    ├── 01_accuracy_training_validation.png
    └── 02_loss_training_validation.png
```

## File Hasil

Program menghasilkan beberapa file:

* `hasil_slp.xlsx`, berisi tabel data awal, pembagian dataset, dan hasil setiap epoch.
* `01_accuracy_training_validation.png`, berisi grafik accuracy training dan validation.
* `02_loss_training_validation.png`, berisi grafik MSE training dan validation.

## Library yang Digunakan

* NumPy
* Pandas
* Matplotlib
* Scikit-learn
* IPython
* Openpyxl

## Cara Menjalankan

Kode dapat dijalankan menggunakan Google Colab.

1. Buka Google Colab.
2. Unggah file `assignment1_slp_aulia(534388).py`.
3. Jalankan seluruh kode.
4. Program akan mengambil dataset Iris secara otomatis.
5. Program akan menampilkan contoh data awal, tabel pembagian dataset, tabel hasil setiap epoch, dan grafik.
6. Tabel dan grafik hasil akan disimpan secara otomatis.

Program tidak memerlukan file CSV atau file dataset tambahan karena dataset Iris diambil langsung melalui Scikit-learn.

## Project Links

* [Google Sheet](https://docs.google.com/spreadsheets/d/1UbDc6-Mrmwye_CvHZPoBBJhFuBKGMMvd/edit)
* [Google Colab](https://colab.research.google.com/drive/1tZj1VYsVCOONwD1P4OJUZn1_mSo6nQKp)
* [GitHub Repository](https://github.com/auliafathustsani/Assignment1-Deep-Learning)

## Referensi

* Fisher, R. A. (1936). The use of multiple measurements in taxonomic problems. *Annals of Eugenics, 7*(2), 179–188.
* Goodfellow, I., Bengio, Y., & Courville, A. (2016). *Deep Learning*. MIT Press.
* [Scikit-learn Iris Dataset](https://scikit-learn.org/stable/modules/generated/sklearn.datasets.load_iris.html)
* [NumPy Documentation](https://numpy.org/doc/)
* [Pandas Documentation](https://pandas.pydata.org/docs/)
* [Matplotlib Documentation](https://matplotlib.org/stable/)
